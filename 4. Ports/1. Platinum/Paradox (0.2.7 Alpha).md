# Paradox (0.2.7 Alpha)

![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot001.jpg)

## Summary

- Name: **Paradox**
- Author(s): **Lady Isabelle, Ogodei**
- Version: **0.2.7 Alpha**
- Year Released: **2021**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/)

## Includes

- Cactus Platform (1.10)
- Paradox (0.2.7 Alpha)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Paradox (0.2.7 Alpha)`** that launches
  **`Game.exe`**, with the flags set to **`-direct`**.

## Known Issues

- The in-game native screenshot functionality doesn't work. You can work
  around this by setting the **`keyscreenshot`** value in **`ddraw.ini`**
  to **`0x2C`** (Print Screen). It will save your screenshots into the
  directory defined by **`screenshotdir`**.

## Porting Fixes

- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Everything
  loaded properly after that.
- Removed **`glide3x.dll`** and **`glide-init.exe`**.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Paradox - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?f=190&t=66578)
	- The link for this download is dead at the link above. I was able to find
	  a copy of the mod on some random torrent online, which I used to port it
	  to Cactus.

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot002.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Paradox_0.2.7_Alpha/screenshots/Screenshot010.jpg)

## Patch Notes

```
Public Alpha 0.2.7 - 04/01/2021

===

Enemies

Various enemies that use player skills now use their own monster version. Curses
however remain the same as the Necromancer's The new monster skills are: Glacial
Spike, Skystrike, Fire Nova, Bone Armor, Burning Weapon, Berserk, Bash,
Concentrate, Smite, Zeal, Vengeance, Jab, Holy Freeze, Might, Charged Bolt,
Prayer, Blessed Aim, Concentration, Conviction, Fanatacism, Sacrifice, and
Defiance.

Monster Bone Armor no longer grants physical resist

Monster Conviction resistance penalty lowered from 30+5/lvl to 25+4/lvl. Monster
Conviction no longer lowers defense.

Monster Vigor minimum speed increased from 7% to 20%. Maximum Speed decreased
from 50% to 40%

Monster Holy Freeze now applies a chill instead of applying a debuff that lowers
enemy speed.

Monster Sacrifice self damage increased from 8% to 16%.

Mephisto now has 10 Melee/Ranged Minions of Hate instead of 20

Melee Minions of Hate deal less poison damage, and deal less physical damage in
Hell difficulty. They also have less attack rating and health in Hell
difficulty.

Succubus now always fire 5 missiles in all difficulties. Lowered the minimum
damage of it as well.

Andariel is now level 75. As a result she has less overall stats, but drops
lower level gear that should be more obtainable by the time you begin fighting
her.

Duriel is now level 85. Similar results to Andariel as mention above.

Regular enemies and chests have an increased chance to drop items, and a
decreased chance to drop Junk

Unique and champion enemies have a 100% chance to drop additional non-magic
items, and no longer drop Junk

Unique, Champion, and Super Unique enemies have an increased chance to drop a
rare, unique, or set item if possible

Act Bosses drop 5 additional items on death

Act bosses have a slightly increased chance to drop uniques, sets and rares

New act 2 enemy that appears in Nightmare and Hell: Hollow Priestess. Appears in
The Stony Tomb 1 and 2, and The Halls of the Dead Level 1, 2 and 3. They drop
Bone of the Damned and the Jewel Infusion Blueprint.

New act 3 enemy that appears in Nightmare and Hell: Atronach. Appears in The
Kurast Temples. They drop Eye of the Oracle and the Armor Infusion Blueprint.

Two new act 5 enemies that appear in Nightmare and Hell: World Crusher and Time
Weaver. The World Crusher drops Ethereal Brain and the Weapon Infusion
Blueprint, while the Time Weaver drops Writer's Hand and the Jewelery Infusion
blueprint. The World Crusher appears in the Hell Portals while the Time Weaver
appears in Nilathak's Temple.

Otherworldly Beasts now also appear in The Cave Level 1 and 2, The Pit Level 1
and 2, and The Underground Passage Level 2. Modified the description of Eldritch
Stones to fit these changes. The beasts are slightly more common as well

Items:

More Draught Blueprints, sold by Alchemist Vendors:

Draught of Inferno - Increases fire skill damage and pierce

Draught of Blizzard - Increases cold skill damage and pierce

Draught of Thunderstorm - Increases lightning skill damage and pierce

Draught of Plague - Increases poison skill damage and pierce

Draugh of Cascade - Increases magic skill damage and pierce

Draught of Souls - Increases minion physical damage and attack speed

Draught of Spirits - Increases minion elemental damage and attack speed

Draught of Water - Increases fire resistance and maximum fire resistance

Draught of Warmth - Increases cold resistance and maximum cold resistance

Draught of Grounding - Increases lightning resistance and maximum lightning
resistance

Draught of Antibiotics - Increases poison resistance and maxiumum poison
resistance

Draught of Warding - Increases magic resistance and flat magic damage reduction

Draught of Carrion - Increases minion life and minion defense

Draught of Steel - Increases defense and physical resistance

=========

Jewels now have 1 random Gem amour affixes instead of pulling from a list of
random affixes

Jewels can no longer be rare

Jewels have new item graphics, thanks to Alpha

Jewels are slightly more rare to find

=========

New Spell Stones: 

Minion Damage, Hp and Defense(Eternal Reign) 

Resistances(Chromatic Ward)

Defense and Damage Reduction(Adamantium Carapace)

Mana Absorb and Magic Resist(Astral Aegis)

Physical Damage and Attack Rating(Crushing Force)

=========

New Unique Gloves that drop from The Lady of Shadows. Like her other items, they
can be combined with a Rune to create a Paradox of Shadows again.

Three New Unique jewels that The Lady of Shadows drops exclusively. Like her
other items, they can be combined with a Rune to create a Paradox of Shadows
again.

Increased the power of Merle's Shadows and the Socket Affinity Aura. The socket
affinity aura has a new graphical effect

New Uniques Sets and Runewords:

Necrophage Stone Unique Jewel

Exile's Innocense Unique Citrine Amulet

Empty Promise Unique Large Charm

Embodiment Unique Grand Charm

Commitment Unique Grand Charm

Divide Unique Grand Charm

Secret Pages Unique Large Charm

Empty Stomach Unique Grand Charm

Flesh Weap Unique Talisman

Mind Weap Unique Talisman

Blood Weap Unique Talisman

Scorching Facet Unique Jewel

Freezing Facet Unique Jewel

Shocking Facet Unique Jewel

Poisonous Facet Unique Jewel

Arcane Facet Unique Jewel

Reflections Set

End Sorceress Weapon Runeword (Zod)

Comforting Welcome Unique Lesser Eagle Orb

Shiva's Ward Unique Greater Dragon Stone

Fire Eye's Ire Set

Tal Rasha's Ascendancy Set

=========

New Blueprints: Mystic Anvil, Mystic Hammer, Archaic Runestone, and Empty Orb

The Hollow Power Blueprint now requires an Empty Orb (3x Orbs of Scouring)
instead of Gem Dust.

Armorer's Scrap, Orb of Scouring, and Blacksmith's Whetstone now state they are
Crafting Reagents

Adjusted the values of all of the fossils, some are stronger while some are
weaker. They now always have a consistent roll to their values now.

Iron Spears require 30 Dex. Iron Tridents require 35. These may change in a
future patch.

Uniques and sets have an overall increased chance to drop if possible (if an
item drops and there is no unique/set for it, it will instead become rare/magic)

Class items no longer have a 2/3rd drop chance penalty

Sounds:

New sound for Path of Exile Rings

New sound for Path of Exile Amulets

New sound for Path of Exile Currency

New Sound for picking up and consuming any potion

Time Weavers use cut sound effects for Panther Women

Areas:

Act 1 Side areas are now Area-Level 75 in Hell

Act 2 Side areas are now Area-Level 85 in Hell

Act 3 Side areas are now Area-Level 95 in Hell

These are lowered in monster-level as to allow target farming for gear that is
around your level, and be slightly less difficult as well

Slightly increased the density of the Kurast Temples

Halved the density of Kurast Causeway

UI:

The Cube's inventory is increased to 7x7

Health and Mana Potions, and the Globes, are now the classic Red & Blue once
again. If you wish to revert the changes, do the following: Go into the mod
folder, in data\global\ui\panel. rename hlthmana.dc6 to something else, and
rename hlthmanaBLACKPURPLE.dc6 to hlthmana.dc6 Then head into data\global\items.
rename NewHealingPotion and NewManaPotion to something else, and rename
NewHealingPotionBLACK and NewHealingPotionPURPLE to NewHealingPotion and
NewManaPotion respectively.

Added two new optional fonts: AVQUEST and LATO-BOLD If you would like to change
these fonts, go to the mod folder, in data\local\. There are two folders,
fontAVQUEST and fontLATOBOLD. Example screenshots can be found in the folders.
When you've decided on whichever one you like, rename either folder to: font. To
disable it, simply rename the font folder to something else.

If you wish to get rid of the color pallete changes, which most notably causes
blood to be black, in data\local you will find color.txt. Delete or rename it to
revert to regular colors.

These instructions can be found within the readme as well, under the FAQ section

Fixes and misc changes:

Updated Blessed/Divine Orb List

Corrected the description of Jeweler's Orb AGAIN seriously I'm unsure why these
changes keep reverting

Incorrect description on The Eclipse is now fixed

Saint of the Conjurer now lists itself as being unable to be used with The
Eclipse due to an oversight

Removed the buggy texture on the pre-screen

Fixed Succubi and Oblivion Knights still casting a bugged Wither

Fixed Ancient Westmarch Bow being the incorrect size

Fixed incorrect welcome messages in the Act 5 Hell Portals

Temporarily disabled the Holy Shrine due to crashes

Fixed Charms having the incorrect name for the Energy Suffix

Fixed Orb of Transmutation's description

Fixed Corrupt Spirits being unable to hit anything

Possibly fixed a color pallete bug that could occur with the Opal gem. Let me
know if it still persists!

Improved the image quality of the Orbs of Prophecy and Fossils

Replaced the image graphic of the Sacred Globe

Several backend changes related to sets to prevent potential issues and
irrelevant error log spam
```