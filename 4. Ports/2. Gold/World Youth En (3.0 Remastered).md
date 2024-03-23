# World Youth En (3.0 Remastered)

![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot002.jpg)

## Summary

- Name: **World Youth En**
- Author(s): **BishoYo**
- Version: **3.0 Remastered**
- Language(s): **Polish (Polski), English**
- Year Released: **2019**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/)

## Includes

- Cactus Platform (1.13c)
- World Youth En (3.0 Remastered)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`World Youth En (3.0 Remastered)`** that
  launches **`Game.exe`**.

## Notes

- This mod is available in **Polish**, and can be easily switched to by changing
  the following values in **`PlugY.ini`**:

	- **`SelectedLanguage`** from **`ENG`** to **`POL`**.

  I can't test this since I only have an English installation, and am missing
  some files.

## Known Issues

- When entering a game from the Character Selection screen, you may sometimes
  get an Access Violation. Keep trying until you get in.

## Porting Fixes

- The provided installer auto-added a **`WY`** suffix to all files. I corrected
  all of the file names.
- The mod was placing files inside multiple files called **`D2XMusic.mpq-EN/PL`**.
  The **`D2XMusic.mpq`** is a Protected File and cannot be modified. Luckily these
  MPQs were actually being used as a way to provide language specific PlugY
  defaults. I've extracted the necessary files, and removed these MPQs.
- The mod will normally force save to the **`Save\WYE-T\`** directory in
  your Diablo II Root Directory. However, I've edited both the **`PlugY.ini`**,
  and **`PlugY/PlugYDefault.ini`**, and changed **`ActiveSavePathChange`** to
  **`0`**, which allows Cactus to manage the folder.
- Removed the **`Chat.exe`** and **`WYE-T.exe`** files.
- Cactus isn't responsible for loading additional MPQs, so I've merged the
  **`D2GamePack.mpq`** into the **`Patch_D2.mpq`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [WYE-T 3.0 Remastered - Mod DB](https://www.moddb.com/mods/diablo-2-wye-t-30-remastered-modification/downloads/diablo-2-wye-t-30-remastered-plen-modification)

## Screenshots

![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/gold/World_Youth_En_3.0_Remastered/screenshots/Screenshot010.jpg)

## Patch Notes

```
WYE-T was originaly created for the Polish version of game. It was created for
several years. After many, many years, it got an English version.

On "Alchemic" website (my website) there are some information about WYE-T.

Recipies can be found in Mod "Data" folder or on the "Alchemic" website.

The full name is World Youth En - Technology - Back from the Dead 3.0 Remastered
:) The name grew over time as new fixes were released. It is mod for fun. There
are a lot of new monsters in it, lots of new items. The characters have hardly
changed and the gameplay seems easier the further it gets. This is my first major
mod that I have ever made. I put a lot of work into it and it was very fun to play.

In early versions, there were bugs caused by monster animations. The Remastered
version fixed a lot of bugs but they can still happen. Additionally, the HD
version may cause errors because it's a plugin not made by me.
```