# XP System with Dynamic UI Bar

## Overview
This script adds an XP (Experience Points) system for players in a FiveM server.
It includes a customizable and dynamically colored XP progress bar displayed on the UI, 
which updates as the player gains XP.

A complete **Prestige, XP, Level, and Buff System** for FiveM.  
Standalone, fully customizable, and compatible with **QB-Core, ESX, Ox_Inventory**.  
Includes **dynamic XP/UI bars, 200 prestige badges, 18 buffs, rewards, killstreaks, mugshot UI, Discord logs, admin tools, leaderboards, and OpenIV texture support.**


# ⚔️ Mobz Prestiged & XP Progression System

## 🎯 Features
---------------------------------------------------------------------------------------------
### 🎨 Dynamic XP & Prestige UI
- Toggleable Prestige UI via keybind (default `E`).
- Points and level progress stored in **oxmysql / server-side DB**.
- Dynamic color and animations based on level.
- Smooth incremental XP animation with level-up popups.
- Fully configurable in `config.lua`:
- UI size, colors, position, animation duration.
- Enable/disable level-up pop

  🛡️ Level 2
  [█████░░░░░░░░░] 200 / 250 POINTS

<img width="294" height="39" alt="b1" src="https://github.com/user-attachments/assets/e42a1503-4417-47fb-a100-5b5315df9dcd" />
<img width="299" height="52" alt="b2" src="https://github.com/user-attachments/assets/a7270b7d-efcd-4522-a5d1-0a5e3b293c36" />
<img width="304" height="53" alt="b3" src="https://github.com/user-attachments/assets/2860a7a7-c509-4c6f-afd5-184589ce8f4c" />


  ![2025-10-0613-45-29-ezgif com-video-to-gif-converter (2)](https://github.com/user-attachments/assets/54f9d95b-7427-4a7b-b7a7-be3606657733)

---------------------------------------------------------------------------------------------
### 💪 Buff System
- Includes 18 default buffs (damage, defense, stamina, health regen, etc).
- Fully open-source buffs.lua.
- Supports buff multipliers for higher prestige levels.
- Optional on-screen Buff HUD:
- Dynamic progress bars for each buff until maxed out.
- Fully configurable in config.lua.
- 	| Buff Name                	| Max Effect | What It Does                                                | Balance Check  |
	| ------------------------ 	| ---------- | ----------------------------------------------------------	| -------------- |
	| 🏊 **Swimming**          | 1.5x       | Swim up to 50% faster. Useful for escapes/diving.         | ✅ Balanced     |
	| 🏃 **Running**           	| 1.5x       | Sprint 50% faster. Big advantage in chases, but fair.     | ✅ Fair         |
	| ❤️ **Health Regen**      | 1.25x      | Slightly quicker healing, not instant. Keeps fights tense. | ✅ Safe         |
	| 🕵️ **Stealth**           	| 1.5x       | Reduced footstep noise. Sneakier, not invisible.           | ✅ Balanced     |
	| 💪 **Strength**          | 2.0x       | Unarmed punches deal double damage at best.                | ✅ Fair         |
	| 🦘 **Super Jump**        | 1.6x       | Jump higher to reach ledges. No “flying.”                  | ✅ Fun but safe |
	| 💨 **Stamina**           | 1.5x       | Run longer without tiring.                                 | ✅ Fair         |
	| 🔥 **Fire Resistance**   	| 1.5x       | Take less fire damage.                                     | ✅ Balanced     |
	| 💥 **Explosion Resist.** 	| 1.5x       | Take less damage from explosions.                          | ✅ Balanced     |
	| 🛡 **Melee Resistance**  	| 1.5x       | Take less melee damage.                                    | ✅ Balanced     |
	| 🪓 **Melee Damage**      | 1.5x       | Melee swings deal 50% more damage.                         | ✅ Balanced     |
	| 🔫 **Weapon Damage**     | 1.15x      | Guns deal up to 15% more damage.                           | ✅ Very fair    |
	| 🛡 **Weapon Defense**    	| 1.5x       | Reduce incoming gun damage.                                | ✅ Balanced     |
	| 🥋 **Melee Defense**     | 1.5x       | Reduce incoming melee damage.                              | ✅ Balanced     |
	| 🚗 **Vehicle Armor**     | 1.5x       | Cars take less damage.                                     | ✅ Balanced     |
	| 🚙 **Vehicle Handling**  | 1.3x       | Vehicles grip/corner better.                               | ✅ Balanced     |
	| 🏎 **Vehicle Speed**     	| 1.2x       | Cars go slightly faster (20% max).                         | ✅ Fair         |


	🏁 Final Verdict

	Strong but not OP – rewards grinding without breaking PvP.
	Safe caps prevent godmode or broken vehicles.
	Perfect mix of fun + balance.

---------------------------------------------------------------------------------------------
## 🎁 Rewards System
- Open-source `rewards.lua` with optional reward tiers.

**Supports:
- qb-core
- esx
- qb-inventory
- ox_inventory
- standalone
- ox_lib
** Configure unique prestige rewards (items, money, weapons, XP, etc).
---------------------------------------------------------------------------------------------
## ⏱️ Playtime Rewards
- Optional system to reward prestige points over time.
- Uses oxmysql to save player playtime.
- Configurable interval + reward amounts.
---------------------------------------------------------------------------------------------
## ⚔️ Killstreaks & Deaths
**Gain prestige points from:
- NPC kills
- Player kills

**Deaths (optional)
- Killstreak Titles:
- Unique names with colors.

**Feet Effects:
- Glowing synced effects on both feet.
- Different colors for different streaks.
- Fully synced so all players see them.
---------------------------------------------------------------------------------------------
## 📸 Mugshot UI
- Displays a custom UI when a player achieves a killstreak.

**Shows:
- Player’s name.
- Current killstreak title.
- A real-time mugshot of the player’s head.
- Broadcasts to all players for a short duration.
---------------------------------------------------------------------------------------------
## 🪵 Discord Logs
- Sends prestige updates, rewards, and killstreaks to Discord via webhooks.
- Fully configurable.
---------------------------------------------------------------------------------------------
## 🛡️ Prestige Badges
- Preconfigured 200 prestige badges (prestiged1 → prestiged200).
- Stored inside a .ypt texture dictionary.
- Synced badge display above players’ heads.
- Configurable animations, styles, and positioning.
- Roman numeral level display support.
<img width="1135" height="560" alt="fulllist1" src="https://github.com/user-attachments/assets/33b64d70-961c-4b7b-8982-d028218a50d1" />

- <img width="1146" height="422" alt="fulllist2" src="https://github.com/user-attachments/assets/cde29ab6-2023-4821-bf66-f40da368637b" />

---------------------------------------------------------------------------------------------
## 🛠️ Admin Management
- Admin panel to:
- Add/remove points.
- Set prestige level.
- Reset players.
- Manage buffs/rewards.
- Permission system configurable in config.lua.
---------------------------------------------------------------------------------------------
## 🏆 Leaderboards
- Prestige leaderboard using ox_lib menu.
- Shows top players with level, points, and badges.
- Dynamically updates.
---------------------------------------------------------------------------------------------
## 🗄️ oxmysql Support
- Automatically saves/loads prestige points and levels.
- Playtime and rewards also stored in the database.
---------------------------------------------------------------------------------------------
## 🌍 Full Sync
- Server-side broadcasting ensures all prestige levels, 
- buffs, and badges are always synced across all players.
---------------------------------------------------------------------------------------------
## 🏗️ Developer Notes
- Fully standalone, but supports QB-Core, ESX, and Ox_Inventory.
- Easy to expand with new buffs, rewards, or badges.
- buffs.lua and rewards.lua are intentionally open for customization.
- Badges (prestiged1 → prestiged200) can be extended by adding new entries in your .ypt.
---------------------------------------------------------------------------------------------


# 🏆 Mobz-Prestiged Documentation

---------------------------------------------------------------------------------------------

## 📑 Table of Contents

1. [Server Exports](#server-exports-reference)

   * [Core Data Functions](#core-data-functions)
   * [Basic Getters](#basic-getters)
   * [Modifiers](#modifiers)
   * [Buff System](#buff-system)
   * [Achievements & Titles](#achievements--titles)
   * [Visuals & Prestige Info](#visuals--prestige-info)
   * [Multipliers](#multipliers)
   * [Leaderboards](#leaderboards)
   * [Online / Offline Data](#online--offline-data)
   * [Saving Progression](#saving-progression)
   * [Developer Tips](#developer-tips)
2. [Client Exports](#client-exports-reference)

   * [Core Data Functions](#core-data-functions-1)
   * [Stats Getters](#stats-getters)
   * [Stats Modifiers](#stats-modifiers)
   * [Buff System](#buff-system-1)
   * [Visuals & Effects](#visuals--effects)
   * [Multipliers](#multipliers-1)
   * [Data Sync](#data-sync)
   * [Developer Tips](#developer-tips-1)
3. [License](#license)

---------------------------------------------------------------------------------------------

# 📡 Server Exports Reference

Below is a full list of server-side exports available through:

```lua
exports["mobz-prestiged"]:ExportName(...)
```

---------------------------------------------------------------------------------------------

## 🧠 Core Data Functions

### ✅ EnsurePlayerDataServer(identifier)

Ensures a player's data exists and returns it (used internally).

```lua
local data = exports["mobz-prestiged"]:GetLevel_sv("steam:110000112345678")
print(data.level)
```

---------------------------------------------------------------------------------------------

## 🧾 Basic Getters

| Export                                | Description                           | Returns  |
| ------------------------------------- | ------------------------------------- | -------- |
| `GetLevel_sv(identifier)`             | Returns player’s current level        | `number` |
| `GetPoints_sv(identifier)`            | Returns total points                  | `number` |
| `GetKills_sv(identifier)`             | Returns total player kills            | `number` |
| `GetNpcKills_sv(identifier)`          | Returns total NPC kills               | `number` |
| `GetDeaths_sv(identifier)`            | Returns total deaths                  | `number` |
| `GetKillstreak_sv(identifier)`        | Returns current killstreak            | `number` |
| `GetPrestige_sv(identifier)`          | Returns prestige rank                 | `number` |
| `GetPlaytime_sv(identifier)`          | Total playtime in seconds             | `number` |
| `GetPlaytimeFormatted_sv(identifier)` | Returns formatted playtime as `HH:MM` | `string` |

**Example:**

```lua
local kills = exports["mobz-prestiged"]:GetKills_sv(identifier)
print(("Player has %d kills"):format(kills))
```

---------------------------------------------------------------------------------------------

## ⚔️ Modifiers

| Export                                 | Description                                  |
| -------------------------------------- | -------------------------------------------- |
| `AddKill_sv(identifier, isNpc)`        | Adds a kill to either player or NPC category |
| `AddDeath_sv(identifier)`              | Adds a death and resets killstreak           |
| `SetPrestige_sv(identifier, prestige)` | Sets prestige and updates labels/icons       |

**Example:**

```lua
local id = GetPrimaryIdentifier(source)
exports["mobz-prestiged"]:AddKill_sv(id, false)
exports["mobz-prestiged"]:AddDeath_sv(id)
exports["mobz-prestiged"]:SetPrestige_sv(id, 2)
```

---------------------------------------------------------------------------------------------

## 🧪 Buff System

| Export                                    | Description                     |
| ----------------------------------------- | ------------------------------- |
| `AddBuff_sv(identifier, buffName, label)` | Adds a buff with optional label |
| `RemoveBuff_sv(identifier, buffName)`     | Removes a specific buff         |
| `ClearBuffs_sv(identifier)`               | Removes all buffs               |

**Example:**

```lua
local id = GetPrimaryIdentifier(source)
exports["mobz-prestiged"]:AddBuff_sv(id, "damage_boost", "🔥 Damage Boost")
exports["mobz-prestiged"]:RemoveBuff_sv(id, "damage_boost")
```

---------------------------------------------------------------------------------------------

## 🏅 Achievements & Titles

| Export                                          | Description                   |
| ----------------------------------------------- | ----------------------------- |
| `UnlockAchievement_sv(identifier, achievement)` | Unlocks specific achievement  |
| `UnlockTitle_sv(identifier, title)`             | Unlocks a title               |
| `GetAchievements_sv(identifier)`                | Returns all achievements data |
| `GetTitles_sv(identifier)`                      | Returns all unlocked titles   |

**Example:**

```lua
local id = GetPrimaryIdentifier(source)
exports["mobz-prestiged"]:UnlockAchievement_sv(id, 5)
exports["mobz-prestiged"]:UnlockTitle_sv(id, "Elite Slayer")

local achievements = exports["mobz-prestiged"]:GetAchievements_sv(id)
for lvl, data in pairs(achievements) do
    print(("Achievement %s: %s"):format(lvl, data.unlocked and "Unlocked" or "Locked"))
end
```

---------------------------------------------------------------------------------------------

## 👑 Visuals & Prestige Info

| Export                            | Description                                       |
| --------------------------------- | ------------------------------------------------- |
| `GetPlayerVisuals_sv(identifier)` | Returns mugshot, prestige icon, and active effect |

**Example:**

```lua
local visuals = exports["mobz-prestiged"]:GetPlayerVisuals_sv(identifier)
print(json.encode(visuals))
```

---------------------------------------------------------------------------------------------

## 🧮 Multipliers

| Export                                 | Description                                      |
| -------------------------------------- | ------------------------------------------------ |
| `GetMultiplier_sv(identifier, factor)` | Returns dynamic multiplier based on player level |

**Example:**

```lua
local id = GetPrimaryIdentifier(source)
local mult = exports["mobz-prestiged"]:GetMultiplier_sv(id, 0.02)
print("XP Multiplier:", mult)
```

---------------------------------------------------------------------------------------------

## 📊 Leaderboards

| Export                         | Sorted By             | Example Return                              |
| ------------------------------ | --------------------- | ------------------------------------------- |
| `GetTopPoints_sv(limit)`       | Points                | `{ {identifier, name, points}, ... }`       |
| `GetTopLevels_sv(limit)`       | Level                 | `{ {identifier, name, level}, ... }`        |
| `GetTopKills_sv(limit)`        | Kills                 | `{ {identifier, name, kills}, ... }`        |
| `GetTopAchievements_sv(limit)` | Achievements unlocked | `{ {identifier, name, achievements}, ... }` |

**Example:**

```lua
local topKills = exports["mobz-prestiged"]:GetTopKills_sv(5)
for _, player in ipairs(topKills) do
    print(("[%s] %s - %d kills"):format(player.identifier, player.name, player.kills))
end
```

---------------------------------------------------------------------------------------------

## 🌐 Online / Offline Data

| Export                        | Description                           |
| ----------------------------- | ------------------------------------- |
| `GetOnlinePlayersStats_sv()`  | Returns stats for all online players  |
| `GetOfflinePlayersStats_sv()` | Returns stats for all offline players |

**Example:**

```lua
local online = exports["mobz-prestiged"]:GetOnlinePlayersStats_sv()
print(json.encode(online))
```

---------------------------------------------------------------------------------------------

## 💾 Saving Progression

| Export              | Description                                                        |
| ------------------- | ------------------------------------------------------------------ |
| `SaveProgress_sv()` | Triggers manual data save (optional override for JSON persistence) |

**Example:**

```lua
exports["mobz-prestiged"]:SaveProgress_sv()
```

---------------------------------------------------------------------------------------------

## 🧰 Developer Tips

* Always ensure `GetPrimaryIdentifier(source)` returns valid identifiers (`steam:`, `license:`, etc.).
* Use `EnsurePlayerDataServer` only internally.
* Hook this system with your own XP/leveling logic and UI displays.
* Add persistence by implementing JSON saving in `SaveProgression()`.

---------------------------------------------------------------------------------------------

# 📡 Client Exports Reference

Below is a full list of client-side exports available through:

```lua
exports["mobz-prestiged"]:ExportName(...)
```

---------------------------------------------------------------------------------------------

# 🏆 Mobz-Prestiged Documentation (Client Exports)

---------------------------------------------------------------------------------------------

## 📄 Client Exports Reference

Below is a full list of client-side exports available through:

```lua
exports["mobz-prestiged"]:ExportName(...)
```

---------------------------------------------------------------------------------------------

## 🧠 Core Data Functions

### ✅ EnsurePlayerDataClient(identifier)

Ensures local player data exists and initializes defaults if missing.

**Example:**

```lua
local id = GetPlayerServerId(PlayerId())
local pdata = EnsurePlayerDataClient(id)
print(pdata.level) -- prints current level
```

---------------------------------------------------------------------------------------------

## 🧾 Stats Getters

| Export                           | Description        | Returns  |
| -------------------------------- | ------------------ | -------- |
| `GetKills_cl(identifier)`        | Total player kills | `number` |
| `GetNpcKills_cl(identifier)`     | Total NPC kills    | `number` |
| `GetDeaths_cl(identifier)`       | Total deaths       | `number` |
| `GetKillstreak_cl(identifier)`   | Current killstreak | `number` |
| `GetAchievements_cl(identifier)` | Achievements table | `table`  |
| `GetTitles_cl(identifier)`       | Titles table       | `table`  |
| `GetLevel_cl()`                  | Current level      | `number` |
| `GetPoints_cl()`                 | Current points     | `number` |

**Example:**

```lua
local kills = exports["mobz-prestiged"]:GetKills_cl(identifier)
print("You have " .. kills .. " kills!")
```

---------------------------------------------------------------------------------------------

## ⚔️ Stats Modifiers

| Export                                              | Description                        |
| --------------------------------------------------- | ---------------------------------- |
| `AddKill_cl(identifier, isNpc)`                     | Adds a kill (player or NPC)        |
| `AddDeath_cl(identifier)`                           | Adds a death and resets killstreak |
| `UnlockAchievement_cl(identifier, achievementName)` | Unlocks an achievement locally     |
| `UnlockTitle_cl(identifier, titleName)`             | Unlocks a title locally            |
| `SetPrestige_cl(identifier, prestige)`              | Updates prestige level and icon    |

**Example:**

```lua
local id = GetPlayerServerId(PlayerId())
exports["mobz-prestiged"]:AddKill_cl(id, false)
exports["mobz-prestiged"]:AddDeath_cl(id)
exports["mobz-prestiged"]:UnlockAchievement_cl(id, "First Blood")
exports["mobz-prestiged"]:SetPrestige_cl(id, 2)
```

---------------------------------------------------------------------------------------------

## 🧪 Buff System

| Export                                    | Description                    |
| ----------------------------------------- | ------------------------------ |
| `AddBuff_cl(identifier, buffName, label)` | Add a buff with optional label |
| `RemoveBuff_cl(identifier, buffName)`     | Remove a buff                  |
| `ClearBuffs_cl(identifier)`               | Remove all buffs               |

**Example:**

```lua
exports["mobz-prestiged"]:AddBuff_cl(id, "speed_boost", "🏎️ Speed Boost")
exports["mobz-prestiged"]:RemoveBuff_cl(id, "speed_boost")
exports["mobz-prestiged"]:ClearBuffs_cl(id)
```

---------------------------------------------------------------------------------------------

## 👑 Visuals & Effects

### `GetPlayerVisuals_cl(playerId)`

Returns visual info like active foot effects and killstreak labels.

**Returns Table Example:**

```lua
{
    activeEffect = {
        particleDict = "core",
        particleName = "fire_trail",
        scale = 1.0
    },
    label = {
        label = "Rampage",
        color = {255,0,0},
        scale = 0.5,
        heightOffset = 2.0
    }
}
```

**Example:**

```lua
local visuals = exports["mobz-prestiged"]:GetPlayerVisuals_cl(id)
if visuals.label then
    print("Current Killstreak Label:", visuals.label.label)
end
```

---------------------------------------------------------------------------------------------

## 🧮 Multipliers

### `GetLevelMultiplier_cl(factor, callback)`

Requests a multiplier from the server based on player level.

**Example:**

```lua
exports["mobz-prestiged"]:GetLevelMultiplier_cl(0.02, function(mult)
    print("XP multiplier:", mult)
end)
```

---------------------------------------------------------------------------------------------

## 💾 Data Sync

### `mobz-prestiged:syncPlayerData`

Event used to update client data from the server.

**Example:**

```lua
RegisterNetEvent("mobz-prestiged:syncPlayerData")
AddEventHandler("mobz-prestiged:syncPlayerData", function(identifier, newData)
    print("Data synced for:", identifier)
end)
```

---------------------------------------------------------------------------------------------

## 💡 Developer Tips

* Use client exports to query or modify local data for UI or gameplay effects.
* Sync always comes from the server via `mobz-prestiged:syncPlayerData`.
* Buffs and killstreaks are purely client-side visual and gameplay effects.
* Always pass valid identifier (server ID) when using exports.

---------------------------------------------------------------------------------------------

## 📄 License

MIT License — free to use API, modify, and distribute with attribution.

💬 Credits
Developed by Mobz Development

Tebex Store: [https://mobz.tebex.io/](https://mobz.tebex.io/)

---------------------------------------------------------------------------------------------
