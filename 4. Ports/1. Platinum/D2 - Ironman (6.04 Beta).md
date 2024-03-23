# D2: Ironman (6.04 Beta)

![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot001.jpg)

## Summary

- Name: **D2: Ironman**
- Author(s): **Hash**
- Version: **6.04 Beta**
- Year Released: **2021**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/)

## Includes

- Cactus Platform (1.10)
- D2: Ironman (6.04 Beta)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`D2 - Ironman (6.04 Beta)`** that launches
  **`Game.exe`** with the **`-direct`** flag.

## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch
  the **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**
  automatically on start up.  Once that was done, I re-wired the dlls as
  follows:
	- Added **`PlugY.dll`** as the first dll to load in **`D2Mod.dll`**. Order
	  is important.
	- Removed the **`ddraw.dll`** load line from **`D2Mod.ini`**.
- Removed the **`glide3x.dll`** that was included in the package. This protects
  the user from losing their own **`glide3x.dll`** if they have one, and also
  fixes the following access violations at program exit:

	- **`An exception (C000000D) occurred during DllEntryPoint or DllMain in module: C:\Games\Diablo II\glide3x.dll`**
	- **`UNHANDLED EXCEPTION: An invalid parameter was passed to a service or function (c000000d)`**

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [D2: Ironman](https://im.stoned.io/)
- [D2: Ironman - Mod DB](https://www.moddb.com/mods/d2-ironman)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2_Ironman_6.04_Beta/screenshots/Screenshot010.jpg)