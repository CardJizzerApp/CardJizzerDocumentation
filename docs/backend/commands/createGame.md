---
title: Create Game
permalink: /docs/backend/commands/createGame
---

# Create Game

This command is an `auth-required` command used for creating a lobby with the default [state][game-state] `LOBBY`.

Every lobby will get assigned the state `LOBBY` after creation. Once started by the owner the game will change its [state][game-state] and the users will receive their cards.

Furthermore a new `round` object will be assigned to the game object.

## Sample
```json
{
    "command": "creategame",
    "params": {
        "maxplayers": 4, // number
        "deckids": ["UDI12"], // string[]
        "password": "password", // string
        "pointstowin": 8, // number
        "maxroundtime": 30, // number <roundtime in seconds>
        "gametitle": "Pineapple" // string 
    }
}
```

The backend will then respond with a `errorCode` and the `gameId` in the `jsonData` object.

## Response
```json
{
    "errorCode": 0,
    "message": "A new game was created",
    "jsonData": {
        "gameId": "some-random-uuid-here"
    }
}
```

Beside there is also going to be a event triggered so every player currently connected with the websocket receives a [GameStartedEvent][game-created-event].

[game-state]: {{site.baseurl}}/docs/backend/gameState
[game-created-event]: {{site.baseurl}}/docs/backend/events/gameCreatedEvent