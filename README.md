local FakePlayer = "GodY66TH".."Rocket0"
local Type = "Player" -- Base, Player, Crash
local Player = "GodY66TH" -- Player Actual Name
local TeamColor = "Echo" -- Team Name (Full and Correct)
local AttackMode = "AttackCount" -- AttackCount, Instant
local AttackCount = 10

if game:GetService("Players").LocalPlayer.Character and game:GetService("Players").LocalPlayer.Character:FindFirstChild("RPG") then else print("Executed") return end
if Type == "Base" then
	if AttackMode == "AttackCount" then
		if workspace.Tycoon.Tycoons:FindFirstChild(TeamColor) and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield") and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield") and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield"):FindFirstChild("Shield1") then
			for i = 1,AttackCount do
				local HitObject = workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield"):FindFirstChild("Shield1")
				game:GetService("ReplicatedStorage").RocketSystem.RocketHit:FireServer(HitObject.Position + Vector3.new(0,-3000,0),Vector3.new(0,0,-1),game:GetService("Players").LocalPlayer.Character.RPG,game:GetService("Players").LocalPlayer.Character.RPG,HitObject,nil,FakePlayer)
			end
		end
	elseif AttackMode == "Instant" then
		if workspace.Tycoon.Tycoons:FindFirstChild(TeamColor) and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield") and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield") and workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield"):FindFirstChild("Shield1") then
			for i = 1,100 do
			local HitObject = workspace.Tycoon.Tycoons:FindFirstChild(TeamColor).PurchasedObjects:FindFirstChild("Base Shield"):FindFirstChild("Shield"):FindFirstChild("Shield1")
			game:GetService("ReplicatedStorage").RocketSystem.RocketHit:FireServer(HitObject.Position + Vector3.new(0,-3000,0),Vector3.new(0,0,-1),game:GetService("Players").LocalPlayer.Character.RPG,game:GetService("Players").LocalPlayer.Character.RPG,HitObject,nil,FakePlayer)
			end
		end
	end
elseif Type == "Player" then
	if AttackMode == "AttackCount" then
		if game:GetService("Players"):FindFirstChild(Player) and game:GetService("Players"):FindFirstChild(Player).Character then
			for i = 1,AttackCount do
				local HitObject = game:GetService("Players"):FindFirstChild(Player).Character.Head
				game:GetService("ReplicatedStorage").RocketSystem.RocketHit:FireServer(HitObject.Position + Vector3.new(0,-3000,0),Vector3.new(0,0,-1),game:GetService("Players").LocalPlayer.Character.RPG,game:GetService("Players").LocalPlayer.Character.RPG,HitObject,nil,FakePlayer)
			end
		end
	elseif AttackMode == "Instant" then
		if if game:GetService("Players"):FindFirstChild(Player) and game:GetService("Players"):FindFirstChild(Player).Character then
			local HitObject = game:GetService("Players"):FindFirstChild(Player).Character.Head
			for i = 1,100 do
				game:GetService("ReplicatedStorage").RocketSystem.RocketHit:FireServer(HitObject.Position + Vector3.new(0,-3000,0),Vector3.new(0,0,-1),game:GetService("Players").LocalPlayer.Character.RPG,game:GetService("Players").LocalPlayer.Character.RPG,HitObject,nil,FakePlayer)
			end
		end
	end
elseif Type == "Crash" then
	if game:GetService("Players"):FindFirstChild(Player) and game:GetService("Players"):FindFirstChild(Player).Character then
		local HitObject = game:GetService("Players"):FindFirstChild(Player).Character:FindFirstChild("Head")
		if HitObject then
			for i = 1,250 do
				game:GetService("ReplicatedStorage").RocketSystem.RocketHit:FireServer(HitObject.Position + Vector3.new(0,-3000,0),Vector3.new(0,0,-1),game:GetService("Players").LocalPlayer.Character.RPG,game:GetService("Players").LocalPlayer.Character.RPG,nil,nil,FakePlayer)
			end
		end
	end
end
