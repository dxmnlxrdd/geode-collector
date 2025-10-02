# geode-collector

##how to use
getgenv().GeodeConfig = getgenv().GeodeConfig or {
    -- Timers / Delays
    HopIntervalSeconds = 40,
    DeadZoneTimeout    = 5,
    PostTeleportDelay  = 1.5,
    PerHitDelay        = 0.1,
    CheckLoopDelay     = 0.2,

    -- Defaults for toggles
    DefaultAutoCollector = true,
    DefaultAutoHopDead   = false,
    DefaultAutoHopTimer  = true,

    -- Server scan options
    ServerPageLimit   = 6,
    ServersPerPage    = 100,
}

-- Zone order
local ZoneGroups = {
    {"Frostbitten Path"},
    {"Snowy Shores"},
    {"Caldera Island"},
    {"Fortune River"},
    {"Rubble Creek"},
    {"Sunset Beach"},
    {"Fortune River Delta"},
    {"Overgrown Grotto"}
}

loadstring(game:HttpGet("https://raw.githubusercontent.com/dxmnlxrdd/geode-collector/refs/heads/main/main.lua",true))()
