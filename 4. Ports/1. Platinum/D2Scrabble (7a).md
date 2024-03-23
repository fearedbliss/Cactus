# D2Scrabble (7a)

![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot002.jpg)

## Summary

- Name: **D2Scrabble**
- Author(s): **Volf**
- Version: **7a**
- Year Released: **2009**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/)

## Includes

- Cactus Platform (1.10)
- D2Scrabble (7a)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`D2Scrabble (7a)`** that launches
  **`Game.exe`**, with the flags set to **`-mod D2Scrabble`**.

## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Once that was
  done, I rewired the rest of the system by:
	- Renaming **`D2Mod.ini`** to **`D2Scrabble.ini`**.
	- Added **`PlugY.dll`** to first position in **`LrdO.ini`**.
- Installed fresh copy of **`PlugY/`** directory from **PlugY 9.00** since
  the mod was missing these files, causing the game to crash at launch. I'm
  re-using the rest of the PlugY files provided by the mod.
- Removed **`glide3x.dll`** and **`glide-init.exe`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [D2Scrabble Subsite - PhrozenKeep](https://d2mods.info/forum/subsite/d2scrabble/)
- [D2Scrabble 7a - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=187&t=65161&hilit=scrabble+mod)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2Scrabble_7a/screenshots/Screenshot010.jpg)

## Patch Notes

```
D2 Scrabble is a diablo2 expansion mod for 1.10 patch.  The mod ads letter items
that allow you to form words in the horadric cube - Press transmute and the
words become reality.  Well That was the basic idea but eventually the mod
evolved in to a total conversion mod with loads of news skills, allot added to
the world, high res, firearms, cars, horse riding, modern cities etc.

There are tons of changes in this mod
- Ever found and dumped a lousy item with with + 1 + to a character skill. Well
  in d2 scrabble you can get a skill extractor, extract the + to x skill then
transfer it to your favorite weapon.
- Tons of new weapons and armors.
- A whole bunch of new runewords in addition to the vanilla ones.
- New gems in addition to the vanilla ones.
- Additional armor and weapon grades.
- Higher resolution.
- New sub quests.
- Npcs now pay allot more for items sold
- Characters start with cube
- Max Character level is 410
- Realm only runewords are enabled.
- You earn 10 stat points per level
- Stamina drain is greatly reduced, meaning you can keep running around until
  your sick of it!
- Mana recovery is 5 times faster than normal
- belt, gloves, charms, amulets, rings, bolts and arrows can have sockets
- Throwing potions stack up to 500
- Item compressor - pack any item in to 1x1 size container.
- Gem bag - A gembag has been added - sold by Akara
- Letter bag - A bag to store letters in - sold by Akara
- Rune bag - A bag to store runes in - sold by Akara There are loads of other
  changes to but these should be the essentials!  You can also check the
changelog for more details.
```