---
title: Login
permalink: /docs/backend/commands/login
---

# Login

{% include alert.html type="info" title="WIP" content="Work In Progress. Once finished, this alert will disappear." %}

`Login` is a command used for assign the `User`-object with Google-OAuth credentials, stored in the database to the websocket sending this command.

The websocket can then work with the google credentials and be identifiable.

## Sample
```json
{
    "command": "login",
    "params": {
        "token": "Google-Token"
    }
}
```

In this case `params.token` is describing the `Google-OAuth-Access-Token`.

## Response
```json
{
    "errorCode": 0,
    "message": "OK"
}
```
NOTE: This command doesn't provide `jsonData`.