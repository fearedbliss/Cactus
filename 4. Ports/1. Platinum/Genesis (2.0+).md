# Genesis (2.0+)

![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot001.jpg)

## Summary

- Name: **Genesis**
- Author(s): **BishoYo**
- Version: **2.0+**
- Language(s): **Polish (Polski), English**
- Year Released: **2016**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/)

## Includes

- Cactus Platform (1.10)
- Genesis (2.0+)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Genesis (2.0+)`** that launches
  **`Game.exe`**, with the flags set to **`-direct`**.

## Notes

This mod supports **Polish (Polski)**. If you have a Polish installation, you
can change the **`SelectedLanguage`** to **`POL`** in **`PlugY.ini`**. Note,
I can't test this since I only have an English installation, and thus starting
the game for me crashes, most likely because I'm missing some required files.
  
## Known Issues

- None

## Porting Fixes

- This mod will normally force save to the **`Save\Genesis\`** directory in
  your Diablo II root folder. However, I've extracted the **`PlugYDefault.ini`**
  from the **`Patch_D2.mpq`**, renamed it to **`PlugY.ini`**
  and changed **`ActiveSavePathChange`** to **`0`**, which allows Cactus
  to manage the folder.

- Removed **`glide3x.dll`**.

- This mod contains assets in files named after Protected Files:

  - **`D2xMusic.mpq`**
  - **`D2xVideo.mpq`**
  
  Cactus will ignore these files. I also can't confidently repack them since
  the **`Patch_D2.mpq`** also has files with similar names. Instead of dropping
  the mod completely, I'm just going to remove those files from the mod. I'm
  also deleting the **`D2xMusicWYE.mpq`** which may is probably not being read
  by the game. The game still seems to work fine.
  
- I'm not sure if most of the **`D2Mod<>.mpq`** files are being read, but will
  leave them in for now in case **`D2Mod.dll`** understands how to read them.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Genesis](https://www.moddb.com/mods/diablo-2-genesis-20-en-modification/downloads/diablo-2-genesis-20-d2seplen-modification)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Genesis_2.0+/screenshots/Screenshot010.jpg)

## Patch Notes

```
Diablo 2: Genesis 2.0+ [D2SE][PL/EN] Modification created by BishoYo.  Genesis
2.0+ [D2SE][PL/EN]

[2007-2016]

Made by BishoYo

The Mod in this version is compatible with D2SE!



Some Info:

Genesis was originaly created for the Polish version of game. It was created for
several years. After many years, it got an English version.


On "Alchemic" website (my website) there are many information about Genesis.


Recipies and Runewords can be found in Mod "Info" folder or on the "Alchemic"
website.


This is very extensive Modification. Lots of new Maps, lots of new Monsters,
lots of new Items. New Cube recipies, new Runewords. In addition there are many
Events that extend the game. There are also additions for those who like PvP.


Quests may have wrong texts because I think i forgot to change them while
creating the EN version.
```