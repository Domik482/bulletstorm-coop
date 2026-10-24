# bulletstorm-coop

# Bulletstorm: Full Clip Edition — Campaign Co-op Mod

A work-in-progress cooperative campaign modification for **Bulletstorm: Full Clip Edition** (PC / Unreal Engine 3), built with the help of [Co-op Anything](https://coopanything.app).

Previously, Bulletstorm only supported multiplayer in horde-style "Anarchy" and "Echo" modes. This mod unlocks true 2-player cooperative play across the main single-player story campaign by patching UnrealScript bytecode (`StormGame.upk`) and managing map routing via a standalone installer.

## Current Status: Alpha (v0.21)

### What is currently working & synchronized:
- **Story Campaign Progression:** Host and client load directly into single-player campaign chapters via the multiplayer lobby framework.
- **Kismet & World State:** Story triggers, cutscenes, doors, dynamic obstacles, and wave spawners synchronize across players (includes co-op proximity checks for key triggers so one player doesn't soft-lock the other).
- **Enemies & Combat:** AI enemies, physics, skillshots, and combat encounters are shared on the server.
- **Checkpoints & Respawning:** Campaign checkpoint saves and co-op player respawning/teleportation to the current story stage.
- **Dropkit (Shop) & Tutorials:** Custom client-side Dropkit access (`[F]` interaction) and non-pausing multiplayer HUD notifications for campaign tutorials.

### Known Issues (In Progress):
- Remote player vertical weapon aim offset (`AimOffset` pitch) visually stays flat.
- Minor visual beam target offsets when a remote player interacts with the Dropkit leash.
- Client Dropkit UI weapon list population under refinement.

## Installation
1. Unpack the latest release archive (`BulletstormCoop_v0.XX`).
2. Run `Установить.bat` (uses hard links and applies bytecode patches to `StormGame.upk` without requiring external Python dependencies).
3. Launch the game via the generated shortcut **"Bulletstorm Coop - играть"**.
