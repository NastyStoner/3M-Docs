---
title : Installation
parent: Beekeeper
nav_order: 1
---

# Installation

## Requirements
- **Es_extended 1.12.4 or above**
- **oxmysql**
- **ox_lib**
- **Ox_inventory**
- **Ox_Target**

## How to Install Script

- download resource from **https://portal.cfx.re/assets** unzip and put in your resources folder

## Server.cfg
```
ensure oxmysql
ensure ox_lib
ensure ox_inventory
ensure ox_target
ensure beekeeper
```

- add items to your ox inventory 
## Ox Inventory items 
```

['beehive_box'] = {
    label = 'Beehive Box',
    weight = 1000,
    stack = true,
    close = true,
    description = 'Plave Beehive Box',
    client = {
        event = 'beekeeping:placeBeehive' 
    }
},

['bee_food'] = {
    label = 'Bee Food',
    weight = 300,
    stack = true,
    close = true,
    description = 'Specific Bee Food',
},

['water_bottle'] = {
    label = 'Water for bees',
    weight = 200,
    stack = true,
    close = true,
    description = 'Bee water.',
},

['cleaning_agent'] = {
    label = 'Cleaning Agent',
    weight = 250,
    stack = true,
    close = true,
    description = Cleaning Agent',
},

['bee_heal'] = {
    label = 'Bee Heal',
    weight = 200,
    stack = true,
    close = true,
    description = 'Bee Heal',
},

['glass_jar'] = {
    label = 'Empty Jar',
    weight = 100,
    stack = true,
    close = true,
    description = 'Used for honey',
},
['honey_jar'] = {
    label = 'Honey Yar',
    weight = 100,
    stack = true,
    close = true,
    description = 'Honey Yar.',
},

['golden_honey'] = {
    label = 'Golden Honey',
    weight = 300,
    stack = true,
    close = true,
    description = 'Golden Honey',
},

['dark_honey'] = {
    label = 'Dark Honey',
    weight = 300,
    stack = true,
    close = true,
    description = Dark honey',
},
['propolis'] = {
    label = 'Propolis',
    weight = 100,
    stack = true,
    close = true,
    description = 'Propolis extracted from Bumblebee hives',
},
['propolis_jar'] = {
    label = 'Tegla Propolisa',
    weight = 20,
    stack = true,
    close = true,
    description = 'Tegla Propolisa ',
},
['royal_jelly'] = {
    label = 'matična mliječ',
    weight = 20,
    stack = true,
    close = true,
    description = 'matična mliječ',
},
['bee_venom'] = {
    label = 'Pčeljinji otrov',
    weight = 20,
    stack = true,
    close = true,
    description = 'Pčeljinji otrov',
},
['worker_bumbar'] = {
    label = 'Bumblebee',
    weight = 100,
    stack = true,
    close = true,
    description = 'Worker Bumblebee.',
},

['queen_bee'] = {
    label = 'Queen Bee',
    weight = 150,
    stack = false,
    close = true,
    description = Queen Bee.',
},
['bumbar_queen'] = {
    label = 'Queen Bumblebee',
    weight = 150,
    stack = false,
    close = true,
    description = Queen Bumblebee.',
},

['worker_bee'] = {
    label = 'Bees',
    weight = 100,
    stack = true,
    close = true,
    description = 'Worker Bee.',
},
['worker_bumbar'] = {
    label = 'Bumblebee',
    weight = 100,
    stack = true,
    close = true,
    description = 'Worker Bumblebee.',
},

```