# Geode Collector

Auto teleport & geode collector with server hop.

---

## How to Use

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

-- Zone order
getgenv().ZoneGroups = getgenv().ZoneGroups or {
    {"Frostbitten Path"},
    {"Snowy Shores"},
    {"Caldera Island"},
    {"Fortune River"},
    {"Rubble Creek"},
    {"Sunset Beach"},
    {"Fortune River Delta"},
    {"Overgrown Grotto"},
}

loadstring(game:HttpGet("https://raw.githubusercontent.com/dxmnlxrdd/geode-collector/refs/heads/main/main.lua", true))()
