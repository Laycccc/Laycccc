local gui = Instance.new("ScreenGui")
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0.2, 0, 0.3, 0)
frame.BackgroundColor3 = Color3.fromRGB(0, 0, 100)
frame.Active = true
frame.Draggable = true
frame.Position = UDim2.new(0.5, 0, 0.5, 0)
frame.Parent = gui
local madeByText = Instance.new("TextLabel")
madeByText.Size = UDim2.new(1, 0, 0.1, 0)
madeByText.Position = UDim2.new(0, 0, 0.9, 0)
madeByText.Text = "Made by gta5gmplyofficial"
madeByText.TextColor3 = Color3.fromRGB(255, 255, 255)
madeByText.BackgroundTransparency = 1
madeByText.FontSize = Enum.FontSize.Size18
madeByText.Parent = frame
local pilihText = Instance.new("TextLabel")
pilihText.Size = UDim2.new(1, 0, 0.2, 0)
pilihText.Position = UDim2.new(0, 0, 0, 0)
pilihText.Text = "Pilih FPS"
pilihText.TextColor3 = Color3.fromRGB(255, 255, 255)
pilihText.FontSize = Enum.FontSize.Size24
pilihText.Parent = frame
local options = {"60 FPS", "120 FPS", "255 FPS", "Max FPS"}
for i, option in ipairs(options) do
    local fpsButton = Instance.new("TextButton")
    fpsButton.Name = option
    fpsButton.Size = UDim2.new(1, 0, 0.2, 0)
    fpsButton.Position = UDim2.new(0, 0, (i-1) * 0.2, 0)
    fpsButton.Text = option
    fpsButton.Parent = frame
    fpsButton.MouseButton1Click:Connect(function()
        if option == "Max FPS" then
            fpsButton.TextColor3 = Color3.fromRGB(0, 255, 0)
        end
        local notification = Instance.new("TextLabel")
        notification.Size = UDim2.new(0.3, 0, 0.1, 0)
        notification.Position = UDim2.new(0.5, 0, 0.8, 0)
        notification.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        notification.TextColor3 = Color3.fromRGB(0, 0, 0)
        notification.Text = "Fps selected successfully"
        notification.Parent = gui
        wait(2)
        notification:Destroy()
    end)
end
