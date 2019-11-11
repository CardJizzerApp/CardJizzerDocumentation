---
title: Play Card
permalink: /docs/backend/commands/playCard
---

# Play Card

## Prerequisites
- Logged in
- User needs to be in a game with [GameState][game-state] `INGAME`
- He has to **not be** the CardJizzer

Contrary to the [pickCard][pick-card] command playCard is designed for every other player of the round used for playing a card of their hand.

## Sample
```json
{
    "command": "playcard",
    "params": {
        "carduuid": "carduuid-here"
    }
}
```

NOTE: If the player hasn't got the carduuid on his hand (internal object storing all the playable cards).

[pick-card]: {{site.baseurl}}/docs/backend/commands/pickCard
