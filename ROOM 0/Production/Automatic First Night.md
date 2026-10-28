# Automatic first night
User decision, 2026-10-28: the first hotel round starts automatically without clock-in.
Server Main waits for a living spawned player and a successfully loaded coin profile, then calls the existing Shift.Start. Marker validation remains enforced. Other players joining night one are enrolled automatically up to MaxWorkers. It only starts night one; later-night behavior remains unchanged.
Config: AutoStartFirstNight=true; AutoStartPollSeconds=1.
Implemented in rbxyta-assets/tools/studio_hotel/shift/server/Main.server.luau and shared/R0_GameConfig.luau, installed through MCP into Hotel 133290122655457.

Validation: fresh Studio Play run, no clock interaction. Live Diagnostics BindableFunction returned Phase=Night, Night=1, zero marker problems and the player enrolled. Client clock displayed NIGHT 1 / 22:24. Direct MCP require has separate module state; use Diagnostics for authoritative runtime checks.
