---
title: Set Username
permalink: /docs/backend/commands/setUsername
---

# SetUsername - [Deprecated]

{% include alert.html type="warning" title="Deprecated!" content="This command is deprecated and will be deleted soon. View the 'login' command for the alternative that should be used."%}

`SetUsername` is a way of making the websocket human-identifiable. Without this, the player would only see the websocket-uuid which we don't want him to see.

## Sample
```json
{
    "command": "setusername",
    "params": {
        "username": "your-username-here"
    }
}
```

## Response
```json
{
    "errorCode": 0,
    "message": "OK",
    "jsonData": {
        "newusername": "your-username-here"
    }
}
```