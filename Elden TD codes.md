
# **Animations local script partial fix :**

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Events = ReplicatedStorage:WaitForChild("Events")
local AnimateTowerEvent = Events:WaitForChild("AnimateTowerEvent")

local activeAnimations = {}

local function setAnimation(object, animName)
	local humanoid = object:WaitForChild("Humanoid")
	local animationsFolder = object:WaitForChild("Animations")
	
	if humanoid and animationsFolder then
		local AnimationObject = animationsFolder:WaitForChild(animName)
		
		if AnimationObject then
			local Animator = humanoid:FindFirstChild("Animator") or Instance.new("Animator", humanoid)
			local AnimationTrack = Animator:LoadAnimation(AnimationObject)
			return AnimationTrack
		end
	end
end

local function playAnimation(object, animName)
	local AnimationTrack = setAnimation(object, animName)
	
	if AnimationTrack then
		AnimationTrack:Play()
		activeAnimations[object] = activeAnimations[object] or {}
		table.insert(activeAnimations[object], AnimationTrack)
	else
		warn("No Animation track found")
		return
	end
end

local function stopAnimations(object)
	if activeAnimations[object] then
		for _, track in ipairs(activeAnimations[object]) do
			track:Stop()
		end
		activeAnimations[object] = nil
	end
end

workspace.Entities.ChildAdded:Connect(function(object)
	playAnimation(object, "Walk")
end)

workspace.Units.ChildAdded:Connect(function(object)
	playAnimation(object, "Idle")
end)

AnimateTowerEvent.OnClientEvent:Connect(function(unit, animName)
	if animName == "Attack" then
		stopAnimations(unit)
	end
	playAnimation(unit, animName)
	if animName == "Attack" then
		local humanoid = unit:FindFirstChild("Humanoid")
		if humanoid then
			local idleTrack = setAnimation(unit, "Idle")
			if idleTrack then
				idleTrack.Stopped:Wait()
				idleTrack:Play()
			end
		end
	end
end)

```
---

# **Original Animations local script :**

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Events = ReplicatedStorage:WaitForChild("Events")
local AnimateTowerEvent = Events:WaitForChild("AnimateTowerEvent")

local function setAnimation(object, animName)
	local humanoid = object:WaitForChild("Humanoid")
	local animationsFolder = object:WaitForChild("Animations")
	
	if humanoid and animationsFolder then
		local AnimationObject = animationsFolder:WaitForChild(animName)
		
		if AnimationObject then
			local Animator = humanoid:FindFirstChild("Animator") or Instance.new("Animator", humanoid)
			local AnimationTrack = Animator:LoadAnimation(AnimationObject)
			return AnimationTrack
		end
	end
end



local function playAnimation(object, animName)
	local AnimationTrack = setAnimation(object, animName)
	
	if AnimationTrack then
		AnimationTrack:Play()
	else
		warn("No Animation track found")
		return
	end
end



workspace.Entities.ChildAdded:Connect(function(object)
	playAnimation(object, "Walk")
end)

workspace.Units.ChildAdded:Connect(function(object)
	playAnimation(object, "Idle")
end)

AnimateTowerEvent.OnClientEvent:Connect(function(unit, animName)
	playAnimation(unit, animName)
end)
```

---

# **Original Unit Module Script :**

```lua
local PhysicsService = game:GetService("PhysicsService")
local ServerStorage = game:GetService("ServerStorage")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local Events = ReplicatedStorage:WaitForChild("Events")
local SpawnUnitEvent = Events:WaitForChild("SpawnUnit")
local AnimateTowerEvent = Events:WaitForChild("AnimateTowerEvent")

local unit = {}


-- Find the target with the highest health
function FindNearestTarget(newUnit)
	local MaxDistance = 20
	local NearestTarget = nil

	for i, target in ipairs(workspace.Entities:GetChildren()) do
		local Distance = (target.HumanoidRootPart.Position - newUnit.HumanoidRootPart.Position).Magnitude
		if Distance < MaxDistance then
			NearestTarget = target
			MaxDistance = Distance
		end
	end
	return NearestTarget
end




-- VFX 
local particleEmitters = {
	{name = "1", emitCount = 10},
	{name = "2", emitCount = 1},
	{name = "3", emitCount = 1},
	{name = "4", emitCount = 20},
	{name = "5", emitCount = 20},
	{name = "6", emitCount = 20},
	{name = "7", emitCount = 1},
	{name = "8", emitCount = 10},
	{name = "9", emitCount = 2}
}

local function emitParticlesWhenSpawned(unit)
	local torso = unit:FindFirstChild("Torso")
	if torso then
		local vfxAttachment = torso:FindFirstChild("VFX")
		if vfxAttachment then
			for i = 1, #particleEmitters do
				local emitterConfig = particleEmitters[i]
				local emitter = vfxAttachment:FindFirstChild(emitterConfig.name)
				if emitter and emitter:IsA("ParticleEmitter") then
					emitter:Emit(emitterConfig.emitCount)
				end
			end
		else
			warn("VFX attachment not found in the entity's Torso.")
		end
	else
		warn("Torso not found in the entity.")
	end
end





-- Units Attacking
function unit.Attack(newUnit)
	local target = FindNearestTarget(newUnit)
	
	if target and target:FindFirstChild("Humanoid") and target.Humanoid.Health > 0 then
		
		local TargetCFrame = CFrame.lookAt(newUnit.HumanoidRootPart.Position, target.HumanoidRootPart.Position)
		newUnit.HumanoidRootPart.BodyGyro.CFrame = TargetCFrame
		
		AnimateTowerEvent:FireAllClients(newUnit, "Attack")
		target.Humanoid:TakeDamage(45)
	end
	
	task.wait(4)
	
	unit.Attack(newUnit)
end




-- Spawn Units
function unit.Spawn(player, name, cframe)
	local UnitExists = ReplicatedStorage.Units:FindFirstChild(name)
	
	if UnitExists then 
		local newUnit = UnitExists:Clone()
		newUnit:SetPrimaryPartCFrame(cframe)
		newUnit.Parent = workspace.Units
		
		local BodyGyro = Instance.new("BodyGyro")
		BodyGyro.MaxTorque = Vector3.new(math.huge, math.huge, math.huge)
		BodyGyro.D = 0
		BodyGyro.CFrame = newUnit.HumanoidRootPart.CFrame
		BodyGyro.Parent = newUnit.HumanoidRootPart

		for i, object in newUnit:GetDescendants() do
			if object:IsA("BasePart") or object:IsA("MeshPart") or object:IsA("Part") then
				object.CollisionGroup = "Units"
				object.Anchored = false
			end
		end
		
		coroutine.wrap(unit.Attack)(newUnit)
		task.wait(0.01)
		emitParticlesWhenSpawned(newUnit, cframe)
	else
		warn("Unit not found: ", name)
	end
end

SpawnUnitEvent.OnServerEvent:Connect(unit.Spawn)

return unit

```