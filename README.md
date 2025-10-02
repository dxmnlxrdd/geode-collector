# Geode Collector

Auto teleport & geode collector with server hop.

---

## How to Use (config version)

Copy and paste this into your executor / autoexec:

```lua
getgenv().GeodeConfig = getgenv().GeodeConfig or {
    -- Timers / Delays
    HopIntervalSeconds = 40,   -- auto hop every X seconds
    DeadZoneTimeout    = 5,    -- seconds of no geodes before leaving zone
    PostTeleportDelay  = 1.5,  -- wait after teleport before scanning
    PerHitDelay        = 0.1,  -- delay between simulated hits
    CheckLoopDelay     = 0.2,  -- loop check delay

    -- Defaults for toggles
    DefaultAutoCollector = true,
    DefaultAutoHopDead   = false,
    DefaultAutoHopTimer  = true,

    -- Server scan options
    ServerPageLimit   = 6,
    ServersPerPage    = 100,
}

-- Zone order, removed if not wanted(auto skip if not unlocked)
-- it will go in order too
getgenv().ZoneGroups = getgenv().ZoneGroups or {
local ZoneGroups = {
    {"Frozen Peak"},
    {"Frostbitten Path"},
    {"Snowy Shores"},
    {"The Magma Furnace"},
    {"Caldera Island"},
    {"Windswept Beach"},
    {"Fortune River"},
    {"Rubble Creek"},
    {"Sunset Beach"},
    {"Fortune River Delta"},
    {"Overgrown Grotto"}
}
}

loadstring(game:HttpGet("https://raw.githubusercontent.com/dxmnlxrdd/geode-collector/refs/heads/main/main.lua", true))()
```
## Normal Version
```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/dxmnlxrdd/geode-collector/refs/heads/main/main.lua", true))()
```
