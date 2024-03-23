# Disotheb (Hotfix 4)

![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot001.png)

## Summary

- Name: **Disotheb**
- Author(s): **erevos**
- Version: **Hotfix 4**
- Year Released: **2023**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/)

## Includes

- Cactus Platform (1.10)
- Disotheb (Full Version)
- Disotheb (Hotfix 4)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Disotheb (Hotfix 4)`** that launches
  **`Game.exe`** with the flags set to **`-3dfx`**.

## Known Issues

- The game will not work with **`cnc-ddraw`** and will crash (and/or also have
  messed up UI). It requires the use of the provided **`glide3x.dll`**.
- There is an [open bug](https://github.com/bolrog/d2dx/issues/124) with **`D2DX`**
  where screenshots cannot be taken from the game. You'll need to rely on the
  screenshot captured by Windows (and some image editing) for your screenshots.
- When playing in window mode, opening and closing UI elements will cause the
  mouse to jump outside the window.
- The help menu in game is cut off when playing below resolutions of **`1280x768`**.

Due to the above window/cursor issues, I would recommend playing on **`1280x768`**,
full screen + stretched mode, which is mostly the default, until the situation
improves in a potential future patch. If your game starts at **`1024x768`**,
make sure to adjust.
  
## Notes
  
- If you make a new Witch character and name her **`test`**, she will start at
  level 50. Originally I thought this was a bug but I think I just hit some
  a magic string. Sorry for discovering your secret, erevos :).

## Porting Fixes

This mod is ***VERY*** particulate about its set up and how things are loaded.
If any deviation is done, the game will most likely crash. Also note, that it
seems the order of how you load the dlls in **`D2Mod.ini`** matters. Which
makes sense.

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Once that was
  done, I rewired the rest of the dlls by:
	- Adding **`PlugY.dll`** to **`D2Mod.ini`** at the end of the dll load list.
	  Order matters.
- Removed the unused **`Utility.dll`** and **`CharStart.dll`** from **`D2Mod.ini`**
  and their corresponding dlls.
- Removed **`dsound.dll`** and **`dsound.ini`**. Cactus already provides
  **DSOAL w/ OpenAL Soft** which implements proper **Environmental Effects**
  support. **IndirectSound** doesn't implement it, it just fakes the feature,
  from the **`dsound.ini`**:

	```
	EAX ("Environmental Audio Extensions") is not emulated by IndirectSound.

	IndirectSound can emulate EAX support, however.
	In other words, IndirectSound will pretend that EAX is supported
	so that games using IndirectSound will think that EAX is available.
	This is useful for some games that don't calculate
	3D positional audio unless EAX is supported.

	(Actual emulation of EAX is under development
	but is not yet ready to release.)
	```
- Fixed main menu mod name by changing **`VersionText`** from 
  **`Escape from the Afterlife`** to **`Disotheb`** in **`PlugY.ini`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Disotheb - Full Version](https://www.moddb.com/mods/disotheb/downloads/disotheb-full-version)
- [Disotheb - Hotfix 4](https://www.moddb.com/mods/disotheb/downloads/disotheb-hotfix-4-includes-previous-hotfixes)

## Screenshots

![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot002.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot003.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot004.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot005.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot006.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot007.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot008.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot009.png)
![](https://xyinn.org/diablo/platforms/gold/Disotheb_Hotfix_4/screenshots/Screenshot010.png)

## Patch Notes

```
Hotfix 4
-------------
Change log

    Burnblade will work with all two-handed weapons. The bug were it could work with one-handed swords is fixed.
    Hunt Dogs false description fixed
    Injuration false description fixed
    The Knave of Swords level increase of War Banner is fixed
    Rune of Turtles is fixed
    Potion of Thieves bonus now grants Souls Find 100% per 50 sec
    Injuration description fixed
    Summon Spirit Wolf now displays properly its damage.
    Fixed on Relics the high level requirement of % Faster Cast affix
    Fixed a typo on Scalp Organ
    Added info about known issues on Help Guide
    Lucky Coin will not have a chance anymore to spawn town maps
    Drop chance of Armor/Shield/Blade Pieces materials is fixed
    Bosses are now immune to their own attack element
    Bosses will not do extra damage to minions/Mercs
    Changed the colors of items like Runes, to be visible without using D2DX
    A crash caused by a Skill on a Manifestation Relic, is fixed
    Fixed Life and Damage of Spirit Wolf and Fenris. Added synergies with Minions affixes
    Shieldmaiden will give Endurance instead of Strength
    Fixed some missing strings
    Souls will again dropped by every monster
    Fixed Claws Expertise Node bonus of Attack Rating
    Afterlife Path 12 crash is corrected and the an extra dungeon entrance is added
    Electric Pulse Tower crash animation corrected
    Bug of Den of Evil Quest on Nightmare, is solved
    Magic Resist of Mechanic is corrected
    Remove Durability affix from rolling on items that don't use durability
    Remove wrong description of Goblin Swords
    Corrected several typos
    Removed Magic Resist -50 by Savager and increased his Fire/Cold/Lightning Resistance handicap to -25 (no retroactive change) - Removed Magic Resist penalty from Mechanic and added a -25 Cold Resist penalty (no retroactive change)
    Catacombs and Durance has light emitting out of blood
    KAA skill got some adjustments and he deals now Physical/Magic Damage.
    Disabled an unused Unique, enabled the right one.
    Changed the name of 7 swords having names of Staffs. Corrected their inventory sizes too
    Adjusted Inner Sight
    Increase some values on Small Relics and Relics
    Monster Bear got a Mana Cost and reduced cooldown to 5 sec
    Fire Skiachtro error of up to 3 simultaneously is fixed.
    Non-class pet skills minimum mana cost (lvl 1), increased to 50.
    Heavilly reduced the chances of a Treasure Goblin appearance at same maps. Instead they got a lot more bigger variety of breakable/chest items that they can spawn.
    A Thief Goblin item is added on the loot circle.
    Corrected calculation for Halbu prices


Full Version
-------------
Disotheb features: | 7 classes archetypes | +200 New Skills | Souls based Skill
Points System | Lifebound Items | Weight System | Healing Orbs | Life based on
Armor System | 98 New Runes – 7 Tiers each | 80 New Gems | Class Loot | New Music
| Map Enhancements | Hell difficulty as an End-Game Dungeon/Maps |
+100 New Monsters | New affixes and base item | Detailed Stats Screens | In-game
Tutorial/Help Screen | and countless gameplay changes.

Learn everything about Disotheb by pressing "H" while in-game with your first character!

Disotheb's Discord Server: https://discord.gg/kyk25j6JCb
```