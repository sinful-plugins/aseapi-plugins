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
Read [explaination](https://github.com/sinful-plugins/aseapi-plugins/blob/main/PlayerInfo/config.explained.jsonc)