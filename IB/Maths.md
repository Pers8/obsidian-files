---
tags: [MOC,math]
---
[[📝Dashboard]] > [[Maths]]
<br/>
$$\huge{MATHS}$$
$$
HL
$$
<br/>

# Theme 1: Nombre et Algèbre
1. [[Logarithmes]]
2. [[Séries et Séquences]]
3. [[Théorème Binomial]]
4. [[Nombres complexes]]
5. [[Permutations et combinations]]

# Theme 2: Fonctions
1. [[Fonctions quadratiques]]
2. [[Etude graphique des fonctions quadratiques]]
3. [[Formules de Viète]]
4. [[Position relative parabole et droite]]
5. [[Polynômes]]
# Theme 3: Géométrie et Trigonométrie
1. [[Radians]]
2. [[Lois des sinus et cosinus]]
3. [[Cercle trigonométrique]]
4. [[Identités trigonométriques]]
5. [[Vecteurs]]

# Theme 4: Statistique et Probabilité

1. [[Probabilité discrètes]]
2. [[Distribution discrètes]]
3. [[Distribution binomiale]]
4. [[Distribution normale]]
5. [[Statistiques I]]
6. [[Fonction de densité de probabilité]]

# Theme 5: Etude du fonction
1. [[Dérivation]]
2. [[Intégration]]
3. [[Cinématique]]
4. [[Equations différentielles]]
5. [[Série Maclaurin]]
6. [[Règle de l'Hôpital]]

```lua
local Ranks = {}
local spr = require(game.ReplicatedStorage.Spring)
local TweenService = game:GetService("TweenService")
local HoverHandler = require(script.Parent.HoverHandler)

------------------------------
-- BACKGROUND FADE
------------------------------
function Ranks:fadeBackground(targetTransparency, duration)
	if self.bgTween then
		self.bgTween:Cancel()
	end
	self.bgTween = game:GetService("TweenService"):Create(
		self.gui,
		TweenInfo.new(duration, Enum.EasingStyle.Linear),
		{BackgroundTransparency = targetTransparency}
	)
	self.bgTween:Play()
end

------------------------------
-- BLUR EFFECT HANDLING
------------------------------
function Ranks:handleBlurEffect(enable)
	if self.lightingBlur then
		self.lightingBlur:Destroy()
		self.lightingBlur = nil
	end

	if enable then
		self.lightingBlur = self.gui.RankBlur:Clone()
		self.lightingBlur.Parent = game:GetService("Lighting")
		self.lightingBlur.Enabled = true
		self.gui.RankBlur.Enabled = false
	else
		self.gui.RankBlur.Enabled = false
	end
end

------------------------------
-- HACKING TEXT EFFECT
------------------------------
function Ranks:hackingTextEffect(textLabel, revealTime)
	local originalText = textLabel.Text
	local textLength = #originalText
	local symbols = {"$", "*", "\"", "+", "@", "#", "%", "&", "~", "!", "?", "|", "\\", "/", "=", "-", "_", ":", ";", "<", ">", "£", "€", "¥"}

	local function getRandomSymbols(count)
		local result = ""
		for i = 1, count do
			result = result .. symbols[math.random(1, #symbols)]
		end
		return result
	end

	textLabel.Text = getRandomSymbols(textLength)

	self.hackingTextConnections = self.hackingTextConnections or {}

	local shuffleConn
	shuffleConn = game:GetService("RunService").Heartbeat:Connect(function(deltaTime)
	end)
	table.insert(self.hackingTextConnections, shuffleConn)

	local revealConn
	revealConn = game:GetService("RunService").Heartbeat:Connect(function(deltaTime)
	end)
	table.insert(self.hackingTextConnections, revealConn)

	local startTime = os.clock()
	local endTime = startTime + revealTime
	local revealedChars = 0

	local function updateAnimation()
		local now = os.clock()
		local progress = math.min(1, (now - startTime) / revealTime)

		local targetRevealed = math.floor(progress * textLength)

		if targetRevealed > revealedChars then
			revealedChars = targetRevealed

			local revealedPart = string.sub(originalText, 1, revealedChars)
			local remainingLength = textLength - revealedChars
			local randomPart = getRandomSymbols(remainingLength)

			textLabel.Text = revealedPart .. randomPart
		end

		if revealedChars < textLength then
			local revealedPart = string.sub(originalText, 1, revealedChars)
			local remainingLength = textLength - revealedChars
			local randomPart = getRandomSymbols(remainingLength)
			textLabel.Text = revealedPart .. randomPart
		end

		if progress >= 1 then
			textLabel.Text = originalText
			for i, conn in ipairs(self.hackingTextConnections) do
				if conn == shuffleConn or conn == revealConn then
					conn:Disconnect()
					table.remove(self.hackingTextConnections, i)
				end
			end
			return
		end
	end

	shuffleConn:Disconnect()
	revealConn:Disconnect()

	local unifiedConn = game:GetService("RunService").Heartbeat:Connect(updateAnimation)
	table.insert(self.hackingTextConnections, unifiedConn)
end

------------------------------
-- INITIALIZATION / VALUES
------------------------------
function Ranks:init(gui)
	self.gui = gui
	self.hoverHandler = HoverHandler.new(self) 
	
	self.guiElements = {
		...
	}
	
	self.region1 = gui.Right["region_switch"]
	self.challenges = gui.Right.Container.scroll
	self.leaderboard = gui.Left.Container.scroll
	self.partyplrs = gui.Left.Party.Players
	self.region2 = gui.Left["region_switch"]
	
	self.gui.BackgroundTransparency = 1
	
	self.hoverHandler:SetupLeaderboardHover()
end

------------------------------
-- SHINE ANIMATION
------------------------------
function Ranks:shine(shineElement, duration, delay)
	local elements = {}

	if shineElement then
		elements = {
			{
				element = shineElement,
				startPos = UDim2.new(-0.5, 0, 0.5, 0),
				endPos = UDim2.new(1.5, 0, 0.5, 0),
				tweenRef = "hoverShineTween"
			}
		}
	else
		elements = {
			{
				element = self.gui.Left.Container.ShineContainer.Shine,
				startPos = UDim2.new(-0.76, 0, -0.618, 0),
				endPos = UDim2.new(1.698, 0, 1.741, 0),
				tweenRef = "leftShineTween"
			},
			{
				element = self.gui.Right.Container.ShineContainer.Shine,
				startPos = UDim2.new(-0.76, 0, -0.618, 0),
				endPos = UDim2.new(1.698, 0, 1.741, 0),
				tweenRef = "rightShineTween"
			},
			{
				element = self.gui.Right.queue.ShineContainer.Shine,
				startPos = UDim2.new(-0.596, 0, -0.241, 0),
				endPos = UDim2.new(1.5, 0, 1.2, 0),
				tweenRef = "queueBtnTween"
			},
			{
				element = self.gui.Middle.Ranks.icon.ShineContainer.Shine,
				startPos = UDim2.new(-1.02, 0, 0.991, 0),
				endPos = UDim2.new(1.937, 0, 0.387, 0),
				tweenRef = "rankIconTween"
			},
			{
				element = self.gui.Middle.ProgressBar.bar.Shine,
				startPos = UDim2.new(-0.5, 0, 0.5, 0),
				endPos = UDim2.new(1.5, 0, 0.5, 0),
				tweenRef = "barShineTween"
			},
			{
				element = self.gui.Middle["elo_rank"].ShineContainer.Shine,
				startPos = UDim2.new(-0.5, 0, 0.5, 0),
				endPos = UDim2.new(1.5, 0, 0.5, 0),
				tweenRef = "eloShineTween"
			},
			{
				element = self.gui.Middle["current_rank"].ShineContainer.Shine,
				startPos = UDim2.new(-0.5, 0, 0.5, 0),
				endPos = UDim2.new(1.5, 0, 0.5, 0),
				tweenRef = "currentShineTween"
			}
		}
	end

	for _, shineData in ipairs(elements) do
		if self[shineData.tweenRef] then
			self[shineData.tweenRef]:Cancel()
		end

		local element = shineData.element
		element.Position = shineData.startPos
		element.Visible = true

		local function playTween()
			self[shineData.tweenRef] = game:GetService("TweenService"):Create(
				element,
				TweenInfo.new(duration or 1, Enum.EasingStyle.Linear),
				{Position = shineData.endPos}
			)
			self[shineData.tweenRef]:Play()
		end

		if delay and delay > 0 then
			task.delay(delay, playTween)
		else
			playTween()
		end
	end
end


------------------------------
-- ANIMATION FUNCTIONS
------------------------------
function Ranks:resetElements()
	for _, props in pairs(self.guiElements) do
		local elem = props.element
		elem.Visible = false
		elem.Size = props.size
		elem.Position = props.pos
		elem.Rotation = props.rot
	end

	for _, entry in ipairs(self.region1:GetChildren()) do
		if entry:IsA("ImageButton") then
			entry.Visible = false
			entry.Size = UDim2.new(0, 0, 0, 0)
			entry.Position = UDim2.new(0, 0, 0, 0)
			entry.Rotation = 0
		end
	end
	
	for _, entry in ipairs(self.region2:GetChildren()) do
		if entry:IsA("ImageButton") then
			entry.Visible = false
			entry.Size = UDim2.new(0, 0, 0, 0)
			entry.Position = UDim2.new(0, 0, 0, 0)
			entry.Rotation = 0
		end
	end
	
	for _, entry in ipairs(self.challenges:GetChildren()) do
		if entry:IsA("Frame") then
			entry.frame.Visible = false
			entry.frame.Size = UDim2.new(1, 0, 1, 0)
			entry.frame.Position = UDim2.new(1.2, 0, 0.5, 0)
			entry.frame.Rotation = 0
			
			if entry.frame:FindFirstChild("claim") then
				entry.frame.claim.Visible = false
				entry.frame.claim.Size = UDim2.new(0, 0, 0, 0)
				entry.frame.claim.Position = UDim2.new(0.5, 0, 1, 0)
				entry.frame.claim.Rotation = 0
			end
			
			if entry.frame:FindFirstChild("ProgressBar") then
				entry.frame.ProgressBar.Visible = false
				entry.frame.ProgressBar.Size = UDim2.new(0, 0, 0, 0)
				entry.frame.ProgressBar.Position = UDim2.new(0.5, 0, 0.5, 0)
				entry.frame.ProgressBar.Rotation = 0
			end
			
			if entry.frame:FindFirstChild("task") then
				entry.frame.task.Visible = false
				entry.frame.task.Size = UDim2.new(0, 0, 0, 0)
				entry.frame.task.Position = UDim2.new(0.498, 0,0.5, 0)
				entry.frame.task.Rotation = 0
			end
		end
	end
	
	for _, entry in ipairs(self.leaderboard:GetChildren()) do
		if entry:IsA("Frame") then
			entry.frame.Visible = false
			entry.frame.Size = UDim2.new(1, 0, 1, 0)
			entry.frame.Position = UDim2.new(-0.2, 0,0.5, 0)
			entry.frame.Rotation = 0
			
			if entry.frame:FindFirstChild("glow") then
				entry.frame.glow.Visible = false
				entry.frame.glow.Size = UDim2.new(0, 0, 0, 0)
				entry.frame.glow.Position = UDim2.new(0.214, 0, 1.172, 0)
				entry.frame.glow.Rotation = 0
			end
			
			entry.frame["plr_icon"].Visible = false
			entry.frame["plr_icon"].Size = UDim2.new(0, 0, 0, 0)
			entry.frame["plr_icon"].Position = UDim2.new(0.37, 0,0.5, 0)
			entry.frame["plr_icon"].Rotation = 0

			if entry.frame["plr_icon"]:FindFirstChild("crown") then
				entry.frame["plr_icon"].crown.Visible = false
				entry.frame["plr_icon"].crown.Size = UDim2.new(0, 0, 0, 0)
				entry.frame["plr_icon"].crown.Position = UDim2.new(0.266, 0, 0.011, 0)
				entry.frame["plr_icon"].crown.Rotation = 15
			end
			
			entry.frame["rank_icon"].Visible = false
			entry.frame["rank_icon"].Size = UDim2.new(0, 0, 0, 0)
			entry.frame["rank_icon"].Position = UDim2.new(0.37, 0,0.5, 0)
			entry.frame["rank_icon"].Rotation = 0
			
			entry.frame.elo.Visible = false
			entry.frame.elo.Size = UDim2.new(0, 0, 0, 0)
			entry.frame.elo.Position = UDim2.new(0.5, 0, 1, 0)
			entry.frame.elo.Rotation = 0
			
			entry.frame.nbr.Visible = false
			entry.frame.nbr.Size = UDim2.new(0, 0, 0, 0)
			entry.frame.nbr.Position = UDim2.new(0, 0, 1, 0)
			entry.frame.nbr.Rotation = 0
			
			entry.frame.user.Visible = false
			entry.frame.user.Size = UDim2.new(0, 0, 0, 0)
			entry.frame.user.Position = UDim2.new(0.5, 0,0.65, 0)
			entry.frame.user.Rotation = 0
			
			if entry.frame.border:FindFirstChild("rank_back") then
				entry.frame.border["rank_back"].Visible = false
				entry.frame.border["rank_back"].Size = UDim2.new(0, 0, 0, 0)
				entry.frame.border["rank_back"].Position = UDim2.new(0.65, 0,0.5, 0)
				entry.frame.border["rank_back"].Rotation = 0
			end
			
			if entry.frame.border:FindFirstChild("glow") then
				entry.frame.border.glow.Visible = false
				entry.frame.border.glow.Size = UDim2.new(0, 0, 0, 0)
				entry.frame.border.glow.Position = UDim2.new(0.5, 0,0.9, 0)
				entry.frame.border.glow.Rotation = 0
			end
			
		end
	end
	
	for _, entry in ipairs(self.partyplrs:GetChildren()) do
		if entry:IsA("ImageLabel") or entry:IsA("ImageButton") then
			entry.Visible = false
			entry.Size = UDim2.new(0, 0, 0, 0)
			entry.Position = UDim2.new(0, 0, 0, 0)
			entry.Rotation = -20
		end
		
	end
	
	-- CHARACTER SHUFFLE
	if self.hackingTextConnections then
		for _, conn in ipairs(self.hackingTextConnections) do
			conn:Disconnect()
		end
		self.hackingTextConnections = nil
	end
	
	-- SHINE
	local elements = {
		{element = self.gui.Left.Container.ShineContainer.Shine, pos = UDim2.new(-0.76, 0, -0.618, 0)},
		{element = self.gui.Right.Container.ShineContainer.Shine, pos = UDim2.new(-0.76, 0, -0.618, 0)},
		{element = self.gui.Right.queue.ShineContainer.Shine, pos = UDim2.new(-0.596, 0, -0.241, 0)},
		{element = self.gui.Middle.Ranks.icon.ShineContainer.Shine, pos = UDim2.new(-1.02, 0, 0.991, 0)},
		{element = self.gui.Middle.ProgressBar.bar.Shine, pos = UDim2.new(-0.5, 0, 0.5, 0)},
		{element = self.gui.Middle["elo_rank"].ShineContainer.Shine, pos = UDim2.new(-0.5, 0, 0.5, 0)},
		{element = self.gui.Middle["current_rank"].ShineContainer.Shine, pos = UDim2.new(-0.5, 0, 0.5, 0)}
	}
	local tweenRefs = {
		"leftShineTween", "rightShineTween", "queueBtnTween",
		"rankIconTween", "barShineTween", "eloShineTween",
		"currentShineTween", "hoverShineTween"
	}
	for _, ref in ipairs(tweenRefs) do
		if self[ref] then
			self[ref]:Cancel()
			self[ref] = nil
		end
	end
	for _, shineData in ipairs(elements) do
		shineData.element.Position = shineData.pos
		shineData.element.Visible = false
	end
	
	-- BACKGROUND
	self.gui.BackgroundTransparency = 1
end

function Ranks:playInitialAnimation()
	...
end

function Ranks:playCloseAnimation()
	...
return Ranks
```