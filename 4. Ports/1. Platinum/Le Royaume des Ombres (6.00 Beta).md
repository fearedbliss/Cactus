# Le Royaume des Ombres (6.00 Beta)

![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot002.jpg)

## Summary

- Name: **Le Royaume des Ombres (The Realm of Shadows)**
- Author(s): **Xaphan**
- Version: **6.00 Beta**
- Language(s): **French (Français), English, Chinese (中文)**
- Year Released: **2013**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/)

## Includes

- Cactus Platform (1.10)
- Le Royaume des Ombres (6.00 Beta)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Le Royaume des Ombres (6.00 Beta)`** that
  launches **`Game.exe`**, with the flags set to **`-mod LrdO`**.

## Notes

- This mod is available in three languages, and can be easily switched between
  by changing the **`SelectedLanguage`** section in **`PlugY.ini`**. Change the
  value as follows:

	- French = **`FRA`**
	- English = **`ENG`**
	- Chinese = **`CHI`**
	
  I can't test this since I only have an English installation, and am missing
  some files. However, with the **English** installation, I was still able to
  successfully test the **French** version though.

- Do not use glide with this mod, or you may experience slowness or other
  issues. The normal DirectDraw mode should work smoothly.

## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Once that was
  done, I rewired the rest of the system by:
	- Renaming **`D2Mod.ini`** to **`LrdO.ini`**.
	- Removed **`pSpell.dll`** from **`PlugY.ini`**.
	- Added **`PlugY.dll`** to first position in **`LrdO.ini`**.
	- Added **`D2Dreamland.dll`** to second position in **`LrdO.ini`**.
	- Added **`pSpell.dll`** to third position in **`LrdO.ini`**.
- Changed default language from **French** to **English** by changing the
  **`SelectedLanguage`** from **`FRA`** to **`ENG`** in **`PlugY.ini`**.
- Removed **`glide3x.dll`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [LRdO 6.00 Beta Announcement - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=184&t=62949)
- [LRdO 6.00 Beta - Mod DB](https://www.moddb.com/mods/le-royaume-des-ombres/downloads/le-royaume-des-ombres-600-public-beta)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_6.00_Beta/screenshots/Screenshot010.jpg)

## Patch Notes

```
This BETA allows you to test version 6.00 of the mod. However, all functionnalities aren't present or completely implemented.

In this BETA, you can :
- Enjoy all 5 acts just like the current released version
- Experiment the new skills for each classes
- Experiment the new mana system
- Experiment changes to maps (cursed chests and the like)
- Experiment new generation of items
- Experiment everything else you can see in the current changelog (On the Keep)

But there is some limitations :
- You are only able to play as a Warrior, a Sorceress, a Huntress or a Necromancer
- New maps features and rework will only be done in act 1
- Unique, sets and runewords are dissabled. You can drop or craft thems but they have no stats
- Monsters are not edited (except a few)

I hope you will enjouy your playtime !
```