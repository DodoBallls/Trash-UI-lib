# Trash UI Library 🗑️

A resizable, clean UI library for Roblox exploit scripts.

## How to Use

Paste this loader script into your executor to run the library directly from this repository:

```lua
-- Loading the UI...
print("Loading Trash UI...")

local TrashLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/DodoBallls/Trash-UI-lib/refs/heads/main/TRASH%20UI"))()
```
### 🚀 Adding UI Elements

Paste these code blocks underneath your main library loader to instantly add a Button, Toggle, or Slider to your window.

#### 1. Add a Button
```lua
lib:AddButton("Gravity switch", function()
    if workspace.Gravity == 196.2 then
        workspace.Gravity = 50
    else
        workspace.Gravity = 196.2
    end
end)
```

#### 2. Add a Toggle
```lua
lib:AddToggle("Fly Hack", function(state)
    print("Feature toggled:", state)
end)
```

#### 3. Add a Slider
```lua
lib:AddSlider("WalkSpeed", 16, 250, 16, function(value)
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
    end
end)
```
