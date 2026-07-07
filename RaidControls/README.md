# RaidControls

- Restrict what can be done during PVP
- Block structure placements
- Block weapon equips
- Block chat command usage
- Block teleports
- Block map transfers
- Block tribe state changes

---

- Console:
```text
rc.reload - reloads the config
```

- Chat:
```text
/rc.reload - reloads the config (admins only)
/currentweapon - gives you the current weapon that you're equipping for configuration (admins only)
/pvpstatus - tells you how long till your PVP restrictions are lifted
/dropstatus - tells you how drop control is affecting you
```

---

# Configuration
```jsonc
{
  "dropControl": {
    "enabled": true, // enables drop controls, allows prevention of popcorn spoiling
    "count": 5,
    "interval": 2,
    "intervalUnit": "minutes" // seconds, minutes, hours
  },
  "blocks": {
    "enabled": true, // enables feature blocks
    "commands": [ // chat commands
      "/bags" 
    ],
    "structures": [ // structures, you can search for the item bp online and paste it in
      "Blueprint'/Game/Mods/AwesomeTeleporters/Blueprints/Teleporter/PrimalItem_AwesomeTeleporters_Teleporter.PrimalItem_AwesomeTeleporters_Teleporter'"
    ],
    "weapons": [ // weapons, you can search fore the item bp online and paste it in, or use /currentweapon
      "Blueprint'/Game/ScorchedEarth/WeaponWhip/PrimalItem_WeaponWhip.PrimalItem_WeaponWhip'"
    ],
    "teleports": { // blocks tps, AwesomeTeleporters can be blocked using this to prevent exploitative PVP stuff
      "dino": true,
      "player": false
    },
    "tribe": { // prevent people from leaving or join tribes to bypass the restrictions
      "join": true,
      "leave": true
    },
    "transfers": { // block people from transferring out of the map with all their stuff
      "out": true
    },
    "notification": { // notification settings
      "enabled": true,
      "duration": 10,
      "durationUnit": "seconds",
      "size": 2,
      "color": {
        "red": 1,
        "green": 0,
        "blue": 0,
        "alpha": 1
      }
    }
  }
}
```