Ok perfect, what I wanted is in a local script placed in Container, when you click self.animationModule.gui.Left["region_switch"].switch, it will play this animation :
local sortedChildren = {}
	for _, entry in ipairs(self.leaderboard:GetChildren()) do
		if entry:IsA("Frame") then
			table.insert(sortedChildren, entry)
		end
	end
	table.sort(sortedChildren, function(a, b) return a.LayoutOrder < b.LayoutOrder end)

	for index, entry in ipairs(sortedChildren) do
		if index == 1 then
			task.spawn(function()
				entry.frame.Visible = true
				spr.target(entry.frame, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.5, 0), Size = UDim2.new(1, 0, 1, 0), Rotation = 0})

				task.spawn(function()
					task.wait(0.2)

					entry.frame["plr_icon"].Visible = true
					entry.frame["rank_icon"].Visible = true
					entry.frame.elo.Visible = true
					entry.frame.nbr.Visible = true
					entry.frame.user.Visible = true

					spr.target(entry.frame["plr_icon"], 0.6, 1.9, {Position = UDim2.new(0.26, 0, 0.5, 0), Size = UDim2.new(0.138, 0, 0.734, 0), Rotation = 0})
					spr.target(entry.frame["rank_icon"], 0.6, 1.9, {Position = UDim2.new(0.855, 0, 0.5, 0), Size = UDim2.new(0.152, 0, 0.766, 0), Rotation = 0})
					spr.target(entry.frame.elo, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.68, 0), Size = UDim2.new(0.36, 0, 0.407, 0), Rotation = 0})
					spr.target(entry.frame.nbr, 0.6, 1.9, {Position = UDim2.new(0.105, 0, 0.5, 0), Size = UDim2.new(0.12, 0, 0.516, 0), Rotation = 0})
					spr.target(entry.frame.user, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.3, 0), Size = UDim2.new(0.321, 0, 0.326, 0), Rotation = 0})
					
					self:hackingTextEffect(entry.frame.nbr, 0.45)
					self:hackingTextEffect(entry.frame.user, 0.7)
					self:hackingTextEffect(entry.frame.elo, 0.6)

					if entry.frame["plr_icon"]:FindFirstChild("crown") then
						entry.frame["plr_icon"].crown.Visible = true
						spr.target(entry.frame["plr_icon"].crown, 0.6, 1.9, {Position = UDim2.new(0.266, 0, 0.011, 0), Size = UDim2.new(1.426, 0, 1.234, 0), Rotation = 0})
					end
					if entry.frame:FindFirstChild("glow") then
						entry.frame.glow.Visible = true
						spr.target(entry.frame.glow, 0.6, 1.9, {Position = UDim2.new(0.09, 0, 0.5, 0), Size = UDim2.new(0.214, 0, 1.172, 0), Rotation = 0})
					end
					if entry.frame.border:FindFirstChild("rank_back") then
						entry.frame.border["rank_back"].Visible = true
						spr.target(entry.frame.border["rank_back"], 0.6, 1.9, {Position = UDim2.new(0.855, 0, 0.5, 0), Size = UDim2.new(0.387, 0, 2.016, 0), Rotation = 0})
					end
					if entry.frame.border:FindFirstChild("glow") then
						entry.frame.border.glow.Visible = true
						spr.target(entry.frame.border.glow, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.647, 0), Size = UDim2.new(1, 0, 1.016, 0), Rotation = 0})
					end
				end)
			end)
		else
			local delayTime = 0.1 + (index - 2) * 0.12
			task.delay(delayTime, function()
				entry.frame.Visible = true
				spr.target(entry.frame, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.5, 0), Size = UDim2.new(1, 0, 1, 0), Rotation = 0})

				task.spawn(function()
					task.wait(0.2)

					entry.frame["plr_icon"].Visible = true
					entry.frame["rank_icon"].Visible = true
					entry.frame.elo.Visible = true
					entry.frame.nbr.Visible = true
					entry.frame.user.Visible = true

					spr.target(entry.frame["plr_icon"], 0.6, 1.9, {Position = UDim2.new(0.26, 0, 0.5, 0), Size = UDim2.new(0.138, 0, 0.734, 0), Rotation = 0})
					spr.target(entry.frame["rank_icon"], 0.6, 1.9, {Position = UDim2.new(0.855, 0, 0.5, 0), Size = UDim2.new(0.152, 0, 0.766, 0), Rotation = 0})
					spr.target(entry.frame.elo, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.68, 0), Size = UDim2.new(0.36, 0, 0.407, 0), Rotation = 0})
					spr.target(entry.frame.nbr, 0.6, 1.9, {Position = UDim2.new(0.105, 0, 0.5, 0), Size = UDim2.new(0.12, 0, 0.516, 0), Rotation = 0})
					spr.target(entry.frame.user, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.3, 0), Size = UDim2.new(0.321, 0, 0.326, 0), Rotation = 0})
					
					self:hackingTextEffect(entry.frame.nbr, 0.45)
					self:hackingTextEffect(entry.frame.user, 0.7)
					self:hackingTextEffect(entry.frame.elo, 0.6)

					if entry.frame["plr_icon"]:FindFirstChild("crown") then
						entry.frame["plr_icon"].crown.Visible = true
						spr.target(entry.frame["plr_icon"].crown, 0.6, 1.9, {Position = UDim2.new(0.266, 0, 0.011, 0), Size = UDim2.new(1.426, 0, 1.234, 0), Rotation = 0})
					end
					if entry.frame:FindFirstChild("glow") then
						entry.frame.glow.Visible = true
						spr.target(entry.frame.glow, 0.6, 1.9, {Position = UDim2.new(0.09, 0, 0.5, 0), Size = UDim2.new(0.214, 0, 1.172, 0), Rotation = 0})
					end
					if entry.frame.border:FindFirstChild("rank_back") then
						entry.frame.border["rank_back"].Visible = true
						spr.target(entry.frame.border["rank_back"], 0.6, 1.9, {Position = UDim2.new(0.855, 0, 0.5, 0), Size = UDim2.new(0.387, 0, 2.016, 0), Rotation = 0})
					end
					if entry.frame.border:FindFirstChild("glow") then
						entry.frame.border.glow.Visible = true
						spr.target(entry.frame.border.glow, 0.6, 1.9, {Position = UDim2.new(0.5, 0, 0.647, 0), Size = UDim2.new(1, 0, 1.016, 0), Rotation = 0})
					end
				end)
			end)
		end
	end

and the shine animation for the self.gui.Right.Container.ShineContainer.Shine only. Make sure to handle fast clicks and don't forget to require the Ranks module since some functions are from there if it's possible