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
  [█████░░░░░░░░░] 200 / 100 LEVEL
---------------------------------------------------------------------------------------------
### 💪 Buff System
- Includes 18 default buffs (damage, defense, stamina, health regen, etc).
- Fully open-source buffs.lua.
- Supports buff multipliers for higher prestige levels.
- Optional on-screen Buff HUD:
- Dynamic progress bars for each buff until maxed out.
- Fully configurable in config.lua.
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
---------------------------------------------------------------------------------------------
## 🔧 Exports System Server Side

| **Export Name**         | **Type**        | **Description**                                   | **Arguments**                 | **Returns / Notes**                  | **Example Usage (Client)**                                                              |
| ----------------------- | --------------- | ------------------------------------------------- | ----------------------------- | ------------------------------------ | --------------------------------------------------------------------------------------- |
| `SaveProgress_cl`       | Modifier        | Sends current points/level to server for saving   | `identifier`                  | none                                 | `exports["mobz-prestiged"]:SaveProgress_cl(identifier)`                                 |
| `AddKill_cl`            | Modifier        | Adds a kill or NPC kill locally                   | `identifier, isNpc`           | none                                 | `exports["mobz-prestiged"]:AddKill_cl(identifier, false)`                               |
| `AddDeath_cl`           | Modifier        | Adds a death and resets killstreak                | `identifier`                  | none                                 | `exports["mobz-prestiged"]:AddDeath_cl(identifier)`                                     |
| `UnlockAchievement_cl`  | Modifier        | Unlocks achievement locally                       | `identifier, achievementName` | none                                 | `exports["mobz-prestiged"]:UnlockAchievement_cl(identifier, "first_blood")`             |
| `UnlockTitle_cl`        | Modifier        | Unlocks a title locally                           | `identifier, titleName`       | none                                 | `exports["mobz-prestiged"]:UnlockTitle_cl(identifier, "champion")`                      |
| `SetMugshot_cl`         | Modifier        | Sets the mugshot image locally                    | `identifier, mugshot`         | none                                 | `exports["mobz-prestiged"]:SetMugshot_cl(identifier, "hero.png")`                       |
| `AddBuff_cl`            | Modifier        | Adds a buff with optional label                   | `identifier, buffName, label` | none                                 | `exports["mobz-prestiged"]:AddBuff_cl(identifier, "speed", "Speed Boost")`              |
| `RemoveBuff_cl`         | Modifier        | Removes a buff locally                            | `identifier, buffName`        | none                                 | `exports["mobz-prestiged"]:RemoveBuff_cl(identifier, "speed")`                          |
| `ClearBuffs_cl`         | Modifier        | Clears all buffs locally                          | `identifier`                  | none                                 | `exports["mobz-prestiged"]:ClearBuffs_cl(identifier)`                                   |
| `SetPrestige_cl`        | Modifier        | Sets prestige locally                             | `identifier, prestige`        | none                                 | `exports["mobz-prestiged"]:SetPrestige_cl(identifier, 2)`                               |
| `GetLevel_cl`           | Getter          | Returns local level                               | `identifier`                  | `number`                             | `local lvl = exports["mobz-prestiged"]:GetLevel_cl(identifier)`                         |
| `GetPoints_cl`          | Getter          | Returns local points                              | `identifier`                  | `number`                             | `local pts = exports["mobz-prestiged"]:GetPoints_cl(identifier)`                        |
| `GetKills_cl`           | Getter          | Returns local kills                               | `identifier`                  | `number`                             | `local kills = exports["mobz-prestiged"]:GetKills_cl(identifier)`                       |
| `GetNpcKills_cl`        | Getter          | Returns local NPC kills                           | `identifier`                  | `number`                             | `local npckills = exports["mobz-prestiged"]:GetNpcKills_cl(identifier)`                 |
| `GetDeaths_cl`          | Getter          | Returns local deaths                              | `identifier`                  | `number`                             | `local deaths = exports["mobz-prestiged"]:GetDeaths_cl(identifier)`                     |
| `GetKillstreak_cl`      | Getter          | Returns local killstreak                          | `identifier`                  | `number`                             | `local streak = exports["mobz-prestiged"]:GetKillstreak_cl(identifier)`                 |
| `GetAchievements_cl`    | Getter          | Returns local achievements table                  | `identifier`                  | `table`                              | `local ach = exports["mobz-prestiged"]:GetAchievements_cl(identifier)`                  |
| `GetTitles_cl`          | Getter          | Returns local titles table                        | `identifier`                  | `table`                              | `local titles = exports["mobz-prestiged"]:GetTitles_cl(identifier)`                     |
| `GetMugshot_cl`         | Getter          | Returns local mugshot                             | `identifier`                  | `string`                             | `local img = exports["mobz-prestiged"]:GetMugshot_cl(identifier)`                       |
| `GetPlayerVisuals_cl`   | Getter          | Returns active foot effects and killstreak labels | `identifier`                  | `table` with `{activeEffect, label}` | `local visuals = exports["mobz-prestiged"]:GetPlayerVisuals_cl(identifier)`             |
| `GetLevelMultiplier_cl` | Utility / Async | Requests dynamic multiplier from server           | `factor, callback(mult)`      | `number` via callback                | `exports["mobz-prestiged"]:GetLevelMultiplier_cl(0.05, function(mult) print(mult) end)` |

---------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------
## 🔧 Exports System Client Side

| Export                                              | Arguments              | Returns | Description                                             |
| --------------------------------------------------- | ---------------------- | ------- | ------------------------------------------------------- |
| `AddPoints_cl(identifier, amount)`                  | string, number         | nil     | Add XP to a player (syncs to server).                   |
| `RemovePoints_cl(identifier, amount)`               | string, number         | nil     | Remove XP from a player (syncs to server).              |
| `SetLevel_cl(identifier, level)`                    | string, number         | nil     | Set player level directly (syncs to server).            |
| `SaveProgress_cl(identifier)`                       | string                 | nil     | Save current player progression to server.              |
| `AddKill_cl(identifier, isNpc)`                     | string, bool           | nil     | Add kill for player or NPC, updates killstreak locally. |
| `AddDeath_cl(identifier)`                           | string                 | nil     | Add death and reset killstreak locally.                 |
| `UnlockAchievement_cl(identifier, achievementName)` | string, string         | nil     | Unlock a specific achievement locally.                  |
| `UnlockTitle_cl(identifier, titleName)`             | string, string         | nil     | Unlock a specific title locally.                        |
| `SetMugshot_cl(identifier, mugshot)`                | string, string         | nil     | Set a custom mugshot locally.                           |
| `AddBuff_cl(identifier, buffName, label)`           | string, string, string | nil     | Add a buff to player locally.                           |
| `RemoveBuff_cl(identifier, buffName)`               | string, string         | nil     | Remove a buff locally by name.                          |
| `ClearBuffs_cl(identifier)`                         | string                 | nil     | Clear all buffs locally.                                |
| `SetPrestige_cl(identifier, prestige)`              | string, number         | nil     | Set player prestige locally.                            |
| `GetLevel_cl(identifier)`                           | string                 | number  | Returns player level locally.                           |
| `GetPoints_cl(identifier)`                          | string                 | number  | Returns player points locally.                          |
| `GetKills_cl(identifier)`                           | string                 | number  | Returns player kills locally.                           |
| `GetNpcKills_cl(identifier)`                        | string                 | number  | Returns player NPC kills locally.                       |
| `GetDeaths_cl(identifier)`                          | string                 | number  | Returns player deaths locally.                          |
| `GetKillstreak_cl(identifier)`                      | string                 | number  | Returns current killstreak locally.                     |
| `GetAchievements_cl(identifier)`                    | string                 | table   | Returns unlocked achievements locally.                  |
| `GetTitles_cl(identifier)`                          | string                 | table   | Returns unlocked titles locally.                        |
| `GetMugshot_cl(identifier)`                         | string                 | string  | Returns mugshot path locally.                           |
| `GetPlayerVisuals_cl(identifier)`                   | string                 | table   | Returns foot effects + killstreak label locally.        |

