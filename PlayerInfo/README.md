# PlayerInfo

- Gets a player's in game info and allows display thru chat commands and rcon

---

# PlayerInfo Commands

- Console / RCON:

```text
PlayerInfo.reload - reload PlayerInfo's config
```

---

# Configuration

## Placeholders

Default values for player info fields

```jsonc
"placeholders": {
  "{charName}": "Unknown", // character name
  "{tribeName}": "?", // tribe name
  "{tribeId}": "?", // tribe id
  "{steamId}": "?", // steam id
  "{playerId}": "?" // player id (vernacular id)
}
```

## Chat commands

Chat commands are defined in the `chatCommands` attribute

Structure:

```jsonc
"chatCommands": {
  "/players": { // command name
    "scope": "map", // scope of the command, "map" or "player"
    "format": "{charName}", // the format for each player entry
    "delimiter": ", ", // the text that joins each player entry
    "reply": "Players Online:\n{format}", // the reply format, "{format}" is the formatted entry
    "author": "Sinfuls [RXP] Cluster", // reply author
    "responseType": "ClientChat", // response type, "ClientChat", "ServerChat" or "Notification"
    "permissions": ["Default"], // permission group that is allowed to use the command
    "defaultResponse": "No Players Online", // response if nobody is there
    "aliases": ["/online", "/who"] // command aliases
  }
}
```

## RCON commands

RCON commands are defined in the `rconCommands` attribute

The commands can then be access by doing `PlayerInfo.<command>`

Structure:

```jsonc
"rconCommands": {
  "getAllPlayerInfos": { // command name
    "arguments": [], // arguments, only accepts "{steamId}" for now
    "scope": "map", // scope of the command
    "format": "{\"charName\": \"{charName}\", \"steamId\": \"{steamId}\", \"tribeName\": \"{tribeName}\", \"tribeId\": \"{tribeId}\", \"playerId\": \"{playerId}\"}", // the format for each player entry
    "formatType": "json", // "json" or "text", allows for JSON structure
    "delimiter": ", ",
    "reply": "[{format}]\n\n",
    "defaultResponse": "No Players Online"
  }
}
```
