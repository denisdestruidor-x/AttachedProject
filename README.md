local TS = game:GetService("TweenService")
local info = TweenInfo.new(0.1, Enum.EasingStyle.Back)

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UIConer = Instance.new("UICorner")
local UIStroke = Instance.new("UIStroke")
local UIStroke2 = Instance.new("UIStroke")
local TextLabel = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(103, 101, 98)
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.429034352, 0, -0.143847877, 0)
Frame.Size = UDim2.new(0, 275, 0, 50)

UIConer.Parent = Frame

UIStroke.Parent = Frame
UIStroke.Thickness = 3

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Size = UDim2.new(0, 275, 0, 50)
TextLabel.Font = Enum.Font.FredokaOne
TextLabel.Text = "Attached!"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 28.000
TextLabel.TextWrapped = true

UIStroke2.Parent = TextLabel
UIStroke2.Thickness = 2

local function Start()
	local Tween = TS:Create(Frame, info, {Position = UDim2.new(0.429034352, 0, -0.043847877, 0)})
	Tween:Play()
	Tween.Completed:Wait()
	wait(2)
	local Tween2 = TS:Create(Frame, info, {Position = UDim2.new(0.429034352, 0, -0.143847877, 0)})
	Tween2:Play()
	Tween2.Completed:Wait()
	Frame:Destroy()
end

wait(1)
Start()
