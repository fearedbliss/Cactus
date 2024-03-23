# Le Royaume des Ombres (5.03)

![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot002.jpg)

## Summary

- Name: **Le Royaume des Ombres (The Realm of Shadows)**
- Author(s): **Xaphan**
- Version: **5.03**
- Language(s): **French (Français), English, Chinese (中文)**
- Year Released: **2013**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/)

## Includes

- Cactus Platform (1.10)
- Le Royaume des Ombres (5.00)
- Le Royaume des Ombres (5.03 Update)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Le Royaume des Ombres (5.03)`** that
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
- Since Cactus isn't responsible for applying patch updates from multiple MPQ
  files, I've merged the **`Patch_LrdO.mpq`** into **`LrdO.mpq`**, and that
  worked perfectly since we have no unknown files. Thanks for providing the
  listfiles, Xaphan. Much appreciated!

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [LRdO 5.00 - Mod DB](https://www.moddb.com/mods/le-royaume-des-ombres/downloads/full-le-royaume-des-ombres-500)
- [LRdO 5.03 Update - Mod DB](https://www.moddb.com/mods/le-royaume-des-ombres/downloads/update-le-royaume-des-ombres-503)
- [LRdO 5.03 - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=184&t=61161)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Le_Royaume_des_Ombres_5.03/screenshots/Screenshot010.jpg)

## Patch Notes

```
Playability :
* Using a town portal now send the player to the last town he has visited (and no more to a specified town depending where the player opened the portal)
* Last town visited is now saved separatly for each difficulty

Translation
* Updated chinese translation by Cai_Miao

Bugfixes :
* Fixed a bug where last row in Belt UI got drawn at wrong place
* Fixed a bug that allowed player to open locked chests without keys
* Fixed a bug that sometime prevented the player to open a chest when he had keys in his inventory
* Fixed a bug preventing the mod to work correctly under Windows XP
```