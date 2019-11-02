---
title: Fetch Cards
permalink: /docs/backend/commands/fetchCards
---

# Fetch Cards
This command is available to all players that are in a game with [state][game-state] `INGAME`. With it players can fetch their current hand and see which cards they are able to play.

Thus the prerequisites look like this.
## Prerequisites
- Logged in
- Game in state `INGAME`
- Sender needs not to be the CardJizzer

## Sample
```json
{
    "command": "fetchcards"
}
```

## Response
```json
{
    "errorCode": 0,
    "message": "OK",
    "jsonData": [
        {
            "text": "some-funny-text",
            "uuid": "some-random-uuid-here"
        },
        {
            "text": "some-funny-text",
            "uuid": "some-random-uuid-here"
        },
        {
            "text": "some-funny-text",
            "uuid": "some-random-uuid-here"
        }
    ]
}
```


[game-state]: {{site.baseurl}}/docs/backend/gameState