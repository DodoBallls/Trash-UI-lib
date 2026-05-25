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
local MainTab = lib:CreateTab("Main Cheats")
```

#### 2. Add a Button (Moon Gravity)
```lua
MainTab:AddButton("Moon Gravity", function()
    if workspace.Gravity == 196.2 then
        workspace.Gravity = 30 -- Low moon gravity
    else
        workspace.Gravity = 196.2 -- Default Roblox gravity
    end
end)
```

#### 3. Add a Toggle (Infinite Jump)
```lua
local InfiniteJumpEnabled = false
game:GetService("UserInputService").JumpRequest:Connect(function()
    if InfiniteJumpEnabled then
        game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass('Humanoid'):ChangeState("Jumping")
    end
end)

MainTab:AddToggle("Infinite Jump", function(state)
    InfiniteJumpEnabled = state
end)
```

#### 4. Add a Slider (Speed Multiplier)
```lua
MainTab:AddSlider("WalkSpeed", 16, 250, 16, function(value)
    local character = game:GetService("Players").LocalPlayer.Character
    if character and character:FindFirstChild("Humanoid") then
        character.Humanoid.WalkSpeed = value
    end
end)
```
