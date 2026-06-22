# Lexicon

- Add simple single response chat commands
- Manage command aliases

## Single Response Chat Commands

Structure:

- Game Chat Response:

```jsonc
{
  "command": "/discord", // the command name
  "responseType": "ClientChat", // response type, available are "ClientChat", "ServerChat", "Notification", "ClientChatGlobal", "ServerChatGlobal", "NotificationGlobal"
  "color": [1.0, 1.0, 1.0, 1.0], // color of the response for "ServerChat" and "Notification" in [R, G, B, A]
  "message": "https://bit.ly/rxp-discord", // the response
  "author": "Sinfuls [RXP] Cluster", // the response author
  "permissions": ["Default"], // permission groups allowed to use the command
  "aliases": ["/invite", "/dc"], // command aliases
}
```

- Notification Response:

```jsonc
{
  "command": "/shop", // the command name
  "responseType": "Notification",
  "color": [1.0, 1.0, 1.0, 1.0],
  "message": "F2 to open the shop!", // the response
  "author": "Sinfuls [RXP] Cluster", // the response author (not used)
  "notification": {
    "title": "Shop Information",
    "duration": 7.5, // how long the notification is displayed for
  },
  "permissions": ["Default"],
  "aliases": ["/kits", "/kit"],
}
```

## Aliases

Structure:

```jsonc
"/commandName": ["/alias1", "/alias2"]
```
