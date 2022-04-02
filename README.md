-- Gui to Lua
-- Version: 3.2

-- Instances:
game:GetService("StarterGui"):SetCoreGuiEnabled(Enum.CoreGuiType.PlayerList, false)

local PlayerList = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local UIGridLayout = Instance.new("UIGridLayout")
local Template = Instance.new("Frame")
local Avatar = Instance.new("ImageLabel")
local AvatarCorner = Instance.new("UICorner")
local NrmalName = Instance.new("TextLabel")
local Displayname = Instance.new("TextLabel")
local Greetings = Instance.new("TextButton")
local Ready = false
local Ready1 = false

--Properties:

PlayerList.Name = "Aggui111"
PlayerList.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
PlayerList.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

MainFrame.Name = "MainFrame"
MainFrame.Parent = PlayerList
MainFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
MainFrame.BackgroundTransparency = 1.000
MainFrame.Position = UDim2.new(0.0249278136, 0, 0.0342246294, 0)
MainFrame.Size = UDim2.new(0.949622154, 0, 0.111229949, 0)

UIGridLayout.Parent = MainFrame
UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIGridLayout.CellSize = UDim2.new(0, 222, 0, 100)

Template.Name = "Template"
Template.Parent = MainFrame
Template.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Template.BackgroundTransparency = 0.350
Template.BorderSizePixel = 0
Template.Size = UDim2.new(0.19628647, 0, 0.961538434, 0)
Template.Visible = false

Avatar.Name = "Avatar"
Avatar.Parent = Template
Avatar.BackgroundColor3 = Color3.fromRGB(149, 149, 149)
Avatar.BackgroundTransparency = 0.200
Avatar.Size = UDim2.new(0.45045045, 0, 1, 0)
Avatar.Image = "rbxasset://textures/ui/GuiImagePlaceholder.png"
Avatar.Visible = false

AvatarCorner.CornerRadius = UDim.new(1, 1)
AvatarCorner.Name = "AvatarCorner"
AvatarCorner.Parent = Avatar

NrmalName.Name = "NrmalName"
NrmalName.Parent = Template
NrmalName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
NrmalName.BackgroundTransparency = 1.000
NrmalName.Position = UDim2.new(0.45045045, 0, 0, 0)
NrmalName.Size = UDim2.new(0.54954952, 0, 0.479999989, 0)
NrmalName.Font = Enum.Font.FredokaOne
NrmalName.Text = "Roblox_Wmh"
NrmalName.TextColor3 = Color3.fromRGB(255, 255, 255)
NrmalName.TextScaled = true
NrmalName.TextSize = 14.000
NrmalName.TextWrapped = true
NrmalName.Visible = false

Displayname.Name = "Displayname"
Displayname.Parent = Template
Displayname.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Displayname.BackgroundTransparency = 1.000
Displayname.Position = UDim2.new(0.45045045, 0, 0.479999989, 0)
Displayname.Size = UDim2.new(0.54954952, 0, 0.219999999, 0)
Displayname.Font = Enum.Font.FredokaOne
Displayname.Text = "@Roblox_Wmh"
Displayname.TextColor3 = Color3.fromRGB(255, 255, 255)
Displayname.TextScaled = true
Displayname.TextSize = 14.000
Displayname.TextWrapped = true
Displayname.Visible = false

Greetings.Name = "Greetings"
Greetings.Parent = Template
Greetings.BackgroundColor3 = Color3.fromRGB(149, 149, 149)
Greetings.BackgroundTransparency = 0.700
Greetings.Position = UDim2.new(0.45045045, 0, 0.769999981, 0)
Greetings.Size = UDim2.new(0.54954952, 0, 0.230000004, 0)
Greetings.Font = Enum.Font.FredokaOne
Greetings.Text = "Greetings"
Greetings.TextColor3 = Color3.fromRGB(170, 255, 255)
Greetings.TextScaled = true
Greetings.TextSize = 14.000
Greetings.TextWrapped = true
Greetings.Visible = false


for i,Player in pairs(game.Players:GetChildren()) do
	local A = Template:Clone()
	local B = Greetings:Clone()
	local C = Avatar:Clone()
	local D = AvatarCorner:Clone()
	local E = NrmalName:Clone()
	local F = Displayname:Clone()
	A.Parent = MainFrame
	A.Visible = true
	A.Name = Player.Name
	B.Parent = A
	B.Visible = true
	C.Visible = true
	C.Parent = A
	local userId = Player.UserId
	local thumbtype = Enum.ThumbnailType.HeadShot
	local thumbsize = Enum.ThumbnailSize.Size420x420
	local content,isReady = game.Players:GetUserThumbnailAsync(userId,thumbtype,thumbsize)
	C.Image = content
	D.Parent = C
	E.Text = Player.DisplayName
	E.Parent = A
	E.Visible = true
	F.Visible = true
	F.Parent = A
	F.Text = "@" .. Player.Name
	B.MouseButton1Click:Connect(function()
		if Ready == false then
			Ready = true
			local A_1 = "Hi, " .. B.Parent.Name .. "!"
			local A_2 = "All"
			local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
			Event:FireServer(A_1, A_2)
			wait(2)
			Ready = false
		end
	end)
end

game.Players.PlayerAdded:Connect(function(Player)
	local A = Template:Clone()
	local B = Greetings:Clone()
	local C = Avatar:Clone()
	local D = AvatarCorner:Clone()
	local E = NrmalName:Clone()
	local F = Displayname:Clone()
	A.Parent = MainFrame
	A.Visible = true
	A.Name = Player.Name
	B.Parent = A
	B.Visible = true
	C.Visible = true
	C.Parent = A
	local userId = Player.UserId
	local thumbtype = Enum.ThumbnailType.HeadShot
	local thumbsize = Enum.ThumbnailSize.Size420x420
	local content,isReady = game.Players:GetUserThumbnailAsync(userId,thumbtype,thumbsize)
	C.Image = content
	D.Parent = C
	E.Text = Player.DisplayName
	E.Parent = A
	E.Visible = true
	F.Visible = true
	F.Parent = A
	F.Text = "@" .. Player.Name
	B.MouseButton1Click:Connect(function()
		if Ready == false then
			Ready = true
			local A_1 = "Hi, " .. B.Parent.Name .. "!"
			local A_2 = "All"
			local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
			Event:FireServer(A_1, A_2)
			wait(2)
			Ready = false
		end
	end)
end)

game.Players.PlayerRemoving:Connect(function(Player)
	for i,v in pairs(MainFrame:GetChildren()) do
		if v and v.Name == Player.Name then
			v:Remove()
			print(Player.Name)
		end
	end
end)

game.Players.LocalPlayer.Chatted:Connect(function(Msg)
	if Msg == "/Destroy" then
		PlayerList:Destroy()
	end
end)

game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(Key)
	if Key == "x" then
		if Ready1 == false then
			Ready1 = true
			MainFrame.Visible = false
		else
			if Ready1 == true then
				Ready1 = false
				MainFrame.Visible = true
			end
		end
	end
end)

while wait(2) do
	if game.Players.LocalPlayer.PlayerGui:FindFirstChild("Aggui111") then
	else
		-- Gui to Lua
		-- Version: 3.2

		-- Instances:

		local PlayerList = Instance.new("ScreenGui")
		local MainFrame = Instance.new("Frame")
		local UIGridLayout = Instance.new("UIGridLayout")
		local Template = Instance.new("Frame")
		local Avatar = Instance.new("ImageLabel")
		local AvatarCorner = Instance.new("UICorner")
		local NrmalName = Instance.new("TextLabel")
		local Displayname = Instance.new("TextLabel")
		local Greetings = Instance.new("TextButton")
		local Ready = false
		local Ready1 = false

		--Properties:

		PlayerList.Name = "Aggui111"
		PlayerList.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
		PlayerList.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

		MainFrame.Name = "MainFrame"
		MainFrame.Parent = PlayerList
		MainFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		MainFrame.BackgroundTransparency = 1.000
		MainFrame.Position = UDim2.new(0.0249278136, 0, 0.0342246294, 0)
		MainFrame.Size = UDim2.new(0.949622154, 0, 0.111229949, 0)

		UIGridLayout.Parent = MainFrame
		UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
		UIGridLayout.CellSize = UDim2.new(0, 222, 0, 100)

		Template.Name = "Template"
		Template.Parent = MainFrame
		Template.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Template.BackgroundTransparency = 0.350
		Template.BorderSizePixel = 0
		Template.Size = UDim2.new(0.19628647, 0, 0.961538434, 0)
		Template.Visible = false

		Avatar.Name = "Avatar"
		Avatar.Parent = Template
		Avatar.BackgroundColor3 = Color3.fromRGB(149, 149, 149)
		Avatar.BackgroundTransparency = 0.200
		Avatar.Size = UDim2.new(0.45045045, 0, 1, 0)
		Avatar.Image = "rbxasset://textures/ui/GuiImagePlaceholder.png"
		Avatar.Visible = false

		AvatarCorner.CornerRadius = UDim.new(1, 1)
		AvatarCorner.Name = "AvatarCorner"
		AvatarCorner.Parent = Avatar

		NrmalName.Name = "NrmalName"
		NrmalName.Parent = Template
		NrmalName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		NrmalName.BackgroundTransparency = 1.000
		NrmalName.Position = UDim2.new(0.45045045, 0, 0, 0)
		NrmalName.Size = UDim2.new(0.54954952, 0, 0.479999989, 0)
		NrmalName.Font = Enum.Font.FredokaOne
		NrmalName.Text = "Roblox_Wmh"
		NrmalName.TextColor3 = Color3.fromRGB(255, 255, 255)
		NrmalName.TextScaled = true
		NrmalName.TextSize = 14.000
		NrmalName.TextWrapped = true
		NrmalName.Visible = false

		Displayname.Name = "Displayname"
		Displayname.Parent = Template
		Displayname.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Displayname.BackgroundTransparency = 1.000
		Displayname.Position = UDim2.new(0.45045045, 0, 0.479999989, 0)
		Displayname.Size = UDim2.new(0.54954952, 0, 0.219999999, 0)
		Displayname.Font = Enum.Font.FredokaOne
		Displayname.Text = "@Roblox_Wmh"
		Displayname.TextColor3 = Color3.fromRGB(255, 255, 255)
		Displayname.TextScaled = true
		Displayname.TextSize = 14.000
		Displayname.TextWrapped = true
		Displayname.Visible = false

		Greetings.Name = "Greetings"
		Greetings.Parent = Template
		Greetings.BackgroundColor3 = Color3.fromRGB(149, 149, 149)
		Greetings.BackgroundTransparency = 0.700
		Greetings.Position = UDim2.new(0.45045045, 0, 0.769999981, 0)
		Greetings.Size = UDim2.new(0.54954952, 0, 0.230000004, 0)
		Greetings.Font = Enum.Font.FredokaOne
		Greetings.Text = "Greetings"
		Greetings.TextColor3 = Color3.fromRGB(170, 255, 255)
		Greetings.TextScaled = true
		Greetings.TextSize = 14.000
		Greetings.TextWrapped = true
		Greetings.Visible = false


		for i,Player in pairs(game.Players:GetChildren()) do
			local A = Template:Clone()
			local B = Greetings:Clone()
			local C = Avatar:Clone()
			local D = AvatarCorner:Clone()
			local E = NrmalName:Clone()
			local F = Displayname:Clone()
			A.Parent = MainFrame
			A.Visible = true
			A.Name = Player.Name
			B.Parent = A
			B.Visible = true
			C.Visible = true
			C.Parent = A
			local userId = Player.UserId
			local thumbtype = Enum.ThumbnailType.HeadShot
			local thumbsize = Enum.ThumbnailSize.Size420x420
			local content,isReady = game.Players:GetUserThumbnailAsync(userId,thumbtype,thumbsize)
			C.Image = content
			D.Parent = C
			E.Text = Player.DisplayName
			E.Parent = A
			E.Visible = true
			F.Visible = true
			F.Parent = A
			F.Text = "@" .. Player.Name
			B.MouseButton1Click:Connect(function()
				if Ready == false then
					Ready = true
					local A_1 = "Hi, " .. B.Parent.Name .. "!"
					local A_2 = "All"
					local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
					Event:FireServer(A_1, A_2)
					wait(2)
					Ready = false
				end
			end)
		end

		game.Players.PlayerAdded:Connect(function(Player)
			local A = Template:Clone()
			local B = Greetings:Clone()
			local C = Avatar:Clone()
			local D = AvatarCorner:Clone()
			local E = NrmalName:Clone()
			local F = Displayname:Clone()
			A.Parent = MainFrame
			A.Visible = true
			A.Name = Player.Name
			B.Parent = A
			B.Visible = true
			C.Visible = true
			C.Parent = A
			local userId = Player.UserId
			local thumbtype = Enum.ThumbnailType.HeadShot
			local thumbsize = Enum.ThumbnailSize.Size420x420
			local content,isReady = game.Players:GetUserThumbnailAsync(userId,thumbtype,thumbsize)
			C.Image = content
			D.Parent = C
			E.Text = Player.DisplayName
			E.Parent = A
			E.Visible = true
			F.Visible = true
			F.Parent = A
			F.Text = "@" .. Player.Name
			B.MouseButton1Click:Connect(function()
				if Ready == false then
					Ready = true
					local A_1 = "Hi, " .. B.Parent.Name .. "!"
					local A_2 = "All"
					local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest
					Event:FireServer(A_1, A_2)
					wait(2)
					Ready = false
				end
			end)
		end)

		game.Players.PlayerRemoving:Connect(function(Player)
			for i,v in pairs(MainFrame:GetChildren()) do
				if v and v.Name == Player.Name then
					v:Remove()
					print(Player.Name)
				end
			end
		end)

		game.Players.LocalPlayer.Chatted:Connect(function(Msg)
			if Msg == "/Destroy" then
				PlayerList:Destroy()
			end
		end)

		game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(Key)
			if Key == "x" then
				if Ready1 == false then
					Ready1 = true
					MainFrame.Visible = false
				else
					if Ready1 == true then
						Ready1 = false
						MainFrame.Visible = true
					end
				end
			end
		end)
	end
end
