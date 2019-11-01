---
title: Fetch All Played Cards
permalink: /docs/backend/commands/fetchAllPlayedCards
---

# Fetch All Played Cards

## Prerequisites
- Logged in
- Game in state `INGAME`
- Sender needs to be the CardJizzer of the round

This command is designed to get the cards played by the players. The CardJizzer can then pick the best fitting card for the blackcard with the [pickCard Command][pick-card].

## Sample
```json
{
    "command": "fetchallplayedcards",
}
```

## Response
```json
{
    "errorCode": 0,
    "message": "OK",
    "jsonData": {
        "player-one-uuid": [
            {
                "text": "Some text",
                "uuid": "some-random-uuid-here"
            }
        ],
        "player-two-uuid": [
            {
                "text": "Some better text",
                "uuid": "some-random-uuid-here"
            }
        ]
    }
}
```

[pick-card]: {{site.baseurl}}/docs/backend/commands/pickCard