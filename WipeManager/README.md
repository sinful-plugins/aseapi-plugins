# WipeManager

- Allows for wiping of everything but the admin's stuff
- Good for soft wipes

---

# WipeManager Commands

- Console / RCON:

```text
wm.wipeDinos <bypass ids> - wipes dinos with tribes ids in the argument being skipped
wm.wipeStructures <bypass ids> - wipes structures with tribes ids in the argument being skipped
wm.wipeCharacters <bypass ids> - wipes characters with tribes ids in the argument being skipped
wm.wipeExcept <bypass ids> - wipes everything with tribes ids in the argument being skipped
wm.setday <day number> - sets the server's day count
```

- Chat:

```text
/wm.wipeDinos <bypass ids> - wipes dinos with tribes ids in the argument being skipped
/wm.wipeStructures <bypass ids> - wipes structures with tribes ids in the argument being skipped
/wm.wipeCharacters <bypass ids> - wipes characters with tribes ids in the argument being skipped
/wm.wipeExcept <bypass ids> - wipes everything with tribes ids in the argument being skipped
/wm.setday <day number> - sets the server's day count
```

---

# Configuration

```jsonc
{
  "destroyPerTick": 500, // number of actors to destroy per tick
  "tickInterval": 1, // tick interval in seconds
  "saveBeforeWipe": true, // save the world before wiping
  "allowedGroups": ["Admins"], // permission groups allowed to do the commands
  "ignoredGroups": ["Admins"], // tribes with these permission groups gets skipped when wiping
}
```
