# API

## Client Exports
```lua
exports['car-thief']:IsAppOpen() --> boolean
```

## Server Exports
```lua
exports['car-thief']:ValidateResult(src, payload) --> boolean
```

## Net Events
- `nasty_carthief:client:openUI(meta)`
- `nasty_carthief:server:submitResult(payload)`

## NUI callbacks
- `ui:ready` · `ui:submit` · `ui:close`
