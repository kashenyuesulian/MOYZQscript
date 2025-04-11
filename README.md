local OrionLib = loadstring(game:HttpGet("https://example.com/script.lua"))()
local LBLG = Instance.new("ScreenGui", getParent)
local LBL = Instance.new("TextLabel", getParent)
local player = game.Players.LocalPlayer
LBLG.Name = "LBLG"
LBLG.Parent = game.CoreGuiL
BLG.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
LBLG.Enabled = true
LBL.Name = "LBL"
LBL.Parent = LBLG
LBL.BackgroundColor3 = Color3.new(1, 1, 1)
LBL.BackgroundTransparency = 1
LBL.BorderColor3 = Color3.new(0, 0, 0)
LBL.Position = UDim2.new(0.75,0,0.010,0)
LBL.Size = UDim2.new(0, 133, 0, 30)
LBL.Font = Enum.Font.GothamSemibold
LBL.Text = "TextLabel"
LBL.TextColor3 = Color3.new(1, 1, 1)
LBL.TextScaled = true
LBL.TextSize = 14
LBL.TextWrapped = true
LBL.Visible = true
local FpsLabel = LBL
local Heartbeat = game:GetService("RunService").Heartbeat
local LastIteration, Start
local FrameUpdateTable = { }
local function HeartbeatUpdate()
	LastIteration = tick()
	for Index = #FrameUpdateTable, 1, -1 do
		FrameUpdateTable[Index + 1] = (FrameUpdateTable[Index] >= LastIteration - 1) and FrameUpdateTable[Index] or nil
	end
 FrameUpdateTable[1] = LastIteration
	local CurrentFPS = (tick() - Start >= 1 and #FrameUpdateTable) or (#FrameUpdateTable / (tick() - Start))
	CurrentFPS = CurrentFPS - CurrentFPS % 1
	FpsLabel.Text = ("死亡时间:"..os.date("%H").."时"..os.date("%M").."分"..os.date("%S"))end
Start = tick()
Heartbeat:Connect(HeartbeatUpdate)
local Window = OrionLib:MakeWindow({Name = "AT", HidePremium = false, SaveConfig = true,IntroText = "AT", ConfigFolder = "AT"})
game:GetService("StarterGui"):SetCore("SendNotification",{ Title = "AT"; Text ="欢迎使用AT"; Duration = 4; })
local about = Window:MakeTab({
    Name = "作者信息",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})
about:AddParagraph("作者: YOL")
about:AddParagraph("作者qq: 91")
about:AddParagraph("qq群: 91")
local about = Window:MakeTab({
    Name = "玩家信息",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})
about:AddParagraph("您的用户名:"," "..game.Players.LocalPlayer.Name.."")
about:AddParagraph("您的注入器:"," "..identifyexecutor().."")
about:AddParagraph("您当前服务器的ID"," "..game.GameId.."")
local about = Window:MakeTab({
    Name = "公告",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})
about:AddParagraph("94")
about:AddParagraph("93")
about:AddParagraph("97")
about:AddParagraph("92")
local Tab =Window:MakeTab({
	Name = "复制作者信息",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
Tab:AddButton({
	Name = "复制作者QQ",
	Callback = function()
     setclipboard("4")
  	end
})
Tab:AddButton({
	Name = "复制QQ群",
	Callback = function()
     setclipboard("93")
  	end
})
OrionLib:MakeNotification({
	Name = "AT",
	Content = "欢迎使用AT（最强战场）",
	Image = "rbxassetid://4483345998",
	Time = 2})local Tab = Window:MakeTab({
    Name = "最强战场破防脚本",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})local Section = Tab:AddSection({
	Name = "各种功能"
})
Tab:AddButton({
	Name = "甩飞（会封）",
	Callback = function()     loadstring(game:HttpGet("https://pastebin.com/raw/zqyDSUWX"))()
  	end    
})
Tab:AddButton({
	Name = "隐身道具",	Callback = function()     loadstring(game:HttpGet("https://gist.githubusercontent.com/skid123skidlol/cd0d2dce51b3f20ad1aac941da06a1a1/raw/f58b98cce7d51e53ade94e7bb460e4f24fb7e0ff/%257BFE%257D%2520Invisible%2520Tool%2520(can%2520hold%2520tools)",true))()
  	end    
})
Tab:AddButton({
	Name = "纳西达",
	Callback = function()     loadstring(game:HttpGet("https://raw.githubusercontent.com/rbxluau/Roblox/main/ScriptHub.lua"))()
  	end    
})
