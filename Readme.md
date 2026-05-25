# Trash UI Library 🗑️

A resizable, clean UI library for Roblox exploit scripts.

## How to Use

Paste this loader script into your executor to run the library directly from this repository:

```lua
-- Loading the UI...
print("Loading Trash UI...")

local TrashLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/DodoBallls/Trash-UI-lib/refs/heads/main/TRASH%20UI"))()
```
# Trash UI Library 🗑️

A lightweight, resizable UI framework for Roblox exploits.

## 🚀 Independent Element Loaders

Run these scripts separately in your executor to instantly add elements to the UI.

### 1. Load Button Only
```lua
local TrashLib = loadstring(game:HttpGet("https://githubusercontent.com"))()

TrashLib:CreateButton("Quick Reset", function()
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Head") then
        game.Players.LocalPlayer.Character.Head:Destroy()
    end
end)
```

### 2. Load Toggle Only
```lua
local TrashLib = loadstring(game:HttpGet("https://githubusercontent.com"))()

TrashLib:CreateToggle("Fly Hack", function(state)
    print("Fly mode status: ", state)
end)
```

### 3. Load Slider Only
```lua
local TrashLib = loadstring(game:HttpGet("https://githubusercontent.com"))()

TrashLib:CreateSlider("WalkSpeed", 16, 250, 16, function(value)
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Humanoid") then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = value
    end
end)
```
