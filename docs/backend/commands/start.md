---
title: Start
permalink: /docs/backend/commands/start
---

# Start

This command is a `auth-required` one only available to the lobby-creator. If all players he wants in his game has joined the lobby he can start (update the [GameState][game-state] to `INGAME` and assign a new round to the game. Resulting in a new [event][event] triggered - the [gameStartedEvent][game-started-event])


[event]: {{site.baseurl}}/docs/backend/events/event
[game-started-event]: {{site.baseurl}}/docs/backend/events/gameStartedEvent