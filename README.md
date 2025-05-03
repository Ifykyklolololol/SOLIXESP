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

## Name ESP

```lua
ddddd
```

## Distance ESP

```lua
ESP:ToggleDistance(true) -- Enable distance ESP
ESP:ToggleDistance(false) -- Disable distance ESP
ESP:ToggleDistance() -- Toggle distance ESP
```

## Health ESP

```lua
ddddd
```

## Name ESP

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

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```

## Name ESP

```lua
ddddd
```
