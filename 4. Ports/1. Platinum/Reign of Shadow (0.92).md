# Reign of Shadow (0.92)

![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot001.jpg)

## Summary

- Name: **Reign of Shadow**
- Author(s): **Freiik, SpiKe.**
- Version: **0.92**
- Year Released: **2006**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/)

## Includes

- Cactus Platform (1.10)
- Reign of Shadow (0.92)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Reign of Shadow (0.92)`** that launches
  **`Game.exe`**.

## Known Issues

- None

## Porting Fixes

- The mod will normally force save to the **`save\Reign of Shadow\`** directory.
  However, I've edited the **`PlugY.ini`** and changed **`ActiveSavePathChange`**
  to **`0`**, which allows Cactus to manage the folder.
- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`PatchD2gfxDll.exe`** included in **`PlugY 9.00`** to patch the
  **`D2gfx.dll`** on **`1.10`**. Once that was done, I re-wired the dll loading
  so that PlugY loads **`D2Mod.dll`** from **`PlugY.ini`**, and removed
  **`PlugY.dll`** from being loaded from the **`D2Mod.ini`**. These changes allowed
  the mod to work. Using the [D2gfx.dll](https://www.moddb.com/mods/reign-of-shadow/downloads/reign-of-shadow-d2gfxdll)
  uploaded at that link caused PlugY not to load 100% correctly and thus I received
  an **Unknown Failure** error when launching the character.
- Removed the **`glide3x.dll`** that was included in the package. This protects
  the user from losing their own **`glide3x.dll`** if they have one, and also
  fixes the following access violations at program exit:
 
	- **`An exception (C000000D) occurred during DllEntryPoint or DllMain in module: C:\Games\Diablo II\glide3x.dll`**
	- **`UNHANDLED EXCEPTION: An invalid parameter was passed to a service or function (c000000d)`**

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Reign of Shadow](http://ros.freiik.de/)
- [Reign of Shadow - Mod DB](https://www.moddb.com/mods/reign-of-shadow/downloads/reign-of-shadow-092)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Reign_of_Shadow_0.92/screenshots/Screenshot010.jpg)

## Patch Notes

```
Content Patch 0.92 for Reign of Shadow - Diablo 2 Modification. Download
Instructions, Changelog and additional Information can be found on our Discord
discord.gg/wM9WjyYRS6.

Patch Notes 0.92

General:
- Improved the descriptions for cube components, providing better clarity
- Implemented different colors for low, mid, high, and uber runes to enhance the recognition speed
- Removed the German language option
- Fixed a bug where the Ureh event could stop if you were too far away from the boss

Items:
- Fixed an issue where Ammuit Clan Ring and Ennead Clan Ring were not dropping
- Fixed an issue where Unique quivers were not dropping
- Added rare quivers to the drop pool
- Adjusted Cowset Bonus Aura to function as an oskill
- Decreased the overall droprates to reduce screen clutter
- Reduced elemental pierce on items by approximately 30%
- Decreased maximum elemental resistance on items by approximately 25%
- Decreased curse resistance on items by approximately 25%
- Decreased absorb attribute on items by approximately 25%

Monsters:
- Lowered monster resistances in Hell difficulty, making 95% of all monsters pierceable
- Increased the difficulty of Diablo Clone- Brutality can no longer drop the Hellfire Torch.
- Brutality now drops a new charm called "Obliterius"

Runewords:
- Introduced tiered gemwords for runewords that were originally crafted with 2 chipped gems:
Example Runeword:
Tier 1: Crafted with 2 Chipped Sapphires
Tier 2: Crafted with 2 Flawed Sapphires
Tier 3: Crafted with 2 Sapphires
Tier 4: Crafted with 2 Flawless Sapphires
Tier 5: Crafted with 2 Perfect Sapphires
- Added two new gemwords: Strife and Struggle
Strife: Crafted by inserting 2 Perfect Skulls into Gloves
Struggle: Crafted by inserting 2 Perfect Amethysts into Gloves

Characters:

Barbarian:
- Fixed an issue with Barb Iron Skin's Damage Reduction calculation (without %)
- Declaration of War: Reduced base damage by approximately 30%
- Declaration of War: Increased synergies from 8% to 10%
- War Cry: Increased base damage by 15%
- Fury of Ancients: Increased damage by 10%, synergies from 12 to 14
- Tomahawk Rain: Increased synergies from 6 to 12
- Tomahawk Rain: Slightly increased hit range
- Splintershot: Slightly increased hit range

Sorceress:
- Increased life gained per vitality from 8 to 10
- Fixed Ice Bolt Synergy for Blizzard
- Fixed Ice Blast Synergy for Frozen Orb
- Fireball: Increased damage by 20%
- Metroid Hail: Increased physical damage by 50% and fire damage by 30%
- Meteor: Increased physical damage by 50% and fire damage by 30%
- Lightning: Increased damage by 20%

Assassin:
- Fixed an issue with Hail of Arrow Synergy not functioning correctly
- Psychic Hammer: Increased base damage by 30%
- Mind Blast: Increased base damage by 15%
- Dragon Talon: Now utilizes kick damage again

Druid:
- Increased life gained per vitality from 8 to 10
- Shock Wave: Increased base damage by 30%

Paladin:
- Fist of the Heavens (FoH): Nerfed base lightning damage by approximately 20%
- FoH: Reduced synergies from 15 to 10
- Shield Toss: Increased synergies from 12 to 18
- Blessed Hammer: Increased synergies from 12 to 18
- Hammer Rain: Increased synergies from 5 to 12
- Divine Wrath: Increased base damage by 35%
- Scattering Javelin: Decreased base damage in endgame by approximately 25%
- Purifying Javelin: Adjusted base damage, decreased base damage in endgame by approximately 15%
- Iced Javelin: Adjusted base damage, decreased base damage in endgame by approximately 15%
- Conviction: Reduced base resistances from 25 to 15, decreased resistances gained per soft point from 2 to 1, and per hard point from 5 to 3

Necromancer:
- Increased life gained per vitality from 8 to 10
- Poison Spawn: Increased damage by approximately 50%
- Bone Spirit: Increased base physical damage by approximately 30% and base magic damage by approximately 15%
- Soul Ablaze: Increased damage by approximately 50%
- Eviscerate: Increased magic damage by approximately 40%
- Lower Resist: Reduced base resistances from 25 to 15

Skills:
- Lightning, Poison, Fire, and Cold Conviction: Reduced base resistances from 25 to 15, decreased resistances gained per level from 5 to 3.

Abyss:
- Increased the area level by 5
- Raised monster levels by 3-5
- Monsters have increased life, damage, and experience points

Desert of Oblivion:
- Replaced the 3 keys with the Key of War, Key of Bones, and Key of Gluttony
- Key of War can be cubed with the 4 Boss Souls (Andariel, Mephisto, Diablo, Baal)
- Key of Bones can be found from the Master of the Dark Arts in Sewers Level 2 - Act 3
- Key of Gluttony can be cubed with the 4 symbols found in the Grotto Level 2 - Act 1

New (Old) Uber Pandemonium Tristram:

Disclaimer: There is a bug that can sometimes occur, so it is recommended to save the character before opening the level to avoid losing the cube components.

- Cube the 3 Pandemonium keys to open the uber event in Act 5
- Key of Destruction can be found from Nihlathak in Act 5
- Key of Hate can be found from The Summoner in Act 2
- Key of Terror can be found from Countess in Act 1
```
