# The Sin War (3.50)

![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot002.jpg)

## Summary

- Name: **The Sin War**
- Author(s): **borg**
- Version: **3.50**
- Language(s): **English, Chinese (中文)** 
- Year Released: **2024**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/)

## Includes

- Cactus Platform (1.13c)
- The Sin War (3.50)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`The Sin War (3.50)`** that launches
  **`Game.exe`**.

## Notes

- This mod supports **Chinese (中文)**. You can activate it by renaming the
  **`data_CHI`** folder to **`data`**, and adding the **`-direct`** flag. I was
  able to successfully test this, however the game crashed in some instances
  most likely since I'm missing some files due to my installation being in
  **English**.

## Known Issues

- An **`Unhandled Exception: Access Violation (c0000005)`** will sometimes occur.
  This issue is already documented by upstream.

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`Game.exe`** loader for **`1.13c`** in **BaseMod 1.13.9** to load
  **`BaseMod.dll`**. After that the mod automatically loaded everything it
  needed, including **`PlugY.dll`**, and **`SGD2FreeRes.dll`**. The files are
  most likely the obfuscated **unknown files** in the **`Patch_D2.mpq`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [The Sin War](https://www.moddb.com/mods/tsw/news/version-350-officially-released)
- [Borg Home Page](https://home.gamer.com.tw/borg)

## Screenshots

![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/gold/The_Sin_War_3.50/screenshots/Screenshot009.jpg)

## Patch Notes

```
Suffered from diminishing returns, passive skills with min/max stat mostly are
not worthy of heavy investment. To prevent wasting skill points, players tend to
spend just 1 point. In this version, however, extra points can benefit synergy
skills and thus deserve more consideration.

Interface

    Fixed an issue where advanced stats page fails to display defense bonus from skills.

Skills

Amazon

    Inner Sight and Slow Missiles receive duration bonus from Pierce.
    Decoy has longer base duration and higher chance to parry, receiving life bonus from Dodge and Avoid.
    Valkyrie receives damage bonus from Critical Strike and defense bonus from Evade.

Assassin

    Psychic Hammer receives magic damage bonus from Mind Blast.
    Shadow Warrior has less chance to parry and higher damage resist.

Barbarian

    Concentrate receives defense bonus from Stun.
    Frenzy receives damage bonus from Concentrate instead of Bash.
    Slightly increased chance of Find Item for magic types.
    Shout receives duration bonus from Iron Skin.
    Battle Orders receives duration bonus from Battle Cry.
    Battle Command receives duration bonus from Natural Resistance.

Druid

    Spirits and vines have higher chance to parry, receiving chance bonus from Raven.
    Removed innate 35% poison resist from vines.
    Oak Sage provides defense bonus (capped at 25%).
    Heart of Wolverine provides velocity instead of defense bonus.
    Added 30% damage resist to Grizzly.

Necromancer

    Revive receives duration bonus from Summon Resist.
    Removed innate 35% damage resist from Iron Golem.
    Removed innate 35% fire resist from Fire Golem.

Items

    Slightly balanced normal/exceptional set items listed below:
    => Angelic Raiment: Angelic Mantle, complete set bonus.
    => Cathan's Traps: Cathan's Seal (4 items bonus), complete set bonus.
    => Arcanna's Tricks: Arcanna's Flesh (and 3 items bonus), Arcanna's Sign, complete set bonus.
    => Isenhart's Armory: Isenhart's Case
    => Vidala's Rig: complete set bonus.
    => Cow King's Leathers: complete set bonus.
    => The Disciple: Credendum (4 and 5 items bonus)
    => Naj's Ancient Vestige: Naj's Circlet
    => Orphan's Call: Whitstan's Guard (and 3 items bonus)
    Slightly adjusted life/mana leech suffixes values.
    Gothic Shield (and upgraded versions) can have 4 maximum sockets.
```