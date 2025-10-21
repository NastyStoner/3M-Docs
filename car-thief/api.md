---
title: API (Events & Callbacks)
parent: Car Thief
nav_order: 4
---

# API

## Server events

```lua
-- automafija:tryStealVehicle(plate, modelName)
-- Store a vehicle into the stolen pool (job-restricted)
automafija:tryStealVehicle(plate, modelName)

-- automafija:returnVehicle(plate)
-- Return vehicle to owned_vehicles and spawn to caller
automafija:returnVehicle(plate)

-- automafija:deleteVehicleForCash(plate)
-- Delete from stolen pool and pay cash
automafija:deleteVehicleForCash(plate)

-- automafija:getStolenVehicles()
-- Open NUI garage with list
automafija:getStolenVehicles()

-- automafija:buyNpc(npcId)
-- Buy/unlock a drop-off NPC for the job
automafija:buyNpc(npcId)

-- automafija:hasNpcAccess(cb)  ->  { [npcId]=true/false, ... }
automafija:hasNpcAccess(function(map) ... end)

-- automafija:canStoreVehicle(cb)  ->  boolean
automafija:canStoreVehicle(function(canStore) ... end)

-- automafija:getStolenVehiclesForTablet(cb)
-- -> array of { id, owner, vehicleLabel, registration, buybackPrice }
automafija:getStolenVehiclesForTablet(function(list) ... end)

// returnVehicle({ plate })
returnVehicle({ plate })

// deleteVehicle({ plate })
deleteVehicle({ plate })

// getStolenVehicles()
getStolenVehicles()

// closeGarage()
closeGarage()

App id: Config.Identifier  (default: automafija-app)
When opened: server callback populates items
Internal messages: SET_CARS  (items array)

