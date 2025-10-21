# Car Thief — 3M Studio

**Make car theft meaningful.** A mafia-grade, job-gated system for stealing *owned* vehicles, storing/scrapping them, and managing your black‑market network with unlockable drop‑off NPCs and a slick LB‑Tablet app.

## Why you'll love it
- **Real consequences** — moves records between `owned_vehicles` ⇄ `ukradena_vozila` with timestamps
- **Balanced economy** — dynamic payouts per model via `data/vehicle_prices.json` × `Config.VehicleScrapPercent`
- **Immersive UX** — LB‑Tablet companion app + classic NUI garage
- **Server‑first security** — all critical validations on the server
- **Plug‑and‑play keys** — auto‑detects `qs-vehiclekeys` or `wasabi_carlock` (or use `none`)

## Features
- Job‑locked stealing (`Config.JobName`) with **lockpick/coding minigame** (`exports['cardecode']:StartVehicleCoding`)
- **Unlockable drop‑off NPCs** (buy with cash, persists per job)
- **Return** a car to owner (spawns to player) or **Destroy for cash**
- **Discord logging** for stolen/returned/scrapped actions
- **Tablet app** (custom LB‑Tablet) with screenshots listing
- **Admin tools**: `/reloadvehprices`, `/setvehprice`, `/getvehprice`

## Configuration (highlights)
```lua
Config.JobName = 'automafija'
Config.MaxStolenVehicles = 15
Config.VehicleScrapPercent = 0.30
Config.KeySystem = 'auto' -- auto | qs | wasabi | none
Config.Lockpick = {
  Enabled = true, JobOnly = true, PromptKey = 38,
  MinDistance = 2.5, CooldownMs = 5000, ConsumeOnStart = false,
  ItemName = 'lockpick',
}
```
> Prices come from `data/vehicle_prices.json` (lowercase keys). Use `/setvehprice` in‑game to update & persist.

## Dependencies
- ESX 1.12.4, ox_lib, oxmysql, lb-tablet
- Optional: ox_target, ox_inventory, okokNotify/brutal_notify, qs-vehiclekeys or wasabi_carlock

## What you can customize in `functions.lua`
- **Notify bridge** (`okok` / `brutal` / `esx` chat)
- **Key systems adapter** (`qs-vehiclekeys`, `wasabi_carlock`, or `none`)
- **Server/Client hooks** for coding results & cooldowns

## Notes
- Script auto‑creates `ukradena_vozila` table by reflecting columns from `owned_vehicles` (+ `ukradeno_at`)
- Name mappings for owners are pulled from `users (identifier, firstname, lastname)`
