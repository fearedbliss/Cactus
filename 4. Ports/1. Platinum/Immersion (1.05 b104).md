# Immersion (1.05 b104)

![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot001.jpg)

## Summary

- Name: **Immersion**
- Author(s): **Demon9ne**
- Version: **1.05 b104**
- Year Released: **2009**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/)

## Includes

- Cactus Platform (1.10)
- Immersion (1.05 b104)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Immersion (1.05 b104)`** that launches
  **`Game.exe`**, with the flags set to **`-mod Immersion`**.

## Notes

- This mod only has two classes available in this build: **Barb**, and **Sorc**.
  I wasn't able to find the files for newer builds that have **Necro**, and
  potentially others.

## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism for both
  DLLS, and custom MPQs. Luckily, since this mod works with 1.10, I was able to
  use **D2Mod** for both of these purposes. I first used the **`D2ModSetup.bat`**
  included in **`D2Mod102`** to patch the **`D2gfx.dll`** on **`1.10`** so that
  it loads **`D2Mod.dll`**. Once that was done, I rewired as follows:
	- Added a **`Immersion.ini`** file that will be used by **D2Mod** to load
	  the required DLLs and MPQs.
	- Added **`PlugY.dll`** to the **`Immersion.ini`** at the first position.
	- Added **`D2Immersion.dll`** to the **`Immersion.ini`**.
	
	Once this D2Mod loads this file and its corresponding DLLs, it will properly
	load **`Immersion.mpq`**, **`Immpatch.mpq`**, PlugY files, and anything else
	needed.
- The mod already includes a full implementation of **PlugY 9.00** built into
  its MPQs.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Immersion - Mod DB](https://www.moddb.com/mods/immersion)
- [Immersion v1.05 b1.04 - Mod DB](https://www.moddb.com/games/diablo-2-lod/addons/d2se-immersion-v105-b104-sfx)
- [Immersion Returns - Updated 02.11.2013 - v1.05b b1.05e (Not Available)](https://d2mods.info/forum/viewtopic.php?f=5&t=57234&hilit=Immersion)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Immersion_1.05_b104/screenshots/Screenshot010.jpg)