game:GetService("StarterGui"):SetCoreGuiEnabled(Enum.CoreGuiType.PlayerList,false) local c=Instance.new("ScreenGui") local k=Instance.new("Frame") local _=Instance.new("UIGridLayout") local e=Instance.new("Frame") local d=Instance.new("ImageLabel") local b=Instance.new("UICorner") local m=Instance.new("TextLabel") local l=Instance.new("TextLabel") local g=Instance.new("TextButton") local i=false local a=false c.Name="Aggui111" c.Parent=game.Players.LocalPlayer:WaitForChild("PlayerGui") c.ZIndexBehavior=Enum.ZIndexBehavior.Sibling k.Name="MainFrame" k.Parent=c k.BackgroundColor3=Color3.fromRGB(255,255,255) k.BackgroundTransparency=1.000 k.Position=UDim2.new(0.0249278136,0,0.0342246294,0) k.Size=UDim2.new(0.949622154,0,0.111229949,0) _.Parent=k _.SortOrder=Enum.SortOrder.LayoutOrder _.CellSize=UDim2.new(0,222,0,100) e.Name="Template" e.Parent=k e.BackgroundColor3=Color3.fromRGB(0,0,0) e.BackgroundTransparency=0.350 e.BorderSizePixel=0 e.Size=UDim2.new(0.19628647,0,0.961538434,0) e.Visible=false d.Name="Avatar" d.Parent=e d.BackgroundColor3=Color3.fromRGB(149,149,149) d.BackgroundTransparency=0.200 d.Size=UDim2.new(0.45045045,0,1,0) d.Image="rbxasset://textures/ui/GuiImagePlaceholder.png" d.Visible=false b.CornerRadius=UDim.new(1,1) b.Name="AvatarCorner" b.Parent=d m.Name="NrmalName" m.Parent=e m.BackgroundColor3=Color3.fromRGB(255,255,255) m.BackgroundTransparency=1.000 m.Position=UDim2.new(0.45045045,0,0,0) m.Size=UDim2.new(0.54954952,0,0.479999989,0) m.Font=Enum.Font.FredokaOne m.Text="Roblox_Wmh" m.TextColor3=Color3.fromRGB(255,255,255) m.TextScaled=true m.TextSize=14.000 m.TextWrapped=true m.Visible=false l.Name="Displayname" l.Parent=e l.BackgroundColor3=Color3.fromRGB(255,255,255) l.BackgroundTransparency=1.000 l.Position=UDim2.new(0.45045045,0,0.479999989,0) l.Size=UDim2.new(0.54954952,0,0.219999999,0) l.Font=Enum.Font.FredokaOne l.Text="@Roblox_Wmh" l.TextColor3=Color3.fromRGB(255,255,255) l.TextScaled=true l.TextSize=14.000 l.TextWrapped=true l.Visible=false g.Name="Greetings" g.Parent=e g.BackgroundColor3=Color3.fromRGB(149,149,149) g.BackgroundTransparency=0.700 g.Position=UDim2.new(0.45045045,0,0.769999981,0) g.Size=UDim2.new(0.54954952,0,0.230000004,0) g.Font=Enum.Font.FredokaOne g.Text="Greetings" g.TextColor3=Color3.fromRGB(170,255,255) g.TextScaled=true g.TextSize=14.000 g.TextWrapped=true g.Visible=false for _,h in pairs(game.Players:GetChildren())do local j=e:Clone() local g=g:Clone() local f=d:Clone() local b=b:Clone() local e=m:Clone() local d=l:Clone() j.Parent=k j.Visible=true j.Name=h.Name g.Parent=j g.Visible=true f.Visible=true f.Parent=j local c=h.UserId local a=Enum.ThumbnailType.HeadShot local _=Enum.ThumbnailSize.Size420x420 local a,_=game.Players:GetUserThumbnailAsync(c,a,_) f.Image=a b.Parent=f e.Text=h.DisplayName e.Parent=j e.Visible=true d.Visible=true d.Parent=j d.Text="@"..h.Name g.MouseButton1Click:Connect(function()if i==false then i=true local a="Hi, "..g.Parent.Name.."!" local _="All" local b=game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest b:FireServer(a,_) wait(2) i=false end end)end game.Players.PlayerAdded:Connect(function(f)local j=e:Clone() local h=g:Clone() local g=d:Clone() local c=b:Clone() local e=m:Clone() local d=l:Clone() j.Parent=k j.Visible=true j.Name=f.Name h.Parent=j h.Visible=true g.Visible=true g.Parent=j local b=f.UserId local a=Enum.ThumbnailType.HeadShot local _=Enum.ThumbnailSize.Size420x420 local a,_=game.Players:GetUserThumbnailAsync(b,a,_) g.Image=a c.Parent=g e.Text=f.DisplayName e.Parent=j e.Visible=true d.Visible=true d.Parent=j d.Text="@"..f.Name h.MouseButton1Click:Connect(function()if i==false then i=true local b="Hi, "..h.Parent.Name.."!" local a="All" local _=game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest _:FireServer(b,a) wait(2) i=false end end)end) game.Players.PlayerRemoving:Connect(function(a)for _,_ in pairs(k:GetChildren())do if _ and _.Name==a.Name then _:Remove() print(a.Name)end end end) game.Players.LocalPlayer.Chatted:Connect(function(_)if _=="/Destroy"then c:Destroy()end end) game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(_)if _=="x"then if a==false then a=true k.Visible=false else if a==true then a=false k.Visible=true end end end end) while wait(2)do game.Players.LocalPlayer.Character.Humanoid.Died:Connect(function()local b=Instance.new("ScreenGui") local k=Instance.new("Frame") local _=Instance.new("UIGridLayout") local e=Instance.new("Frame") local d=Instance.new("ImageLabel") local c=Instance.new("UICorner") local m=Instance.new("TextLabel") local l=Instance.new("TextLabel") local h=Instance.new("TextButton") local i=false local a=false b.Name="Aggui111" b.Parent=game.Players.LocalPlayer:WaitForChild("PlayerGui") b.ZIndexBehavior=Enum.ZIndexBehavior.Sibling k.Name="MainFrame" k.Parent=b k.BackgroundColor3=Color3.fromRGB(255,255,255) k.BackgroundTransparency=1.000 k.Position=UDim2.new(0.0249278136,0,0.0342246294,0) k.Size=UDim2.new(0.949622154,0,0.111229949,0) _.Parent=k _.SortOrder=Enum.SortOrder.LayoutOrder _.CellSize=UDim2.new(0,222,0,100) e.Name="Template" e.Parent=k e.BackgroundColor3=Color3.fromRGB(0,0,0) e.BackgroundTransparency=0.350 e.BorderSizePixel=0 e.Size=UDim2.new(0.19628647,0,0.961538434,0) e.Visible=false d.Name="Avatar" d.Parent=e d.BackgroundColor3=Color3.fromRGB(149,149,149) d.BackgroundTransparency=0.200 d.Size=UDim2.new(0.45045045,0,1,0) d.Image="rbxasset://textures/ui/GuiImagePlaceholder.png" d.Visible=false c.CornerRadius=UDim.new(1,1) c.Name="AvatarCorner" c.Parent=d m.Name="NrmalName" m.Parent=e m.BackgroundColor3=Color3.fromRGB(255,255,255) m.BackgroundTransparency=1.000 m.Position=UDim2.new(0.45045045,0,0,0) m.Size=UDim2.new(0.54954952,0,0.479999989,0) m.Font=Enum.Font.FredokaOne m.Text="Roblox_Wmh" m.TextColor3=Color3.fromRGB(255,255,255) m.TextScaled=true m.TextSize=14.000 m.TextWrapped=true m.Visible=false l.Name="Displayname" l.Parent=e l.BackgroundColor3=Color3.fromRGB(255,255,255) l.BackgroundTransparency=1.000 l.Position=UDim2.new(0.45045045,0,0.479999989,0) l.Size=UDim2.new(0.54954952,0,0.219999999,0) l.Font=Enum.Font.FredokaOne l.Text="@Roblox_Wmh" l.TextColor3=Color3.fromRGB(255,255,255) l.TextScaled=true l.TextSize=14.000 l.TextWrapped=true l.Visible=false h.Name="Greetings" h.Parent=e h.BackgroundColor3=Color3.fromRGB(149,149,149) h.BackgroundTransparency=0.700 h.Position=UDim2.new(0.45045045,0,0.769999981,0) h.Size=UDim2.new(0.54954952,0,0.230000004,0) h.Font=Enum.Font.FredokaOne h.Text="Greetings" h.TextColor3=Color3.fromRGB(170,255,255) h.TextScaled=true h.TextSize=14.000 h.TextWrapped=true h.Visible=false for _,g in pairs(game.Players:GetChildren())do local j=e:Clone() local h=h:Clone() local f=d:Clone() local a=c:Clone() local e=m:Clone() local d=l:Clone() j.Parent=k j.Visible=true j.Name=g.Name h.Parent=j h.Visible=true f.Visible=true f.Parent=j local _=g.UserId local b=Enum.ThumbnailType.HeadShot local c=Enum.ThumbnailSize.Size420x420 local b,_=game.Players:GetUserThumbnailAsync(_,b,c) f.Image=b a.Parent=f e.Text=g.DisplayName e.Parent=j e.Visible=true d.Visible=true d.Parent=j d.Text="@"..g.Name h.MouseButton1Click:Connect(function()if i==false then i=true local _="Hi, "..h.Parent.Name.."!" local a="All" local b=game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest b:FireServer(_,a) wait(2) i=false end end)end game.Players.PlayerAdded:Connect(function(f)local j=e:Clone() local h=h:Clone() local g=d:Clone() local b=c:Clone() local d=m:Clone() local e=l:Clone() j.Parent=k j.Visible=true j.Name=f.Name h.Parent=j h.Visible=true g.Visible=true g.Parent=j local c=f.UserId local a=Enum.ThumbnailType.HeadShot local _=Enum.ThumbnailSize.Size420x420 local a,_=game.Players:GetUserThumbnailAsync(c,a,_) g.Image=a b.Parent=g d.Text=f.DisplayName d.Parent=j d.Visible=true e.Visible=true e.Parent=j e.Text="@"..f.Name h.MouseButton1Click:Connect(function()if i==false then i=true local _="Hi, "..h.Parent.Name.."!" local b="All" local a=game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest a:FireServer(_,b) wait(2) i=false end end)end) game.Players.PlayerRemoving:Connect(function(a)for _,_ in pairs(k:GetChildren())do if _ and _.Name==a.Name then _:Remove() print(a.Name)end end end) game.Players.LocalPlayer.Chatted:Connect(function(_)if _=="/Destroy"then b:Destroy()end end) game.Players.LocalPlayer:GetMouse().KeyDown:Connect(function(_)if _=="x"then if a==false then a=true k.Visible=false else if a==true then a=false k.Visible=true end end end end)end)end
