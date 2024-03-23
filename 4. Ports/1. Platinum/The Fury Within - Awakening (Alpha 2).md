# The Fury Within - Awakening (Alpha 2)

![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot001.jpg)

## Summary

- Name: **The Fury Within - Awakening**
- Author(s): **DeathScythe, SilentX, Myhrginoc**
- Version: **Alpha 2**
- Year Released: **2002**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/)

## Includes

- Cactus Platform (1.10)
- The Fury Within - Awakening (Alpha 2)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`The Fury Within - Awakening (Alpha 2)`** that
  launches **`Game.exe`**, with the flags set to **`-mod TFW -direct`**.

## Known Issues

- None

## Porting Fixes

- Replaced the provided **`Game.exe`** with the default Cactus one which
  provides No CD support.
- Removed **`dsound.dll`** and **`dsound.ini`**. Cactus already provides
  **DSOAL w/ OpenAL Soft** which has proper **Environmental Effects** support.
  **IndirectSound** doesn't (even if it lets you enable it, go to a cave and
  test it yourself). Furthermore, **`dsound.dll`** is a
  Cactus Protected File.
- Removed **`D2.LNG`** file. This is a Cactus Protected File. If this
  causes issues for this mod, then I'll need to drop the mod down to **Bronze**
  level since Cactus won't allow this due to a high likelihood that it will
  break your game installation. The mod seems to be working perfectly fine with
  the default **`D2.LNG`** file, from my testing during the porting process.
  Hopefully this stays that way.
- This mod comes with a **`D2gfx.dll`** that is already patched to load
  **`PlugY.dll`** and **`D2Mod.dll`**. I've replaced it with a freshly patched
  **`D2gfx.dll`** that only loads **`D2Mod.dll`**.
- Removed **`dsound.dll`** from **`D2mod.ini`**.
- Removed all addons that were most likely added by D2SE packagers:
	- Removed **SGD2FreeRes**.
	- Removed **D2GL**.
	- Removed **PlugY**.
- Cactus isn't responsible for loading external MPQs, and this mod contains a
  **`Patch_D2.mpq`**, and **`tfw-patch.mpq`** with unkwown files. Due to me not
  having those files, I can't easily repack them. So I've done the following
  to allow loading of the external MPQ:
	- Renamed **`D2Mod.ini`** to **`TFW.ini`**.
	- Renamed **`tfw-patch.mpq`** to **`TFW.mpq`**.
	
  This will allow **D2Mod** to load those extra files.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [TFW: Awakening - Alpha 2 - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=24&t=37107)
- [TFW: Awakening - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?t=3955)
- [TFW: Awakening - Mod DB](https://www.moddb.com/mods/the-fury-within-awakening/downloads/d2se-the-fury-within-awakening-a2p17a)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/The_Fury_Within_Awakening_Alpha_2/screenshots/Screenshot010.jpg)