# D2FC (Season 4)

![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot001.jpg)

## Summary

- Name: **D2FC**
- Author(s): **VuDentist**
- Version: **Season 4**
- Year Released: **2021**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/)

## Includes

- Cactus Platform (1.10)
- D2FC (Season 4)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`D2FC (Season 4)`** that launches
  **`Game.exe`**.

## Notes

- D2FC stands for **Diablo 2 Fan Club**.

## Known Issues

- None

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Once that was
  done, I rewired the rest of the dlls by:
	- Removed **`D2Mod.dll`** from **`D2Mod.ini`**. This is redundant.
	- Removed **`ddraw.dll`** from **`D2Mod.ini`**.
- Removed the **`glide3x.dll`** since this was causing the following errors
  upon program exit:
 
	- **`An exception (C000000D) occurred during DllEntryPoint or DllMain in module: C:\Games\Diablo II\glide3x.dll`**
	- **`UNHANDLED EXCEPTION: An invalid parameter was passed to a service or function (c000000d)`**

- Removed **`ddraw.dll`**, and any other unnecessary files.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [D2FC](https://www.moddb.com/mods/d2fc-mod/downloads/d2fc-mod-update-seasion-4)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/D2FC_Season_4/screenshots/Screenshot010.jpg)

## Patch Notes

```
mod by DentistVu - a Vietnamese modder - New skill (99+), new item, new recipe,
new Bosses, new map - New quest system, uber quest, event online, - More
challenger, more fun.. 
```