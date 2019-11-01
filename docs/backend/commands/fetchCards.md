---
title: Fetch Cards
permalink: /docs/backend/commands/fetchCards
---

# Fetch Cards
Contrary to the [fetchAllPlayedCards command][fetch-all-played-cards] this one is made for the players of the game that are able to lay a card.

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
The server will respond with a collection of all cards without text. Only with their UUIDs. This can be useful when the frontend tries to display the players that haven't picked yet.
```json
{
    "errorCode": 0,
    "message": "OK",
    "jsonData": {
        "player-one-uuid": [
            {
                "uuid": "some-random-uuid-here"
            }
        ],
        "player-two-uuid": [
            {
                "uuid": "some-random-uuid-here"
            },
            {
                "uuid": "some-random-uuid-here"
            }
        ]
    }
}
```


[fetch-all-played-cards]: {{site.baseurl}}/docs/backend/commands/fetchAllPlayedCards