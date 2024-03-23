# Escape from the Afterlife (1.56 - Hotfix 2)

![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot001.jpg)

## Summary

- Name: **Escape from the Afterlife**
- Author(s): **mouse, erevos**
- Version: **1.56 - Hotfix 2**
- Year Released: **2004**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/)

## Includes

- Cactus Platform (1.10)
- Escape from the Afterlife (1.56)
- Escape from the Afterlife (1.56 - Hotfix 2)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Escape from the Afterlife (1.56 - Hotfix 2)`**
  that launches **`Game.exe`** with the **`-direct`** flag.

## Known Issues

- You will get two errors when you exit Diablo II which seem to be related:
	- **`An exception (C000000D) occurred during DllEntryPoint or DllMain in module: C:\Games\Diablo II\glide3x.dll`**
	- **`UNHANDLED EXCEPTION: An invalid parameter was passed to a service or function (c000000d)`**
	
	Removing **`glide3x.dll`** from the mod prevented the mod from starting
	completely. There seems to be something that isn't allowing DirectDraw to
	become the main renderer which should eliminate the above issue and upgrade
	this mod to **Platinum**.

## Porting Fixes

- Since this mod depends on another launcher for its hooking mechanism,
  I luckily was able to find an old copy of **`PlugY 5.06`**, which provided
  the **`PlugY_Install.exe`**, allowing me to patch the **`D2gfx.dll`**
  on **`1.10`**. Once that was done, I re-wired the dll loading so that
  PlugY loads **`D2Mod.dll`** from **`PlugY.ini`**. These changes allowed
  the mod to work.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Escape from the Afterlife - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=92&t=66698)
- [Escape from the Afterlife - 1.40 Beta - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=92&t=21208)
- [Escape from the Afterlife - 1.56 - Mod DB](https://www.moddb.com/mods/escape-from-the-afterlife/downloads/efta-final-version-1-56)
- [Escape from the Afterlife - 1.56 - Hotfix 2 - Mod DB](https://www.moddb.com/mods/escape-from-the-afterlife/downloads/efta156-hotfix-2)

## Screenshots

![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/gold/Escape_from_the_Afterlife_1.56_Hotfix_2/screenshots/Screenshot010.jpg)

## Patch Notes

```
Escape from the Afterlife Final 1.56 is finally here! Packed with new features
and innovations: Lifebound items, Life/Mana Orbs, Salvage systems, Emblems,
Equipment Parts, Embracement Rings, Runestones, Runeletters/Affix-Words,
Clan Items, Off Hands, Fused Uniques, End Game - Lairs. More New Affixes,
Item types, Skills, Plunders and many more changes and additions!

Everything about Escape from the Afterlife Final 1.56 is HERE

EftA's Discord

INSTALLATION

(Delete any previous EftA installation. Characters of previous versions are not compatible)

    Make sure you have D2SE installed on your D2 folder.
    (i do recommend you to install D2SE on Diablo II v1.13)
    Extract EftA-final-1-56.rar to your desktop
    Run EftA-final-1-56.exe, press the “...” button and select the Diablo II\MODS folder
    Press OK and then Extract
    Run D2SE and Run EftA - Paths 1.56

(don’t change glide settings)

Known Issues
- Letter clutter (red letters) on some equipment parts. They work flawlessly, its only a visual bug
- Poke's skill icon description It work flawlessly, its only a visual bug

THANKS & Credits:

@jessedazebra for Item background transparency
@Shex for Map plugins (Countess, Crypts, Act1 walls, Lut Gholein)
@lady_Isabelle, @Necrolis, @Myhrginoc.
@Mnw95 for the Bufficons plugin
@SVR for the D2Mod System
@Dav92 for D2ExpRes.dll
@Revan for D2tweaks.dll
@Havvoric for D2Newstats.dll
@Yohann for PlugY
#Font mod by void@median-xl.com
#Uniques plugin by @Talonrage (modified by erevos)
#Maps plugin by @Talonrage (modified by erevos)
#Skill icons by @GuyAskingQuestion
@andsimo and the whole DIABLO MODS Discord community
@Johannes Bohm for "Johnny's Mod 1.22"
@Phrozen Heart & @Pagan Rainfall for "Pagan Heart"
Mods: Heroes of the End, Walhalla, Lamment of Innocence

Vanilla EftA up to v1.45c credits

Ettin plugin (modified by mouse)
Pitfiend plugin (modified by mouse)
Red myconid plugin (modified by mouse)
Acromatic Aria & infinitum - Ice Golem new token plugin
Alkalund: bone golem plugin, chimera plugin
Demon666 - act 1 town plugin -digibo - d1 item pack
Goro3d: big cube/stash/inventory plugin
Har'lea'quinn: Aerial servant plugin
Jbouley & Charsi's Forge for the web hosting!
jbouley - item packs 2 & 3, rune pack
Joel & Red Havoc - arcane sanctuary plugin -kingpin - tropo new token plugin
Myhrginoc - new titles plugin
om & jbouley - item packs 1 & 2
phrozen heart - sherical animated gif, bugbear captain dcc's
Red Havoc: several overlays & missiles from his re-colored missile & overlay package
Riparious - gem images
Vegabond_635 - shadow new token plugin, cofs+data for earth elemental, cursed guard
Volf - cow level plugin
Uncountable helpful people at the Phrozen Forums who have helped me through my journey into mod making

Special thanks to:

@mouse (EftA's original creator)
@Sanny8, developer of "Dominus Octava" mod
@tmuhlhausen, developer of "Reawakening" mod
@Conqueror Araksson

Beta test team: @Freeyourmind, @Crystal_Feather, @nulitor, @Meme RePoster

=======================

EftA1.56 hotfix 2 includes hotfix 1, pls report any issues you might have. Comments and feedback are appreciated.

Installation:

Extract the efta156-hotfix2 to Diablo II\MODS\EftA - Paths v1.56\
Replace all files when prompt

Everything about Escape from the Afterlife 1.56
EftA Discord

FIXED

- Equipment Parts, letter clutter (red letters) on some of them
- Blooded Organs, 3 of them missing the string "Blooded Organ"
- Poke's skill icon description
- Runestone rarely dropped as Flawless Diamonds
- Wrong names on some Prefixes
- Rain of Axes, monsters death skill proc damage nerfed (it was too much)
- Leap Attack crash fixed
- Voiced Skill Sound for Lycaine changed, now its female
- Lycaine's Slasher skill, added damage info
- Plunders, 5 of couldn't unlock
- Dancing Blade, a crash with this Ursine's skill (thanks to Sanny)
- Dancing Blade, added a proper pet icon
- Inventory, grid is added. (If you prefer non-grid inventory, after you install
  hotfix 2, go to: Diablo II\MODS\EftA - Paths v1.56\data\global\ui\ and delete
  the PANEL folder)


KNOWN ISSUES

If you haven't equipped anything on both ring slots, when a ring of your class
drops, you will need to open your inventory to retrieve it. But very early in
the mod you will have rings in the two slots so is just a minor annoyance.
```