## Singling
##### By: Jonathan Vasquez (fearedbliss)
##### Build: 2021-04-25-2000

## Description & Goals

A collection of non-gameplay modifications and fixes in order to improve the
Vanilla Diablo II Single Player & LAN Experience.

Singling is made to be a **`Simple Drag & Drop Solution`**. There is no
configuration file or toggable options. If I don't believe a fix is 
needed or stable enough, it simply won't be included.

Singling **`does not`** provide any sort of modifications that have a 
psychological impact on the immersion aspect of **`Vanilla`** Diablo II, 
which eliminates all visual level changes as a result. For example, 
Extended Stash (10x10), Font Fix, and Item Level don't really have any 
gameplay impact, however they do have a psychological impact on the 
immersion of the user's experience. Since my goal with **`Cactus`** and 
**`Singling`** is to allow people to enjoy any version of Diablo II that 
ever came out **`while adhearing to the original spirit of the game`**,
modifications outside of this goal are not included.

## Supported Versions

- **`1.00`**
- **`1.05b`**
- **`1.07`**
- **`1.08`**
- **`1.09b`**
- **`1.10`**
- **`1.13d`**

## Features

- You can now run multiple clients of Diablo II.
- You are now able to quickly join LAN games.
- Fixed CPU usage bug in Main Menu, Single Player, and LAN games.
- The Battle.net button has been disabled for safety reasons.
- The introduction cinematics are now automatically skipped.
- The FPS is now unlocked in Single Player. **`(Same as LAN games)`**
- The scrolling letters slowdown is now fixed for both **`DirectDraw`** and **`Glide`**.

- **`[1.00-1.08]`** The **`players`** command is now implemented.

- **`[1.00-1.10]`** You no longer need the CD in order to play the game.
- **`[1.00-1.10]`** You can now make Hardcore characters without beating Softcore.

- **`[1.08-1.13d]`** The game will now work with the MPQ files included in the
  new Blizzard Installer.
  
- **`[1.08/1.10-1.13d]`** Ladder Runewords are now enabled on Single Player.

## Notes

- The scrolling letters fix required the disabling of the **`fps`** command.

- When using **`cnc-ddraw`**, you will also automatically gain the ability for
  the window to no longer minimize when you click out of it when using its
  window mode capabilities. Do not use Diablo II's **`-w`** flag since it will
  interfere with **`cnc-ddraw`**. You will also gain the minimize/maximize
  buttons, and the ability to dynamically resize the window as well. Using
  **`cnc-ddraw`** (regardless of the scrolling letters fix) will also prevent
  the **`fps`** command from working.

- If you experience extreme lag in the Main Menu for versions 
  **`1.00-1.09b`**, try using **`cnc-ddraw`**, this should fix it. If for 
  whatever reason that still doesn't work, you'll need to revert the CPU 
  fix for the Main Menu specifically (You'll still have the fix for Single 
  Player and LAN). Simply replace the **`D2Win.dll`** you are currently 
  using with the one in the Singling Stock Directory for the affected 
  version. 

- If you experience weirdness with the mouse cursor, this is most likely 
  due to the FPS Unlock Fix. Regardless of the displayed FPS, the game 
  will always be a **`25 FPS`** game and thus the showed FPS doesn't 
  actually matter. The reason this fix is being implemented is because the 
  mouse cursor on **`Single Player`** games is directly connected to this 
  FPS limit, which makes the cursor choppy. The fix simply disconnects 
  the mouse cursor from this limit and allows it to run independently. 
  This is effectively the same as what happens on **`LAN`** and on 
  **`Battle.net`**. This weirdness will mostly likely never happen or 
  happen rarely. 

- The **`players`** command works similarly to **`1.09b`**. You type **`players #`**
  with no slash and the game will simulate that. No confirmation will be displayed.
  If you are in a LAN game, the host will need to set the **`players #`** explicitly.
  The Monster's HP, Experience, and Item Drops (Including Chests) will be affected.

  For versions before **`1.07`**, the game was designed with monsters and chests
  having a chance to drop only a single item, and chests are not affected by
  player count at all. Monsters however will have an increased chance of dropping
  a single item for every additional player in the game (up to players 5, everything
  after that doesn't matter).

  This feature also required us to remove the **`soundchaosdebug`** command
  which was really only used during development.

### Players Command Usage (Pre 1.09)

The minimum number of players you can set is **`1`** and the maximum amount of
players is **`8`**. If you exceed these values, the players count will be set
to the lowest or highest accordingly.

- **`players`** - Sets the players to **`1`**.
- **`playersX`** - Sets the players to **`X`**.
- **`players X`** - Sets the players to **`X`**.

If you do something like **`xplayers`** or **`players in space`**, it will
correctly ignore those messages. If you do something like **`players 5p`** or
**`players5p`**, it will consider that as **`players 5`** and will ignore
the rest.

## Patch Rationale 

#### Patch 1.00 (Thursday, June 29, 2000)

This patch was selected due to it simply being the first version of 
Diablo II released. There are some things possible in this version that 
were quickly patched out, however, there are also many instabilities in 
the game that may result in crashes or even the character becoming 
corrupted.

Some things that can happen in **`1.00`** that were patched in 
subsequent **`Pre-1.07`** patches: 

- The Cow Level can be opened even if the King is killed.
- Whirlwind attack checks happen once per frame.
- Bonefarming
- Maggotfarming
- Corpse Explosion scales with the player count.
- Lord de Seis can steal your potions.

#### Patch 1.05b (Friday, February 2, 2001)

This patch was picked because it is the most stable and balanced version 
of the game before **`Lord of Destruction`**. It was also picked over 
**`1.06`** since the main reason **`1.06`** was released was to 
implement anti-duping code. Due to the way item generation works in 
these patches, you can legitimately find items that have the same 
fingerprint, and the anti-duping code would delete those items. Watch 
the following [video](https://odysee.com/@TheCactusSanctuary:f/1_-Diablo-II--Play-1.05b%2C-Not-1.06_b.-Item-Dupe-Removal-Behavior-Demo.-yFFBYNhH8Pw:6) for a
demonstration of this.

If you are looking for a stable version of **`Diablo II`** that closely 
resembled the design, feeling, and balance of **`Diablo I`**, this is 
the patch for you. Patches **`1.07-1.09`** departed from a lot of the 
original **`Diablo II`** game design by refining and extending core 
elements of the game, but overall still had some resemblance to the 
original **`Diablo II`**. Two years later, Patch **`1.10`** was released 
and fundamentally changed the way the entire game was played. Original 
**`Diablo II`** before the Expansion is pretty much a completely 
different game. Even though **`Diablo II`** still retained a 
**`Classic`** mode after the Expansion was released, the Classic 
experience was fundamentally altered. 

Some amazing and interesting things about **`Pre-1.07`**:

- Unique items have no level requirements.
- Unique item stats were very different than **`1.07+`**.
- Uniques, Sets, and Rares can all be gambled for with a fixed chance of **`3%`**, **`5%`**, and **`7%`** respectively.
- There are no immunities in the game.
- There are no spell cooldowns.
- Item drop rates are very low and everything means something.
- Slow game progression (No **`players #`**, but implemented in **`Singling`**).
- Item affix generation and possibilities are much better than **`1.07+`**.
- Set items actually drop more frequently than Rares (**`Common`** -> **`Magic`** -> **`Set`** -> **`Rare`** -> **`Unique`**).
- More deterministic RNG.
	- If you have a **`Manald Heal`** and a **`Nagelring`**, then the next Unique ring will be a **`Stone of Jordan`**.
	- Failed Uniques have triple durability and drop as a Rare instead (i.e: If you already happened to have the Unique in the game).
- Mana potions cannot be purchased in stores and drop less frequently than **`1.07+`**.
	- This makes **`Energy`**, **`Warmth`**, **`Mana Per Kill`**, and **`Mana Leech`** very valuable.
- Crushing Blow does not work on SuperUniques, Champions, and Bosses.
- Magic Find does not work on SuperUniques, Champions, and Bosses.
- No Partial Set Bonuses.
- Nothing from **`Lord of Destruction`** such as **`Runes`**, **`Charms`**, **`Jewels`**,
  **`Elite Items`**, and **`Improved Hirelings`** since the Expansion didn't exist yet.

For all **`Pre-1.07`** versions, there seems to be a bug where monsters have
**`4x`** their intended attack rating. This pretty much makes defense rating
practically useless in the majority of situations.

#### Patch 1.07 (Wednesday, June 27, 2001)

This patch was selected because it is the first version of
**`Lord of Destruction`** that was released on the Expansion CDs and was 
the first massive change to Diablo II. Due to the game still being 
pretty buggy, **`1.07`** could only be played on **`Single Player`**, 
since people connecting to **`Battle.net`** were immediately updated to 
**`1.08`**. Due to the state of the patch, it contains a lot of 
features, behaviors, and item generation combinations that were 
immediately patched out in patches **`1.08-1.09`**. It also contains 
some bugs and differences that are fun to play with such as: 

- Rejuvenation Potion Bug
- Mana Per Kill (MPK) rings
- The Original **`1.07`** Unique Items (Often called **`1.08`** Uniques).
- Static Field in the Expansion works the same as Classic.
- Shield blocking in Classic actually uses the Expansion formula. **`(1.07-1.08)`**
- Crazy +Damage Charms
- Dual Wielding Bug
- Crushing Blow works with full effectiveness on ranged weapons.
- Poison damage bug works even with melee weapons.
- Immunities were introduced but can be broken with full force.
- Triple immunities are possible.
- The sound for Gems was different than other versions.
- Magic Finding is effectively broken, and the primary way of getting 
  items is by Rack Running. 
- Runes are in the game but the available Runewords and their stats are
  vastly different than what was available in **`1.08-1.09`**. 

#### Patch 1.08 (Wednesday, June 27, 2001)

This patch was selected because it is a more stable version of 
**`1.07`** that still retains particular early expansion design 
decisions, such as still containing mostly the same unique items that 
**`1.07`** had, and better racking probabilities than **`1.07`**. The 
patch seems to be closer to **`1.07`** rather than **`1.09`** but still 
sits in a healthy middle. 

#### Patch 1.09b (Wednesday, September 5, 2001)

This patch was selected because it is the most stable version of Diablo 
II after **`Lord of Destruction`** was released that still includes some 
of the design elements and mechanics of the original **`Diablo II`**, 
and overall completed the refinements to the Expansion as originally 
released. This patch also introduced the **`players`** command and many 
other quality of life improvements and fixes. **`1.09b`** was also 
picked over **`1.09d`** because it contains **`players 64`** and working 
CtC. **`1.09d`** has broken CtC which means that you will see the 
animation of your CtC effect, but it actually won't do anything. 

#### Patch 1.10 (Tuesday, October 28, 2003)

This patch was selected because it was the last patch released by 
**`Blizzard North`** after two years of observing the **`1.09`** 
community, and released around **`3`** months after the [Blizzard North 
Exodus](https://en.wikipedia.org/wiki/Blizzard_North#History), where 
most of the key people left and formed **`Flagship Studios`**, 
**`Castaway Entertainment`**, and **`Hyboreal Games`**. [Peter 
Hu](https://www.diablowiki.net/Peter_Hu) was the Chief Architect for 
Patch **`1.10`** and from my conversations with David Brevik, Peter 
stayed behind to finish the patch. Afterwards, he left Blizzard North 
and joined Flagship Studios. 

Patch **`1.10`** was the last and biggest update made directly by 
**`Blizzard North`** that brought Diablo II into the modern era. It 
massively redesigned and rebalanced the game, and for the most part is 
the Diablo II that we all know and love today. All further additions 
added to the game such as **`Respecs`**, **`Increased Rune Drop Rates`**,
**`Faster Merc Leveling`**, and the removal of **`Iron Maiden`** from the
Chaos Sanctuary, came after the Exodus. Other than that, the game hasn't
changed much since. Some of the things introduced in this patch were: 

- Rebalanced all character classes.
- Synergies
- Massively increased game difficulty.
- Guest Monsters
- Blocking Quests
- Experience penalty after level 70.
- Eliminated party experience sharing beyond two screens.
- Mana Potions added to Vendors.
- Lots of new Unique Items, Runewords, and Recipes.
- Improvements to the Treasure Class, Item, and Drop Systems.
- Uber Diablo (Online Only)
- A lot of bug fixes and a lot of other changes.

##### Patch 1.10 / Blizzard North / Flagship Studios Interviews and Presentations

- [David Brevik discusses LOD and Patch 1.10](https://youtu.be/cuNgTnfk-wU?t=3992)
- [David Brevik discusses Diablo was intended to be a Hardcore-only game from the beginning](https://youtu.be/rML7xVqaVr4?t=950)
- [Flagship Studios Developer Interview - Formation of FSS after Blizzard North Exodus](https://www.youtube.com/watch?v=-6AQZVru2to)
- [Mike Huang's Experience at Blizzard North](https://web.archive.org/web/20100224063807/http://diablo.incgamers.com/blog/comments/guest-article-remembering-blizzard-north-and-diablo-ii)

#### Patch 1.13d (Thursday, October 27, 2011)

This patch was selected because it is the last patch released by 
**`Blizzard`** that still retained the original program architecture. 
It contains all of the major changes and features ever released for the 
game after **`1.10`**. This is also the last patch that supports 
**`DirectDraw`**, so if you are planning on using **`cnc-ddraw`** as 
your main video renderer, you should choose this version over 
**`1.14d`**. Besides the internal compatibility fixes in **`1.14d`**, 
they are both identical. 

Since **`Diablo II: Resurrected`** is based on **`1.14d`**, this will be 
the last version supported by Singling. 

## References

- [Release Dates - 1](https://www.theamazonbasin.com/wiki/index.php?title=Patch)
- [Release Dates - 2](https://www.theamazonbasin.com/forums/index.php?/forums/topic/125365-diablo-ii-patch-dates/)
- [1.00 Info](https://www.diabloii.net/forums/threads/the-time-travelers-vortex-part-2-a-guide-to-version-1-00.933726/)
- [1.05 Info](https://www.diabloii.net/forums/threads/a-guide-to-classic-1-06b.745320/)
- [1.07 Info](https://www.diabloii.net/forums/threads/repuszs-1-07-guide-repost.472485/)
- [1.08 Info](https://www.diabloii.net/forums/threads/1-08-news-info-and-gossip.955142/)
- [1.09 Info](https://www.diabloii.net/forums/threads/robbyds-time-travelers-guide-to-1-09-v1-1.753642/)
- [1.10 Info](https://www.diabloii.net/forums/threads/1-10-faq-for-sp-v-2-0-repost.472493/)
- [Time Traveler's Vortex - Part 1](https://www.diabloii.net/forums/threads/the-time-travelers-vortex-part-1-a-guide-to-spf-time-travel.933724/)
