---
title: GameState
permalink: /docs/backend/gameState
---

# GameState

GameState is a object used for describing whether a lobby is joinable or not. The three states needed are:
- LOBBY
- INGAME
- STOPPED

## Lobby
This GameState allows every player to join a game.

## Ingame
This state is similar to the `STOPPED`-state. In both of them joining is permitted.

## Stopped
This GameState is the reason for not giving the lobby a boolean describing the joinability of the game.

In this state the gamers can review all cards of the recent game. Maybe there will be a possibility in the frontend for sharing a picture of the laid white- and blackcard.
