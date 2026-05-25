--Example

-- Initialize Main Core Frame
local UIWindow = TrashLib:CreateWindow("Trash Lib Separate Edition")

-- Generate a New Page Layer
local mainTab = TabModule:CreateTab(UIWindow, "Movement Checks")

-- Injection of Elements Manually passing target location elements
ButtonModule:CreateButton(mainTab, "Kill Head", function()
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Head") then
        game.Players.LocalPlayer.Character.Head:Destroy()
    end
end)

ToggleModule:CreateToggle(mainTab, "Godmode Active", function(state)
    print("Godmode Status: ", state)
end)

SliderModule:CreateSlider(mainTab, "Custom Speed", 16, 250, 16, function(value)
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
    end
end)

