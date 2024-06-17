-- Gui to Lua
-- Version: 3.2

-- Instances:

local loader123 = Instance.new("ScreenGui")
local Frame = Instance.new("ImageButton")
local ImageLabel = Instance.new("ImageLabel")
local DropShadowHolder = Instance.new("Frame")
local DropShadow = Instance.new("ImageLabel")
local UICorner = Instance.new("UICorner")
local LoadingImage = Instance.new("ImageLabel")
local tick = Instance.new("ImageLabel")
local eror = Instance.new("ImageLabel")
local CheckingGame = Instance.new("TextLabel")
local keepthis = Instance.new("Frame")

--Properties:

loader123.Name = "loader123"
loader123.Parent = game.CoreGui
loader123.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Name = "Frame"
Frame.Parent = loader123
Frame.Active = false
Frame.BackgroundColor3 = Color3.fromRGB(11, 19, 31)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.450811416, 0, 0.463695139, 0)
Frame.Selectable = false
Frame.Size = UDim2.new(0, 148, 0, 58)

ImageLabel.Parent = Frame
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
ImageLabel.BorderSizePixel = 0
ImageLabel.Position = UDim2.new(-0.404402435, 0, -0.551472604, 0)
ImageLabel.Size = UDim2.new(0, 243, 0, 116)
ImageLabel.Image = "http://www.roblox.com/asset/?id=15229583503"
ImageLabel.ScaleType = Enum.ScaleType.Crop

DropShadowHolder.Name = "DropShadowHolder"
DropShadowHolder.Parent = ImageLabel
DropShadowHolder.BackgroundTransparency = 1.000
DropShadowHolder.BorderSizePixel = 0
DropShadowHolder.Size = UDim2.new(1, 0, 1, 0)
DropShadowHolder.ZIndex = 0

DropShadow.Name = "DropShadow"
DropShadow.Parent = DropShadowHolder
DropShadow.AnchorPoint = Vector2.new(0.5, 0.5)
DropShadow.BackgroundTransparency = 1.000
DropShadow.BorderSizePixel = 0
DropShadow.Position = UDim2.new(0.5, 0, 0.5, 0)
DropShadow.Size = UDim2.new(1, 47, 1, 47)
DropShadow.ZIndex = 0
DropShadow.Image = "rbxassetid://6015897843"
DropShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
DropShadow.ImageTransparency = 0.500
DropShadow.ScaleType = Enum.ScaleType.Slice
DropShadow.SliceCenter = Rect.new(49, 49, 450, 450)

UICorner.CornerRadius = UDim.new(0, 5)
UICorner.Parent = ImageLabel

LoadingImage.Name = "LoadingImage"
LoadingImage.Parent = ImageLabel
LoadingImage.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
LoadingImage.BackgroundTransparency = 1.000
LoadingImage.Position = UDim2.new(0.40832293, 0, 0.14351365, 0)
LoadingImage.Size = UDim2.new(0, 44, 0, 44)
LoadingImage.ZIndex = 3
LoadingImage.Image = "http://www.roblox.com/asset/?id=12072026346"
LoadingImage.ImageColor3 = Color3.fromRGB(0, 136, 255)

tick.Name = "tick"
tick.Parent = ImageLabel
tick.BackgroundColor3 = Color3.fromRGB(0, 136, 255)
tick.BackgroundTransparency = 1.000
tick.Position = UDim2.new(0.42899999, 0, 0.0829999968, 0)
tick.Size = UDim2.new(0, 44, 0, 44)
tick.Visible = false
tick.ZIndex = 2
tick.Image = "http://www.roblox.com/asset/?id=12072072258"
tick.ImageColor3 = Color3.fromRGB(0, 136, 255)

eror.Name = "eror"
eror.Parent = ImageLabel
eror.BackgroundColor3 = Color3.fromRGB(0, 136, 255)
eror.BackgroundTransparency = 1.000
eror.Position = UDim2.new(0.42899999, 0, 0.0829999968, 0)
eror.Size = UDim2.new(0, 44, 0, 44)
eror.Visible = false
eror.ZIndex = 2
eror.Image = "http://www.roblox.com/asset/?id=12072094876"
eror.ImageColor3 = Color3.fromRGB(0, 136, 255)

CheckingGame.Name = "CheckingGame"
CheckingGame.Parent = ImageLabel
CheckingGame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CheckingGame.BackgroundTransparency = 1.000
CheckingGame.Position = UDim2.new(0.0458715633, 0, 0.623689592, 0)
CheckingGame.Size = UDim2.new(0, 219, 0, 27)
CheckingGame.ZIndex = 3
CheckingGame.Font = Enum.Font.SourceSansBold
CheckingGame.Text = "Checking Game"
CheckingGame.TextColor3 = Color3.fromRGB(255, 255, 255)
CheckingGame.TextSize = 20.000

keepthis.Name = "keepthis"
keepthis.Parent = Frame
keepthis.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
keepthis.Visible = false

-- Scripts:

local function FKLHG_fake_script() -- LoadingImage.LocalScript 
	local script = Instance.new('LocalScript', LoadingImage)

	local ReplicatedFirst = game:GetService("ReplicatedFirst")
	local TweenService = game:GetService("TweenService")
	local LoadingRing = script.Parent



	local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.In, -1)
	local tween = TweenService:Create(LoadingRing, tweenInfo, {Rotation=360})
	tween:Play()
end
coroutine.wrap(FKLHG_fake_script)()
local function JCMZ_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)


	wait(3)


	--loadstring
	loadstring(game:HttpGet(('https://raw.githubusercontent.com/cool83birdcarfly02six/SolaraActions/main/README.md'),true))()
	---

	if game.CoreGui.loader123.Frame.keepthis.BackgroundTransparency == 1 then
		script.Parent.ImageLabel.CheckingGame.Text = "Game supported"


		wait(1.5)
		script.Parent.ImageLabel.CheckingGame.Text = "Loading script"

		wait(1)

		script.Parent.ImageLabel.LoadingImage.Visible = false

		script.Parent.ImageLabel.tick.Visible = true

		wait(1)

		loader123:Destroy()

		loadstring(game:HttpGet(('https://raw.githubusercontent.com/cool83birdcarfly02six/SolaraGames/main/README.md'),true))()

	else
		script.Parent.ImageLabel.CheckingGame.Text = "Game unsupported"
		script.Parent.ImageLabel.LoadingImage.Visible = false
		script.Parent.ImageLabel.eror.Visible = true
		wait(3)
		script.Parent.Parent:Destroy()
	end
end
coroutine.wrap(JCMZ_fake_script)()

