# Solix ESP Docs



# Loadstring

```lua
local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/Ifykyklolololol/SOLIXESP/refs/heads/main/EspSource"))()
```

## Core Functions
## Initialization and Cleanup

```lua
ESP:Init() -- Initializes the ESP library (called automatically)
ESP:Destroy() -- Cleans up all resources used by the ESP library
```


## Toggle ESP

```lua
ESP:Toggle(true) -- Enable ESP
ESP:Toggle(false) -- Disable ESP
ESP:Toggle() -- Toggle between enabled and disabled
```

## Box ESP

```lua
ESP:ToggleBox(true) -- Enable box ESP
ESP:ToggleBox(false) -- Disable box ESP
ESP:ToggleBox() -- Toggle box ESP
ESP:SetBoxType("2D") -- Set box type ("2D", "3D", "Corner")
```

## Name ESP

```lua
ESP:ToggleName(true) -- Enable name ESP
ESP:ToggleName(false) -- Disable name ESP
ESP:ToggleName() -- Toggle name ESP
```

## Distance ESP

```lua
ESP:ToggleDistance(true) -- Enable distance ESP
ESP:ToggleDistance(false) -- Disable distance ESP
ESP:ToggleDistance() -- Toggle distance ESP
```

## Health ESP

```lua
ESP:ToggleHealth(true) -- Enable health ESP
ESP:ToggleHealth(false) -- Disable health ESP
ESP:ToggleHealth() -- Toggle health ESP
ESP:SetHealthBarType("Vertical") -- Set health bar type ("Vertical", "Horizontal")
```

## Tracer ESP

```lua
ESP:ToggleTracer(true) -- Enable tracer ESP
ESP:ToggleTracer(false) -- Disable tracer ESP
ESP:ToggleTracer() -- Toggle tracer ESP
ESP:SetTracerOrigin("Bottom") -- Set tracer origin ("Bottom", "Center", "Mouse")
ESP:SetTracerStyle("Line") -- Set tracer style ("Line", "Dashed", "Dotted") -- DO NOT USE DASHED NOR DOTTED THEY WILL COOK UR FPS
```

## Chams ESP

```lua
ESP:ToggleChams(true) -- Enable chams ESP
ESP:ToggleChams(false) -- Disable chams ESP
ESP:ToggleChams() -- Toggle chams ESP
```

## Skeleton ESP

```lua
ESP:ToggleSkeleton(true) -- Enable skeleton ESP
ESP:ToggleSkeleton(false) -- Disable skeleton ESP
ESP:ToggleSkeleton() -- Toggle skeleton ESP
ESP:SetSkeletonStyle("Line") -- Set skeleton style (options: "Line", "Dashed", "Dotted")
```

## Head Dot ESP

```lua
ESP:ToggleHeadDot(true) -- Enable head dot ESP
ESP:ToggleHeadDot(false) -- Disable head dot ESP
ESP:ToggleHeadDot() -- Toggle head dot ESP
```

## Tool ESP

```lua
-- Tool ESP is controlled via settings
ESP.Settings.ToolEnabled = true -- Enable tool ESP
ESP.Settings.ToolEnabled = false -- Disable tool ESP
```

## State ESP

```lua
-- State ESP is controlled via settings
ESP.Settings.StateEnabled = true -- Enable state ESP
ESP.Settings.StateEnabled = false -- Disable state ESP
```

## Hitbox ESP

```lua
-- Hitbox ESP is controlled via settings
ESP.Settings.HitboxEnabled = true -- Enable hitbox ESP
ESP.Settings.HitboxEnabled = false -- Disable hitbox ESP
```

## Aim Point ESP

```lua
-- Aim Point ESP is controlled via settings
ESP.Settings.AimPointEnabled = true -- Enable aim point ESP
ESP.Settings.AimPointEnabled = false -- Disable aim point ESP
```

## Custom Text ESP

```lua
ESP:ToggleCustomText(true) -- Enable custom text ESP
ESP:ToggleCustomText(false) -- Disable custom text ESP
ESP:ToggleCustomText() -- Toggle custom text ESP
```

## Team Check ESP

```lua
-- Dont recommend since this only works if game uses the Teams Service 
ESP:ToggleTeamCheck(true) -- Enable team check
ESP:ToggleTeamCheck(false) -- Disable team check
ESP:ToggleTeamCheck() -- Toggle team check
```

## Visible Check ESP

```lua
ESP:ToggleVisibilityCheck(true) -- Enable visibility check
ESP:ToggleVisibilityCheck(false) -- Disable visibility check
ESP:ToggleVisibilityCheck() -- Toggle visibility check
```

## Rainbow ESP

```lua
-- Pro lgtbtwq mode fr
ESP:ToggleRainbowMode(true) -- Enable rainbow mode
ESP:ToggleRainbowMode(false) -- Disable rainbow mode
ESP:ToggleRainbowMode() -- Toggle rainbow mode
ESP:SetRainbowSpeed(1) -- Set rainbow speed (default is 1)
```

# Customization Functions

## Colors

```lua
ESP:SetColor(Color3.fromRGB(255, 255, 255)) -- Set color for all ESP elements
ESP:SetTeamColor(Color3.fromRGB(0, 255, 0)) -- Set color for teammates
ESP:SetEnemyColor(Color3.fromRGB(255, 0, 0)) -- Set color for enemies
```

## Transparency

```lua
ESP:SetTransparency(0.7) -- Set transparency for all ESP elements (0-1)
```

## Thickness

```lua
ESP:SetThickness(1) -- Set thickness for all line-based ESP elements
```

## Text Size

```lua
ESP:SetTextSize(14) -- Set text size for all text-based ESP elements
```

## Text Font

```lua
ESP:SetFont(2) -- Set font for all text-based ESP elements
-- Font options: 0 (Legacy), 1 (UI), 2 (System), 3 (Monospace) 
```

## Outline

```lua
ESP:SetOutline(true) -- Enable outline for all text-based ESP elements
ESP:SetOutlineColor(Color3.fromRGB(0, 0, 0)) -- Set outline color
ESP:SetOutlineTransparency(0.5) -- Set outline transparency (0-1)
```

## Set Distance

```lua
ESP:SetMaxDistance(1000) -- Set maximum distance for ESP
```

# Player Management

## Whitelist

```lua
ESP:AddToWhitelist("PlayerName") -- Add player by name
ESP:AddToWhitelist(123456789) -- Add player by UserId
ESP:AddToWhitelist(player) -- Add player object
ESP:RemoveFromWhitelist("PlayerName") -- Remove player by name
ESP:RemoveFromWhitelist(123456789) -- Remove player by UserId
ESP:RemoveFromWhitelist(player) -- Remove player object
ESP:ClearWhitelist() -- Clear whitelist
```

## Blacklist

```lua
ESP:AddToBlacklist("PlayerName") -- Add player by name
ESP:AddToBlacklist(123456789) -- Add player by UserId
ESP:AddToBlacklist(player) -- Add player object
ESP:RemoveFromBlacklist("PlayerName") -- Remove player by name
ESP:RemoveFromBlacklist(123456789) -- Remove player by UserId
ESP:RemoveFromBlacklist(player) -- Remove player object
ESP:ClearBlacklist() -- Clear blacklist
```
# Settings Management

## Get/Set Settings

```lua
local settings = ESP:GetSettings() -- Get all settings
ESP:SetSettings({
    BoxEnabled = true,
    BoxColor = Color3.fromRGB(255, 0, 0),
    -- Add more settings as needed
}) -- Set multiple settings at once
ESP:ResetSettings() -- Reset all settings to default
```

## Refresh Rate

```lua
ESP:SetRefreshRate(0.01) -- Set refresh rate in seconds
```

# Keybind Management

## Configure Keybinds

```lua
ESP:SetKeybind("Toggle", Enum.KeyCode.RightShift) -- Set keybind for toggling ESP
ESP:ConfigureKeybinds({
    Toggle = Enum.KeyCode.RightShift,
    Box = Enum.KeyCode.One,
    Name = Enum.KeyCode.Two,
    Distance = Enum.KeyCode.Three,
    Health = Enum.KeyCode.Four,
    Tracer = Enum.KeyCode.Five,
    Chams = Enum.KeyCode.Six,
    Skeleton = Enum.KeyCode.Seven,
    HeadDot = Enum.KeyCode.Eight
}) -- Configure all keybinds at once
```

## Enable/Disable Keybinds

```lua
ESP:EnableKeybinds(true) -- Enable keybinds
ESP:EnableKeybinds(false) -- Disable keybinds
ESP:EnableKeybinds() -- Toggle keybinds
```

## Get Keybinds

```lua
local keybinds = ESP:GetKeybinds() -- Get all keybinds
```

# Custom Text Example

## Set Custom Text

```lua
-- Set custom text for a specific player
ESP:SetCustomText(player, function(player, character)
    -- Return the text to display
    return "Custom Text"
end)

-- Example: Display player's health
ESP:SetCustomText(player, function(player, character)
    local humanoid = character:FindFirstChild("Humanoid")
    if humanoid then
        return "Health: " .. math.floor(humanoid.Health)
    end
    return "No Health"
end)

-- Example: Display multiple stats
ESP:SetCustomText(player, function(player, character)
    local humanoid = character:FindFirstChild("Humanoid")
    local health = humanoid and math.floor(humanoid.Health) or "N/A"
    local tool = character:FindFirstChildOfClass("Tool")
    local toolName = tool and tool.Name or "None"
    return "Health: " .. health .. " | Tool: " .. toolName
end)
```

##  Custom Text Appearance

```lua
-- Customize appearance through settings
ESP.Settings.CustomTextColor = Color3.fromRGB(255, 255, 0) -- Yellow text
ESP.Settings.CustomTextSize = 14
ESP.Settings.CustomTextPosition = "bottom" -- Options: "top", "bottom", "left", "right"
ESP.Settings.CustomTextYOffset = 60
ESP.Settings.CustomTextXOffset = 0
ESP.Settings.CustomTextOutline = true
ESP.Settings.CustomTextOutlineColor = Color3.fromRGB(0, 0, 0)
```

# Settings Reference

## General Settings

```lua
ESP.Settings.Enabled = true -- Master toggle
ESP.Settings.RefreshRate = 0.01 -- Update rate in seconds
ESP.Settings.MaxDistance = 1000 -- Maximum distance for ESP visibility
ESP.Settings.TeamCheck = false -- Check if player is on the same team
ESP.Settings.VisibilityCheck = false -- Check if player is visible
ESP.Settings.IgnoreInvisible = true -- Ignore players with transparent characters
ESP.Settings.IgnoreDead = true -- Ignore dead players
ESP.Settings.IgnoreNPCs = false -- Ignore NPCs
ESP.Settings.IgnoreFriends = false -- Ignore friends
ESP.Settings.UseDisplayName = false -- Use DisplayName instead of Name
ESP.Settings.AlwaysOnTop = true -- Draw ESP on top of other elements
ESP.Settings.DrawOnTop = true -- Draw ESP on top of game world
ESP.Settings.ZIndex = 1 -- Z-index for drawing order
ESP.Settings.RenderPriority = 1 -- Render priority
ESP.Settings.FadeWithDistance = true -- Fade ESP elements with distance
ESP.Settings.VisibilityFade = true -- Fade ESP elements when not visible
ESP.Settings.SmoothTransitions = true -- Smooth transitions for ESP elements
ESP.Settings.TransitionSpeed = 0.2 -- Transition speed
```

## Box Settings

```lua
ESP.Settings.BoxEnabled = true -- Enable box ESP
ESP.Settings.BoxType = "2D" -- Box type: "2D", "3D", "Corner"
ESP.Settings.BoxColor = Color3.fromRGB(255, 255, 255) -- Box color
ESP.Settings.BoxTransparency = 0.7 -- Box transparency (0-1)
ESP.Settings.BoxThickness = 1 -- Box line thickness
ESP.Settings.BoxFilled = false -- Fill box
ESP.Settings.BoxFilledTransparency = 0.3 -- Box fill transparency (0-1)
ESP.Settings.BoxOutline = true -- Draw box outline
ESP.Settings.BoxOutlineColor = Color3.fromRGB(0, 0, 0) -- Box outline color
ESP.Settings.BoxOutlineTransparency = 0.5 -- Box outline transparency (0-1)
ESP.Settings.BoxRoundedRadius = 5 -- Box corner radius for rounded boxes
ESP.Settings.BoxGradientColor = Color3.fromRGB(0, 0, 255) -- Box gradient color
ESP.Settings.UsePartBoundingBox = true -- Use part bounding box
ESP.Settings.BoxPadding = Vector3.new(0.5, 0.5, 0.5) -- Box padding
ESP.Settings.CornerSize = 8 -- Corner size for corner box
```

## Name Settings

```lua
ESP.Settings.NameEnabled = true -- Enable name ESP
ESP.Settings.NameColor = Color3.fromRGB(255, 255, 255) -- Name color
ESP.Settings.NameTransparency = 0.7 -- Name transparency (0-1)
ESP.Settings.NameOutline = true -- Draw name outline
ESP.Settings.NameOutlineColor = Color3.fromRGB(0, 0, 0) -- Name outline color
ESP.Settings.NameOutlineTransparency = 0.5 -- Name outline transparency (0-1)
ESP.Settings.NameSize = 14 -- Name text size
ESP.Settings.NameFont = 2 -- Name font
ESP.Settings.NamePosition = "top" -- Name position: "top", "bottom", "left", "right"
ESP.Settings.NameYOffset = -15 -- Name Y offset
ESP.Settings.NameXOffset = 0 -- Name X offset
```

## Distance Settings

```lua
ESP.Settings.DistanceEnabled = true -- Enable distance ESP
ESP.Settings.DistanceColor = Color3.fromRGB(255, 255, 255) -- Distance color
ESP.Settings.DistanceTransparency = 0.7 -- Distance transparency (0-1)
ESP.Settings.DistanceOutline = true -- Draw distance outline
ESP.Settings.DistanceOutlineColor = Color3.fromRGB(0, 0, 0) -- Distance outline color
ESP.Settings.DistanceOutlineTransparency = 0.5 -- Distance outline transparency (0-1)
ESP.Settings.DistanceSize = 13 -- Distance text size
ESP.Settings.DistanceFont = 2 -- Distance font
ESP.Settings.DistancePosition = "bottom" -- Distance position: "top", "bottom", "left", "right"
ESP.Settings.DistanceYOffset = 15 -- Distance Y offset
ESP.Settings.DistanceXOffset = 0 -- Distance X offset
ESP.Settings.DistanceTextSize = true -- Scale distance text size with distance
```

## Health Settings

```lua
ESP.Settings.HealthEnabled = true -- Enable health ESP
ESP.Settings.HealthType = "Vertical" -- Health bar type: "Vertical", "Horizontal"
ESP.Settings.HealthColor = Color3.fromRGB(0, 255, 0) -- Health color
ESP.Settings.HealthTransparency = 0.7 -- Health transparency (0-1)
ESP.Settings.HealthOutline = true -- Draw health outline
ESP.Settings.HealthOutlineColor = Color3.fromRGB(0, 0, 0) -- Health outline color
ESP.Settings.HealthOutlineTransparency = 0.5 -- Health outline transparency (0-1)
ESP.Settings.HealthThickness = 1 -- Health line thickness
ESP.Settings.HealthPosition = "left" -- Health position: "top", "bottom", "left", "right"
ESP.Settings.HealthYOffset = 0 -- Health Y offset
ESP.Settings.HealthXOffset = -5 -- Health X offset
ESP.Settings.HealthBarThickness = 2 -- Health bar thickness
ESP.Settings.HealthGradient = true -- Use health gradient (red to green)
```

## Tracer Settings

```lua
ESP.Settings.TracerEnabled = true -- Enable tracer ESP
ESP.Settings.TracerColor = Color3.fromRGB(255, 255, 255) -- Tracer color
ESP.Settings.TracerTransparency = 0.7 -- Tracer transparency (0-1)
ESP.Settings.TracerThickness = 1 -- Tracer line thickness
ESP.Settings.TracerOutline = true -- Draw tracer outline
ESP.Settings.TracerOutlineColor = Color3.fromRGB(0, 0, 0) -- Tracer outline color
ESP.Settings.TracerOutlineTransparency = 0.5 -- Tracer outline transparency (0-1)
ESP.Settings.TracerOrigin = "Bottom" -- Tracer origin: "Bottom", "Center", "Mouse"
ESP.Settings.TracerYOffset = 0 -- Tracer Y offset
ESP.Settings.TracerXOffset = 0 -- Tracer X offset
ESP.Settings.TracerStyle = "Line" -- Tracer style: "Line", "Dashed", "Dotted" Please Do not use Dashed Nor Dotted they will cook ur fps
ESP.Settings.TracerDashSize = 3 -- Tracer dash size
ESP.Settings.TracerDashGap = 2 -- Tracer dash gap
```

## Chams Settings

```lua
ESP.Settings.ChamsEnabled = true -- Enable chams ESP
ESP.Settings.ChamsColor = Color3.fromRGB(255, 0, 0) -- Chams color
ESP.Settings.ChamsTransparency = 0.5 -- Chams transparency (0-1)
ESP.Settings.ChamsOutlineColor = Color3.fromRGB(0, 0, 0) -- Chams outline color
ESP.Settings.ChamsOutlineTransparency = 0.5 -- Chams outline transparency (0-1)
ESP.Settings.ChamsUseTeamColor = false -- Use team color for chams
ESP.Settings.ChamsVisibleOnly = false -- Only show chams when visible
ESP.Settings.ChamsDepthMode = "Occluded" -- Chams depth mode: "Occluded", "AlwaysOnTop"
ESP.Settings.ChamsOutlineEnabled = true -- Enable chams outline
ESP.Settings.ChamsTeamColor = true -- Use team color for chams
```

## Skeleton Settings

```lua
ESP.Settings.SkeletonEnabled = true -- Enable skeleton ESP
ESP.Settings.SkeletonColor = Color3.fromRGB(255, 255, 255) -- Skeleton color
ESP.Settings.SkeletonTransparency = 0.7 -- Skeleton transparency (0-1)
ESP.Settings.SkeletonThickness = 1 -- Skeleton line thickness
ESP.Settings.SkeletonOutline = true -- Draw skeleton outline
ESP.Settings.SkeletonOutlineColor = Color3.fromRGB(0, 0, 0) -- Skeleton outline color
ESP.Settings.SkeletonOutlineTransparency = 0.5 -- Skeleton outline transparency (0-1)
ESP.Settings.SkeletonStyle = "Line" -- Skeleton style: "Line", "Dashed", "Dotted"
ESP.Settings.SkeletonDashSize = 3 -- Skeleton dash size
ESP.Settings.SkeletonDashGap = 2 -- Skeleton dash gap
```

## Head Dot Settings

```lua
ESP.Settings.HeadDotEnabled = true -- Enable head dot ESP
ESP.Settings.HeadDotColor = Color3.fromRGB(255, 0, 0) -- Head dot color
ESP.Settings.HeadDotTransparency = 0.7 -- Head dot transparency (0-1)
ESP.Settings.HeadDotThickness = 1 -- Head dot thickness
ESP.Settings.HeadDotRadius = 3 -- Head dot radius
ESP.Settings.HeadDotFilled = true -- Fill head dot
ESP.Settings.HeadDotOutline = true -- Draw head dot outline
ESP.Settings.HeadDotOutlineColor = Color3.fromRGB(0, 0, 0) -- Head dot outline color
ESP.Settings.HeadDotOutlineTransparency = 0.5 -- Head dot outline transparency (0-1)
ESP.Settings.HeadDotYOffset = 0 -- Head dot Y offset
ESP.Settings.HeadDotXOffset = 0 -- Head dot X offset
ESP.Settings.HeadDotPulse = false -- Enable head dot pulse
ESP.Settings.HeadDotPulseSpeed = 1 -- Head dot pulse speed
ESP.Settings.HeadDotPulseSize = 1.5 -- Head dot pulse size
```

## Tool Settings

```lua
ESP.Settings.ToolEnabled = true -- Enable tool ESP
ESP.Settings.ToolColor = Color3.fromRGB(255, 255, 255) -- Tool color
ESP.Settings.ToolTransparency = 0.7 -- Tool transparency (0-1)
ESP.Settings.ToolOutline = true -- Draw tool outline
ESP.Settings.ToolOutlineColor = Color3.fromRGB(0, 0, 0) -- Tool outline color
ESP.Settings.ToolOutlineTransparency = 0.5 -- Tool outline transparency (0-1)
ESP.Settings.ToolSize = 13 -- Tool text size
ESP.Settings.ToolFont = 2 -- Tool font
ESP.Settings.ToolPosition = "bottom" -- Tool position: "top", "bottom", "left", "right"
ESP.Settings.ToolYOffset = 30 -- Tool Y offset
ESP.Settings.ToolXOffset = 0 -- Tool X offset
```

## State Settings

```lua
ddddd
```

## Name ESP

```lua
ESP.Settings.StateEnabled = true -- Enable state ESP
ESP.Settings.StateColor = Color3.fromRGB(255, 255, 255) -- State color
ESP.Settings.StateTransparency = 0.7 -- State transparency (0-1)
ESP.Settings.StateOutline = true -- Draw state outline
ESP.Settings.StateOutlineColor = Color3.fromRGB(0, 0, 0) -- State outline color
ESP.Settings.StateOutlineTransparency = 0.5 -- State outline transparency (0-1)
ESP.Settings.StateSize = 13 -- State text size
ESP.Settings.StateFont = 2 -- State font
ESP.Settings.StatePosition = "bottom" -- State position: "top", "bottom", "left", "right"
ESP.Settings.StateYOffset = 45 -- State Y offset
ESP.Settings.StateXOffset = 0 -- State X offset
```

## Aim Point Settings

```lua
ESP.Settings.AimPointEnabled = true -- Enable aim point ESP
ESP.Settings.AimPointColor = Color3.fromRGB(255, 0, 0) -- Aim point color
ESP.Settings.AimPointTransparency = 0.7 -- Aim point transparency (0-1)
ESP.Settings.AimPointThickness = 1 -- Aim point thickness
ESP.Settings.AimPointRadius = 3 -- Aim point radius
ESP.Settings.AimPointFilled = true -- Fill aim point
ESP.Settings.AimPointOutline = true -- Draw aim point outline
ESP.Settings.AimPointOutlineColor = Color3.fromRGB(0, 0, 0) -- Aim point outline color
ESP.Settings.AimPointOutlineTransparency = 0.5 -- Aim point outline transparency (0-1)
ESP.Settings.AimPointYOffset = 0 -- Aim point Y offset
ESP.Settings.AimPointXOffset = 0 -- Aim point X offset
ESP.Settings.AimPointPulse = true -- Enable aim point pulse
ESP.Settings.AimPointPulseSpeed = 1 -- Aim point pulse speed
ESP.Settings.AimPointPulseSize = 1.5 -- Aim point pulse size
```

## Hitbox Settings

```lua
ESP.Settings.HitboxEnabled = true -- Enable hitbox ESP
ESP.Settings.HitboxColor = Color3.fromRGB(255, 0, 0) -- Hitbox color
ESP.Settings.HitboxTransparency = 0.7 -- Hitbox transparency (0-1)
ESP.Settings.HitboxThickness = 1 -- Hitbox thickness
ESP.Settings.UseCustomHitboxPoints = false -- Use custom hitbox points
ESP.Settings.CustomHitboxPoints = {
    Head = true,
    Torso = true,
    Arms = true,
    Legs = true
} -- Custom hitbox points
```

## Custom Text Settings

```lua
ESP.Settings.CustomTextEnabled = true -- Enable custom text ESP
ESP.Settings.CustomTextColor = Color3.fromRGB(255, 255, 255) -- Custom text color
ESP.Settings.CustomTextTransparency = 0.7 -- Custom text transparency (0-1)
ESP.Settings.CustomTextOutline = true -- Draw custom text outline
ESP.Settings.CustomTextOutlineColor = Color3.fromRGB(0, 0, 0) -- Custom text outline color
ESP.Settings.CustomTextOutlineTransparency = 0.5 -- Custom text outline transparency (0-1)
ESP.Settings.CustomTextSize = 13 -- Custom text size
ESP.Settings.CustomTextFont = 2 -- Custom text font
ESP.Settings.CustomTextPosition = "bottom" -- Custom text position: "top", "bottom", "left", "right"
ESP.Settings.CustomTextYOffset = 60 -- Custom text Y offset
ESP.Settings.CustomTextXOffset = 0 -- Custom text X offset
```

## Team Settings

```lua
ESP.Settings.TeamColor = true -- Use team color
ESP.Settings.EnemyColor = Color3.fromRGB(255, 0, 0) -- Enemy color
ESP.Settings.TeamColorMode = "Team" -- Team color mode: "Team", "Custom"
```

# Example Use Of ESP Lib

## Basic Setup

```lua
local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/Ifykyklolololol/SOLIXESP/refs/heads/main/EspSource"))()

-- Enable ESP
ESP:Toggle(true)

-- Configure basic settings
ESP:SetMaxDistance(2000)
ESP:ToggleTeamCheck(true)
ESP:ToggleVisibilityCheck(true)

-- Configure visual elements
ESP:ToggleBox(true)
ESP:SetBoxType("2D")
ESP:ToggleName(true)
ESP:ToggleDistance(true)
ESP:ToggleHealth(true)
ESP:ToggleTracer(true)
```

## Custom Player Info

```lua
local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/Ifykyklolololol/SOLIXESP/refs/heads/main/EspSource"))()

-- Enable ESP and custom text
ESP:Toggle(true)
ESP:ToggleCustomText(true)

-- Set custom text for all players
for _, player in pairs(game.Players:GetPlayers()) do
    if player ~= game.Players.LocalPlayer then
        ESP:SetCustomText(player, function(player, character)
            -- Get player data
            local humanoid = character:FindFirstChildOfClass("Humanoid")
            local health = humanoid and humanoid.Health or 0
            local maxHealth = humanoid and humanoid.MaxHealth or 100
            
            -- Get backpack items
            local backpack = player:FindFirstChildOfClass("Backpack")
            local itemCount = backpack and #backpack:GetChildren() or 0
            
            -- Format and return text
            return string.format("HP: %d/%d | Items: %d", 
                math.floor(health), 
                math.floor(maxHealth),
                itemCount)
        end)
    end
end

-- Handle new players
game.Players.PlayerAdded:Connect(function(player)
    if player ~= game.Players.LocalPlayer then
        ESP:SetCustomText(player, function(player, character)
            local humanoid = character:FindFirstChildOfClass("Humanoid")
            local health = humanoid and humanoid.Health or 0
            
            return "HP: " .. math.floor(health)
        end)
    end
end)
```

## Health ESP Color Based on Amount Of Health

```lua
local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/Ifykyklolololol/SOLIXESP/refs/heads/main/EspSource"))()

-- Enable ESP and custom text
ESP:Toggle(true)
ESP:ToggleCustomText(true)

-- Set custom text with dynamic colors
for _, player in pairs(game.Players:GetPlayers()) do
    if player ~= game.Players.LocalPlayer then
        ESP:SetCustomText(player, function(player, character)
            local humanoid = character:FindFirstChildOfClass("Humanoid")
            if not humanoid then return nil end
            
            local health = humanoid.Health
            local maxHealth = humanoid.MaxHealth
            local healthPercent = health / maxHealth
            
            -- Set color based on health percentage
            if healthPercent > 0.7 then
                ESP.Settings.CustomTextColor = Color3.fromRGB(0, 255, 0) -- Green for high health
            elseif healthPercent > 0.3 then
                ESP.Settings.CustomTextColor = Color3.fromRGB(255, 255, 0) -- Yellow for medium health
            else
                ESP.Settings.CustomTextColor = Color3.fromRGB(255, 0, 0) -- Red for low health
            end
            
            -- Also change box color based on health
            if healthPercent > 0.7 then
                ESP.Settings.BoxColor = Color3.fromRGB(0, 255, 0) -- Green for high health
            elseif healthPercent > 0.3 then
                ESP.Settings.BoxColor = Color3.fromRGB(255, 255, 0) -- Yellow for medium health
            else
                ESP.Settings.BoxColor = Color3.fromRGB(255, 0, 0) -- Red for low health
            end
            
            return "HP: " .. math.floor(health)
        end)
    end
end
```



