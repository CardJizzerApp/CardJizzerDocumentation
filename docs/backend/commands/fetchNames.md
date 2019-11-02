---
title: Fetch Names
permalink: /docs/backend/commands/fetchNames
---

# Fetch Names

This command requires authentication. Furthermore the user needs to be in a lobby.

It is designed to fetch the names of the players that are currently with the user itself in the same game.

NOTE: This command does not require any params.

## Sample
```json
{
    "command": "fetchnames"
}
```

## Response
```json
{
    "errorCode": 0,
    "message": "OK",
    "jsonData": {
        "some-random-uuid-here-one": "username-one",
        "some-random-uuid-here-two": "username-two",
        "some-random-uuid-here-three": "username-three"
    }
}
```

Where `gameid` is the id received from the [`fetchGames`][fetchgames] command.


[GameState]: {{site.baseurl}}/docs/backend/gameState