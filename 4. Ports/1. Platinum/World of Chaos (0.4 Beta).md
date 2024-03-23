# World of Chaos (0.4 Beta)

![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot001.jpg)

## Summary

- Name: **World of Chaos**
- Author(s): **Dav92**
- Version: **0.4 Beta**
- Language(s): **English, German (Deutsch)**
- Year Released: **2007**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/)

## Includes

- Cactus Platform (1.10)
- World of Chaos (0.4 Beta)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`World of Chaos (0.4 Beta)`** that launches
  **`Game.exe`**.

## Notes

- This mod supports the **German** language. You can rename the **`data_DEU`**
  folder to **`data`**, and add **`-direct`** to your flags. I was able to test
  that this works successfully, but the game crashed for me when I press
  **`[Esc]`** in game, most likely because my English install is missing some
  files.
  
## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Everything
  loaded properly after that.
- Added **`PlugY.dll`** at the last position of **`D2Mod.ini`**.
- Removed **PlugY** files from **`Patch_D2.mpq`**, and keeping them in the mod
  since the author has explicitly mentioned **PlugY** in the readme.
- Downgraded **PlugY** from **9.0.0** to **5.0.6**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [World of Chaos - Mod DB](https://www.moddb.com/games/diablo-2-lod/addons/d2se-world-of-chaos-04b)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/World_of_Chaos_0.4_Beta/screenshots/Screenshot010.jpg)

## Patch Notes

```
Welcome to the World of Chaos Mod for Diablo II - Lord of Destruction v1.10.
In this Mod you will play as one of the Monsters, which was at the
beginning only available as a Monster, and not as a Charakter.
```