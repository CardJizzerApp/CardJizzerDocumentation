---
title: Pick Card
permalink: /docs/backend/commands/pickCard
---

# Pick Card

## Prerequisites
- Logged in
- User needs to be in a game with [GameState][game-state] `INGAME`
- User needs to be the CardJizzer of the round

`PickCard` is a command only available for the current rounds cardJizzer. It's the way of picking the best card of the round. All other players are permitted using this.

## Sample
```json
{
    "command": "pickcard",
    "params": {
        "carduuid": "carduuid-here"
    }
}
```

## Response
```json
{
    "errorCode": 0,
    "message": "OK",
}
```

[game-state]: {{site.baseurl}}/docs/backend/gameState