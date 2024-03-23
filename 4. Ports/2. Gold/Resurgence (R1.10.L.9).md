# Resurgence (R1.10.L.9)

![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot002.jpg)

## Summary

- Name: **Resurgence**
- Author(s): **Fohg, Isumi, Amek**
- Version: **R1.10.L.9**
- Year Released: **2016**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/)

## Includes

- Cactus Platform (1.13c)
- Resurgence (R1.10.L.9)

	This was the **`Patch_D2.mpq`** info in the **`d2_resurgence_patch_manifest.xml`**
	when I downloaded it from the **`current_patch`** folder on **`2024-03-01-1845`**:

	- Name: **`Patch_D2.mpq`**
	- CRC: **`70932B32`**
	- Last Modified: **`27/09/20 10:33:12`**

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Resurgence (R1.10.L.9)`** that launches
  **`Game.exe`**.

## Known Issues

- You will get two errors when you exit Diablo II which are related to **`glide3x.dll`**:
	- **`An exception (C000000D) occurred during DllEntryPoint or DllMain in module: C:\Games\Diablo II\glide3x.dll`**
	- **`UNHANDLED EXCEPTION: An invalid parameter was passed to a service or function (c000000d)`**
	
	This mod is tightly coupled with its included copy of **`glide3x.dll`**,
	and the game will not work if the file doesn't exist. Even if we started
	it in **`-w`**, it would still force the existence of this file, which will
	cause the issues above.
	
	Removing **`glide3x.dll`** prevented the mod from starting up completely
	since the mod has a hard check on this file implementation. Even trying to
	replace it with **`D2DX`** or **`D2GL`** failed.
	
- This mod is not compatible with **`cnc-ddraw`**.

## Porting Fixes

- Disabled **`Export On Menu`** in **`BH_Default.cfg`** and **`BH_Basic.cfg`**.
  Due note that if you decide to use this feature, the info will be saved in the
  Diablo II Root Directory's **`stash`** folder, which is not a Cactus Protected
  Folder. It would be better for the feature to save the info in the **`Save Path`**
  instead.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Resurgence](http://resurgence.slashgaming.net/)

## Screenshots

![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/gold/Resurgence_R1.10.L.9/screenshots/Screenshot010.jpg)