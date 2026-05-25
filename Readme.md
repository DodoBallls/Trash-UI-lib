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

Paste these code blocks underneath your main library loader to create tabs and instantly add working components to your window.

#### 1. Create a Tab
```lua
local MainTab = lib:CreateTab("Tab Name")
```

#### 2. Add a Button
```lua
MainTab:AddButton("Button Name", function()
    print("Button clicked!")
end)
```

#### 3. Add a Toggle
```lua
MainTab:AddToggle("Toggle Name", function(state)
    print("Toggle state:", state)
end)
```

#### 4. Add a Slider
```lua
MainTab:AddSlider("Slider Name", 0, 100, 50, function(value)
    print("Slider value:", value)
end)
```
# Trash-UI-lib

## Loader Fix

```lua
local TrashLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/DodoBallls/Trash-UI-lib/refs/heads/main/TRASH%20U"))()
local Window = TrashLib:CreateWindow("[Window Title Here]")

-- Button Example
Window:CreateButton("[Button Name]", function()
    -- [Your Code Here]
end)

-- Quick Reset Button Example
Window:CreateButton("Quick Reset", function()
    if game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("Head") then
        game.Players.LocalPlayer.Character.Head:Destroy()
    end
end)

-- Toggle Example
Window:CreateToggle("[Toggle Name]", function(state)
    if state then
        -- [Code for ON state]
    else
        -- [Code for OFF state]
    end
end)

-- Slider Example
Window:CreateSlider("[Slider Name]", [MinValue], [MaxValue], [DefaultValue], function(value)
    -- [Your Code Here]
end)
```
