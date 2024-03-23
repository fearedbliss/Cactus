# Back to Hellfire (1.02)

![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot002.jpg)

## Summary

- Name: **Back to Hellfire**
- Author(s): **Onyx**
- Version: **1.02**
- Year Released: **2008**
- Porter: **fearedbliss**
- Maintainer: **fearedbliss**
- Port hosted and verified internally by **fearedbliss**
- [**Download Now**](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/)

## Includes

- Cactus Platform (1.10)
- Back to Hellfire (1.02)

## Installation

- Extract the platform into your **`Platforms`** Directory.
- Add an entry to Cactus called **`Back to Hellfire (1.02)`** that launches
  **`Game.exe`**.

## Known Issues

- None

## Porting Fixes

- Since Cactus isn't responsible for loading additional MPQs, and the provided
  mod package was designed for an external launcher, I've merged the following
  MPQs into the original **`Patch_D2.mpq`** from **`1.10`**, in this order:
  - **`BTH.mpq`**
  - **`BTHPatch.mpq`**
  - **`BTHXpack100.mpq`**
- Removed the following files from the **`BTH.mpq`** before the above repacking:
  - **`PlugY/`**
  - **`BTH.ini`**
	- We are instead using the provided **`D2Mod.ini`**.
- Removed **PlugY**.
- The mod normally depends on another launcher for its hooking mechanism. I used
  the **`D2ModSetup.bat`** included in **`D2Mod102`** to patch the
  **`D2gfx.dll`** on **`1.10`** so that it loads **`D2Mod.dll`**. Attempting
  to patch the **`D2gfx.dll`** with the included **`D2Mod.dll`** (1.03) will fail.
  In order to workaround this, backup this file, and then use the **`D2Mod.dll`**
  (1.02) to patch. Afterwards, restore the **`D2Mod.dll`** (1.03). If you don't
  do this, you will have missing strings in the game.
- Back to Hellfire will normally force save to the **`save`** directory. However,
  I've edited the **`D2Mod.ini`**, and unsetted the **`SavePath`**, which allowed
  Cactus to manage the folder.

## References

- [Cactus Platform](https://github.com/fearedbliss/Cactus)
- [Back to Hellfire - 1.00 Release - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?t=49111)
- [Back to Hellfire - 1.01 Release - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?t=49696)
- [Back to Hellfire - 1.02 Release - PhrozenKeep](https://d2mods.info/forum/viewtopic.php?t=51596)
- [Back to Hellfire - 1.02 - Mod DB](https://www.moddb.com/mods/back-to-hellfire-102-for-d2se/downloads/back-to-hellfire-102-for-d2se)

## Screenshots

![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot001.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot003.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot004.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot005.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot006.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot007.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot008.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot009.jpg)
![](https://xyinn.org/diablo/platforms/platinum/Back_to_Hellfire_1.02/screenshots/Screenshot010.jpg)

## Patch Notes

```
Back to Hellfire v1.00 released!

Posted by onyx on Sat Jan 26, 2008 8:08 pm

Enough with the Betas I say, here comes the real thing - Back to Hellfire v1.00!
:) Please take the time to review the changelog, so you know what to expect from
this version (it's a long read, I know). These are the changes done on the mod
since Beta Patch 4.04:

CHARACTERS & SKILLS

    New character added - the Monk
    New character added - the Blood Wizard
    Charged Bolt damage decreased
    Jab skill replaced with Summersault
    Removed "finishing move" from skill descriptions
    Removed "aura" from song skill descriptions
    Fixed wrong framecount of the Dance of Death missile
    Inferno range and damage increased
    Flamewave spread increased
    Fixed the Berserk skill display
    Lighting Wall description and sounds fixed
    Reduced mana cost for many skills
    Added timer for some skills
    Warrior crafting now requires Blacksmith Oil
    Warrior crafting no longer works with socketed items
    Added two missing runewords

MAPS

    Added one new map for the Halls of the Blind sidequest
    Added one new map for the Goat Shrineroom sidequest
    Added two new maps for the Infestation of the Worms sidequest
    Added the original Church tileset
    Walls in Act 5 Caves won't be pierced by missiles anymore
    Slightly increased monster density in the Catacombs
    Slightly increased monster density in the Tombs
    Catacombs Level 3 reworked from scratch
    The Lut Gholein crash has been fixed
    The Act 5 Caves Level 1 crash has been fixed
    Fixed wrong palette in Horazon's Tunnel
    Fixed the entry text of the Poisoned Water Supply
    Snow won't appear in Act 5 town and the Antechamber
    New automap for Act 2 town
    New automap for Act 4 town
    New automap for Act 5 town

ITEMS & AFFIXES

    The book recipe has changed - it now turns two random books into a book for your class
    Skill Books reworked, they now spawn according to monster level
    Added Capes (Blood Wizard only)
    Reworked Staves from scratch
    Staves will spawn with Apocalypse or Teleport charges sometimes
    Blacksmith Oil added
    Added unique Staves and Helms
    Added a new set of recipes
    Removed throwing weapons
    Removed Prevent Monster Heal affixes
    Removed -Durability affixes
    Knockback will now spawn on bows
    Increased values of Mana After Each Kill affixes
    Orbs are now properly sold by act 3 & 4 vendors
    Arcaine's Valor will now properly turn the character golden
    Claw-class weapons will look like katars when equipped

MONSTERS

    Reworked Fallen animations from scratch
    Added new Fallen types - Carvers
    Added new Bat type - Familiars
    Added new Hellboar type - Dreadtusker
    Added melee Goatmen
    Added new Hidden type - Illusion Weaver
    Added new Goat types - Hell Clan
    Added new monsters - Wyrm and Devourer
    Reworked Belial from scratch
    Heavily reworked the Ancients
    Added a new boss, Sir Gorash, to the last level
    Changed the AI of Shredded
    Changed the AI of Bone Demons
    Fixed the AI of Shadowdrinker
    Fixed the AI of King Leoric
    Fixed the AI of Archbishop Lazarus
    Fixed Mephisto's animations
    Reduced damage of Torchants and Psychorbs
    Slowed down the missile attack of Psychorbs and Bone Demons
    Increased size of awareness radius of Gargoyles
    Horned Demons won't turn blue when charging anymore
    Magma Demons will now properly deal damage with their boulders
    Magma Demons are now resistent to fire, not lightning
    Felltwin bosses will not spawn with the Multiple Shot propery
    Na-Krul is now properly slowed down by cold
    Increased group size of Goatmen
    Reduced group size of Gargoyles
    Added shadow to Torchants, Psychorbs, Desert Mercenaries, Iron Wolves, Ormus
    Added taunts for the Defiler, Belial and Na-Krul
    Fixed Snotspill's sounds
    Fixed the Liches' sounds in Cobweb Caves Level 3
    Diablo now shows correct name
    Diablo will now use Apocalypse
    More types of monsters will spawn in many levels
    Fixed wrong framecount for some monsters, causing errors in the log

QUESTS

    New sidequest added - Halls of the Blind
    New sidequest added - Infestation of the Worms
    New sidequest added - The Goat Shrineroom
    Adria has chance to reward with unique ring for rescuing Cain
    The Kill Diablo quest will now trigger only in the proper place
    Changed NPC instructions of the Torn Notes quest in Act 2
    Changed descirptions of the Torn Notes quest in Act 2
    Fixed the text of the Ancients' Altar

MERCENARIES

    Added new skills for Rogue mercenaries - Multiple Shot, Strafe, Immolation Arrow
    Added new auras for Desert mercenaries - Salvation, Concentration, Holy Shock
    Added new auras for Iron Wolf mercenaries - Apocalypse, Chain Lightning, Immolation, Frost Nova
    Cold Iron Wolves will now properly cast their spells
    Heavily reworked HP and levels of all mercenaries

MISCALENNOUS

    New health/mana orbs added
    Original Diablo and Hellfire music included
    Added the Wounded Townsman in Tristram
    Slowed down Vessayar's animation
    Many alterations to various strings
    Some other random tweaks here and there

Check the README for details on requirements, installation and features.

The Back to Hellfire website will be updated with a lot of information in the
following days (including character details, recipes list and sidequests
information), so check back regulary ;) Meanwhile, enjoy playing the mod:

Back to Hellfire v1.00 (154MB)

--------------------------------------------------------------

Back to Hellfire v1.01 released!

Posted by onyx on Sat Mar 22, 2008 9:58 am

About time I released a patch to fix at least some of the bugs in Back to
Hellfire v1.00 :) Here comes v1.01 - a small bugfixing patch with no new features.
Hope you enjoy it :)

CHANGELOG

    Fixed cape-class items - they can be used for runewords and socketing now
    Warrior crafting will now add +2% requirements per skill level to the items
    Capes will spawn with + dexterity bonus (to prevent the Blood Wizard crash bug in some cases)
    Elixirs of Vitality and Energy will now work correctly (thanks to Necrolis)
    Reduced price of mace class items
    Boost of speed and reduced cold effect for King Leoric
    Greatly reduced physical resistance of Bat type monsters
    Monsters won't spawn near the exits of Tomb Level 4
    Fixed wrong palette for objects in Horazon's Tunnels
    Fixed wrong sound file on the Guardians quest completion
    Moved shrines in Catacombs Level 3 so the character won't get stuck behind them
    Reduced chance to knockback on Bloodwave
    Added a short timer on Bloodwave
    Blaze flames won't stack anymore
    Fire Ring flames won't stack anymore
    Reduced Flash mana cost increase per level
    Increased Flash damage increase per level
    Slightly increased Immolation damage
    Slightly reduced Chain Lightning damage
    Increased Ren Geri mana cost
    Removed Summesault mana cost increase per level
    Increased range of Magma Demons
    Decreased damage of Magma Demons
    Fixed Act 5 Magma Demons boulders
    Increased range of Liches and Psychorbs
    Increased Act 3 Succubus damage on Hell difficulty
    Increased damage of Lightning Demons
    Increased HP of Lightning Demons
    + damage and + AR affixes will now spawn on staves
    Increased HP of Diablo
    Increased damage and HP of Archbishop Lazarus
    Fixed a bug that removed Burst of Speed effect after casting Bloodstar or Bone Spirit
    Increased Stone Curse life cost
    Reduced the number of item types sold by Enth'Dar
    Izual's spirit will no longer be named Hork Demon
    Partially fixed armor sold by vendors on Hell difficulty
    Fixed Reflect so it works with no shield equipped
    Blinkbats will now teleport on hit
    Added +AC bonus on Royal Circlet
    Added + magic find bonus on Auric Amulet
    The red portal in Act 4 will no longer read "Travel to Harrogath"
    Fixed loads of typos, mainly reported by D2 Mod Player

To install the patch, simply extract the BTHPatch,mpq file in your BTH folder,
where you already have v1.00 installed. Then run the mod as usual. If everything
is fine, you'll see "v1.01" in the lower right corner of the title screen. If you
don't have v1.00 installed, refer to this thread.

Since we're still experiencing problems with the Phrozen Keep File Center, I'll
give you a direct File Planet link for the download: Back to Hellfire v1.01 (1.04MB)

--------------------------------------------------------------

Back to Hellfire v1.02 released!

Posted by onyx on Mon Sep 15, 2008 3:01 pm

Hello everyone :) Since Patch v1.02 has been greatly delayed in time, I decided
to release what I have already done and leave the rest for the next patch. I'm
talking mainly about the new sidequest that I promised - sadly, it didn't make
it into this patch. The new release fixes some critical bugs though and it was
important to make it available sooner.

CHANGELOG

    Fixed the bug that made the game crash after a Blood Wizard has died (thanks to Havvoric)
    Town Portals cannot be opened in town anymore (thanks to Havvoric)
    Fixed that bug that required you to go to Hell Level 1 before killing Diablo in order to complete the difficulty (thanks to Havvoric)
    Globally increased monster HP, damage, resistances on Nightmare
    Added 8 missing runewords
    More monster variations in many levels
    Added a waypoint in Caves Level 4 and removed the Cathedral waypoint
    Added recipes for Warrior crafting for level 20+
    Added different ambient lighting on levels
    Added new boss - Nightwing the Cold
    Act 2 vendors will sell stamina and thawing potions
    Warcy has constant mana cost
    Reduced Sweep mana cost
    Burning crosses will now glow and damage nearby players
    Lightning Demons were made more aggressive
    Increased monster density in Catacombs
    Reduced monster density in Worldstone Keep
    Removed negative min-damage affixes
    Reduced Demon Crypt levels size to about 2/3 of the original
    Gamble prices will now be static
    Added damage and AR affixes on staves
    Caves entrances will now show on the minimap
    Fixed the hotspot for the Caves "level up" tile
    Tomb Rats won't spawn as Multiple Shot anymore
    Balrogs won't spawn as Multiple Shot anymore
    Act 5 mages were boosted
    Golden Elixir will now show the original image
    Blood Star now steals life
    Bone Spirit now turns enemies into stone
    Blood Star and Bone Spirit cast sounds changed
    Rebalanced lots of runewords
    Carvers won't blink between red and blue color anymore
    Added Blood Knight variations
    Diablo was boosted
    Mephisto was boosted
    Azmodan was boosted
    Archbishop Lazarus was boosted
    Staves will now drop more often
    Leoric will drops runes again
    Removed the Dexterity bonus from Capes (it's obsolete now)
    Loads and loads of typos and errors fixed (thanks to D2 MOD Player)
	
To install the patch, simply extract the BTHPatch.mpq file in your BTH folder,
where you already have v1.00 installed (replace if prompted). Then run the mod
as usual. If everything is fine, you'll see "v1.02" in the lower right corner of
the title screen. If you don't have v1.00 installed, refer to this thread.

Back to Hellfire v1.02 (2.24MB)
```