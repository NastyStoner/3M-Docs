---
title: API (Events & Callbacks)
parent: Car Thief
nav_order: 4
---

# API

## Server events
- `automafija:tryStealVehicle(plate, modelName)` — store a vehicle into stolen pool (job‑restricted)
- `automafija:returnVehicle(plate)` — return to owned_vehicles and spawn to caller
- `automafija:deleteVehicleForCash(plate)` — delete from stolen pool and pay cash
- `automafija:getStolenVehicles()` — open NUI garage with list
- `automafija:buyNpc(npcId)` — buy/unlock a drop‑off NPC for the job

## Server callbacks
- `automafija:hasNpcAccess(cb)` → `{ [npcId]=true/false, ... }`
- `automafija:canStoreVehicle(cb)` → `boolean`
- `automafija:getStolenVehiclesForTablet(cb)` → `array` of `{ id, owner, vehicleLabel, registration, buybackPrice }`

## Client events
- `automafija:receiveStolenVehicles(vehicles)` — opens NUI garage
- `automafija:spawnReturnedVehicle(vehiclePropsJson, plate)` — spawns vehicle to player and gives keys (if enabled)
- `automafija:closeGarage()` — close NUI
- `automafija:client:startCoding(meta)` — starts the Vehicle Coding minigame (client‑side)

## Client → NUI callbacks
- `returnVehicle({ plate })`
- `deleteVehicle({ plate })`
- `getStolenVehicles()`
- `closeGarage()`

## Tablet app messaging
- App id: `Config.Identifier` (default `automafija-app`)
- When opened → server callback populates items; internal messages: `SET_CARS` (items array)
