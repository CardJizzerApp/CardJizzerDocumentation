---
title: Login
permalink: /docs/backend/commands/login
---

# Login

`Login` is a command used for assigning the `User`-object with Google-OAuth credentials, stored in the database to the websocket sending this command.

The websocket can then work with the google credentials and be identifiable.

## Sample
There are two ways to login:

1. Use a idToken received from Google OAuth login
```json
{
    "command": "login",
    "params": {
        "loginData": {
            "idToken": "id-token-here"
        }
    }
}
```

2. Or use your username and password like this
```json
{
    "command": "login",
    "params": {
        "loginData": {
            "username": "username-here",
            "password": "password-here"
        }
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