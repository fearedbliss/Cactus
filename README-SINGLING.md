## Singling
##### By: Jonathan Vasquez (fearedbliss)
##### Build: 2023-04-16-1900

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

Lastly, Singling **`only`** supports versions of the game that were 
developed by **`Blizzard North`**, thus **`1.10`** is the last supported 
version.

## Supported Versions

- **`1.00`**
- **`1.05b (Recommended | Most Stable Original Classic)`**
- **`1.07`**
- **`1.08`**
- **`1.09b (Recommended | Most Stable Original Expansion)`**
- **`1.10 (Recommended | New Expansion & Final Blizzard North Patch)`**

Please check the [Patch Rationale](#patch-rationale) section below
for an explanation as to why each of these patches were selected.

## Features

- You can now run multiple clients of Diablo II.
- You are now able to quickly join LAN games.
- Fixed CPU usage bug in Main Menu, Single Player, and LAN games.
- The Battle.net button has been disabled for safety reasons.
- The introduction cinematics are now automatically skipped.
- The FPS is now unlocked in Single Player. **`(Same as LAN games)`**
- The scrolling letters slowdown is now fixed for both **`DirectDraw`** and **`Glide`**.
- You no longer need the CD in order to play the game.
- You can now make Hardcore characters without beating Softcore.

- **`[1.00-1.08]`** The **`players`** command is now implemented. [(Video)](https://xyinn.org/diablo/videos/09.%20Players%20Command%20for%201.00,%201.05b,%201.07,%20and%201.08%20now%20available%20in%20Singling.mp4)

- **`[1.08-1.10]`** The game will now work with the MPQ files included in the
  new Blizzard Installer.
  
- **`[1.08]`** Ladder Runewords are now enabled on Single Player.

## Notes

- The scrolling letters fix required the disabling of the **`fps`** command.

- When using **`cnc-ddraw`**, you will also automatically gain the ability for
  the window to no longer minimize when you click out of it when using its
  window mode capabilities. Do not use Diablo II's **`-w`** flag since it will
  interfere with **`cnc-ddraw`**. You will also gain the minimize/maximize
  buttons, and the ability to dynamically resize the window as well. Using
  **`cnc-ddraw`** (regardless of the scrolling letters fix) will also prevent
  the **`fps`** command from working.

- If you experience weirdness with the mouse cursor, this is most likely 
  due to the FPS Unlock Fix. Regardless of the displayed FPS, the game 
  will always be a **`25 FPS`** game and thus the showed FPS doesn't 
  actually matter. The reason this fix is being implemented is because the 
  mouse cursor on **`Single Player`** games is directly connected to this 
  FPS limit, which makes the cursor choppy. The fix simply disconnects 
  the mouse cursor from this limit and allows it to run independently. 
  This is effectively the same as what happens on **`LAN`** and on 
  **`Battle.net`**. This weirdness will mostly likely never happen or 
  happens rarely.

- The **`players`** command feature required us to remove the
  **`soundchaosdebug`** command which was really only used for development.

### Players Command Usage (Pre 1.09)

The **`players`** command works similarly to **`1.09b`**. You type **`players #`**
with no slash and the game will simulate that. No confirmation will be displayed.
This also works correctly on LAN, and the difficulty will automatically be increased
if there are more players in the game. If the host sets the players count lower
than the actual current number of players, this number will be ignored and the
higher number will be used.

The Monster's HP, Experience, and Item Drops (Including Chests) will 
all be affected accordingly. For versions before **`1.07`**, the game was
designed with monsters and chests having a chance to drop only a single item,
and chests are not affected by player count at all. Monsters however will
have an increased chance of dropping a single item for every additional
player in the game (up to players 5, everything after that doesn't matter). 
  
The minimum number of players you can set is **`1`** and the maximum amount of
players is **`8`**. If you exceed these values, the players count will be set
to the lowest or highest accordingly.

- **`players`** - Sets the players to **`1`**.
- **`playersX`** - Sets the players to **`X`**.
- **`players X`** - Sets the players to **`X`**.

If you do something like **`xplayers`** or **`players in space`**, it 
will correctly ignore those messages. If you do something like 
**`players 5p`** or **`players5p`**, it will consider that as **`players 
5`** and will ignore the rest. If you do **`players9999`**, only the 
first **`9`** will be used, and subsequently the code will detect that 
it's greater than **`8`** and will use **`8`** instead. If you typed in 
the command in upper case letters such as **`PLAYERS 5`**, mixed case 
letters such as **`PLaYeRs 2`**, or any other variation, it will 
correctly detect that and work the same as the lower case versions.

## I've started playing 1.06/b but want to downgrade to 1.05b for Singling. Is this possible?

Yes! 1.05b and 1.06/b characters are fully compatible. Just move your character to your 1.05b
save folder and enjoy. **Do not** upgrade your 1.05b characters to 1.06/b or you may lose items if you
found any duplicate items legitimately. I also recorded a [video](https://xyinn.org/diablo/videos/12.%20Downgrading%201.06-b%20characters%20to%201.05b.mp4)
testing this compatibility. Make sure to backup your characters before doing this just in case!

## I've started playing 1.09d but want to downgrade to 1.09b for Singling. Is this possible?

Yes! 1.09b and 1.09d characters are fully compatible. Just move your character to your 1.09b
save folder and enjoy. A benefit of moving to 1.09b is that you will have working CtC
and **`players 64`**. Check the Patch Rationale section below for more info. Make sure to
backup your characters before doing this just in case!

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

#### Patch 1.05b (Friday, February 2, 2001) - Recommended

This patch was picked because it is the most stable and balanced version 
of the game before **`Lord of Destruction`** was released. Thus, it is 
the definitive experience of the **`Original Classic`** Diablo II. 

It was also picked over **`1.06`** since the main reason **`1.06`** was 
released was to implement anti-duping code. Due to the way item 
generation works in these patches, you can legitimately find items that 
have the same fingerprint, and the anti-duping code would delete those 
items. Watch the following [video](https://xyinn.org/diablo/videos/11.%20Play%201.05b,%20Not%201.06b.%20Item%20Dupe%20Removal%20Behavior%20Demo.mp4)
for a demonstration of this.

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
- No **`players`** command, but you can use **`Singling`** for this feature.
- Item affix generation and possibilities are much better than **`1.07+`**.
- Set items actually drop more frequently than Rares (**`Common`** -> **`Magic`** -> **`Set`** -> **`Rare`** -> **`Unique`**).
- More deterministic RNG.
	- If you have a **`Manald Heal`** and a **`Nagelring`** on your character (**`Equipped`**, **`Inventory`**, or **`Stash`**), then the next Unique ring will be a **`Stone of Jordan`**.
	- A unique item that's already present in the game will not drop again, but will
	  instead drop as a Failed Unique. Failed Uniques have triple durability and drop as a Rare instead.
- Mana potions cannot be purchased in stores and drop less frequently than **`1.07+`**.
	- This makes **`Energy`**, **`Warmth`**, **`Mana Per Kill`**, and **`Mana Leech`** very valuable.
- Crushing Blow does not work on SuperUniques, Champions, and Bosses. Only white monsters.
- Magic Find does not work on SuperUniques, Champions, and Bosses. Only white monsters.
- No Partial Set Bonuses.
- Nothing from **`Lord of Destruction`** such as **`Runes`**, **`Charms`**, **`Jewels`**,
  **`Elite Items`**, and **`Improved Hirelings`** since the Expansion didn't exist yet.

#### Patch 1.07 (Wednesday, June 27, 2001)

This patch was selected because it is the first version of **`Lord of 
Destruction`** that was released on the Expansion CDs and was the first 
massive change to Diablo II. Patch **`1.07`** is actually
**`Beta Patch 1.07.44`**. The D2 LOD Beta started with Patch **`1.07.41`**,
and during the course of the beta, many more **`1.07.XX`** patches were
released via Battle.net, including **`1.07.45`** and **`1.07.46`**, which
included changes which were later released after the beta was over,
as part of **`1.08`**.

**`1.07`** could only be played on **`Single Player`**, since people 
connecting to **`Battle.net`** were immediately updated to **`1.08`**. 
Due to the state of the patch, it contains a lot of features, behaviors, 
and item generation combinations that were immediately patched out in 
patches **`1.08-1.09`**. It also contains some bugs and differences that 
are fun to play with such as: 

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
- Magic Finding is essentially useless due to a few reasons including but not limited
  to magic finding breakpoints being really high, and the Treasure Class System being
  incomplete. Thus the primary way of getting items is by Rack Running.
  This also means that Windforce cannot drop in **`1.07`** since Racks
  can't drop Bows, Staves, Wands, and a few other types. However, there are
  no **Diminishing Returns** on Magic Find, which means that if you are
  comfortable using the [Dancing of the Souls Easter Egg](https://xyinn.org/diablo/videos/05.%20Dancing%20of%20the%20Souls%20Easter%20Egg.mp4),
  you can stack infinite magic find in order to make monsters only drop unique items.
- Runes are in the game but the available Runewords and their stats are
  vastly different than what was available in **`1.08-1.09`**. 
- No **`players`** command, but you can use **`Singling`** for this feature.

#### Patch 1.08 (Wednesday, June 27, 2001)

This patch was selected because it is the first version of Lord of 
Destruction available after the Beta was over, and was also released on 
Release Day. Thus, anyone that connected to Battle.net was immediately 
updated to **`1.08`**. 

Given where **`1.07`** and **`1.08`** were in the development timeline, 
we may be able to consider this patch as a very late beta build. There 
are still many early expansion design decisions and behaviors (whether a 
bug or not) present in these patches which were changed in **`1.09`**. 
Some of these decisions, features, and quirks are listed below: 

- The majority of the Unique Items are the same as in **`1.07`**.
- There are more activated crafting recipes than in **`1.07`**, and 
  contains a lot of recipes that were better than and disabled immediately 
  in **`1.09`**.
- The Treasure Class system is complete but the Magic Finding is still
  essentially useless (works the same as in **`1.07`** but with higher
  breakpoints). There are still no **Diminishing Returns** on Magic Find so
  if you are comfortable using the [Dancing of the Souls Easter Egg](https://xyinn.org/diablo/videos/05.%20Dancing%20of%20the%20Souls%20Easter%20Egg.mp4),
  you can get infinite magic find and cause monsters to drop only uniques.
  This means that you can actually get a monster to drop the 1.08 version of Windforce.
- The Rack Running mechanics still work the same as **`1.07`**, with
  some exception for **`TC90`** items that need to be racked in a higher
  level area. Thus Rack Running is still possible and actually has
  better chances of dropping Uniques than **`1.07`** (**`1/800 vs 1/1000`**).
- Boss Drops are broken and only drop their Normal TC.
- Rare Jewels can get up to **`6`** Affixes.
- It's possible for Windforce to drop since the TC is fixed. Windforce
  also has different stats than the **`1.09`** version. So it is the
  only patch that you can acquire this particular Bow configuration.
  It's extremely hard for this bow to drop.
- Runeword stats are not saved, thus are regenerated per game.
- Runewords were only available on Battle.net. Thus you can use **`Singling`**
  to access them on Single Player.
- No **`players`** command, but you can use **`Singling`** for this feature.

#### Patch 1.09b (Wednesday, September 5, 2001) - Recommended

This patch was picked because it is the most stable and balanced version 
of the game after **`Lord of Destruction`** was released, but before the 
groundbreaking changes introduced in **`1.10`**. Thus, it is the 
definitive experience of the **`Original Expansion`** of Diablo II. 

This patch also introduced the **`players`** command and many other 
quality of life improvements and fixes. **`1.09b`** was also picked over 
**`1.09d`** because it contains **`players 64`** and working CtC. 
**`1.09d`** has broken CtC which means that you will see the animation 
of your CtC effect, but it actually won't do anything. 

#### Patch 1.10 (Tuesday, October 28, 2003) - Recommended

This patch was selected because it was the last and biggest update made 
directly by **`Blizzard North`** that brought Diablo II into a new era, 
which I'm labeling as: **`New Expansion`**. 

It was released two years after observing the **`1.09`** community, and 
released around **`3`** months after the [Blizzard North 
Exodus](https://en.wikipedia.org/wiki/Blizzard_North#History), where 
most of the key people left and formed **`Flagship Studios`**, 
**`Castaway Entertainment`**, and **`Hyboreal Games`**. [Peter 
Hu](https://www.diablowiki.net/Peter_Hu) was the Chief Architect for 
Patch **`1.10`** and from my conversations with David Brevik, Peter 
stayed behind to finish the patch. Afterwards, he left Blizzard North 
and joined Flagship Studios. 

Patch **`1.10`** massively redesigned and rebalanced the game, and for 
the most part is the Diablo II that we all know and love today. All 
further additions added to the game such as **`Respecs`**, **`Increased 
Rune Drop Rates`**, **`Faster Merc Leveling`**, **`Uber Tristram (Online 
Only)`**, and the removal of **`Iron Maiden`** from the Chaos Sanctuary, 
came after the Exodus. 

Some of the things introduced in this patch were:

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

##### Ladder Runewords Removed From Singling

Singling no longer provides **`Ladder Runewords`** for **`1.10`**. The 
reason for this is that **`Peter Hu`**, the Main Architect of 1.10, 
stayed behind at Blizzard North after the Exodus in order to finish the 
patch. The patch was released on **`October 28, 2003`**. Shortly after, 
Peter left Blizzard North and joined **`Flagship Studios`**. These 
runewords did not exist when **`1.10`** was released and given that the 
patch was released as is and also that there is no evidence suggesting 
Peter was in favor of them being released, they won't be included. The 
**`23`** new Ladder Runewords were introduced server side on **`July 8, 
2004`**, several months after Peter had left (Most likely around Q1 
2004). The new runeword combinations were finally published publicly on 
**`December 10, 2004`**. 

It sucks in a way to come to this conclusion since the ladder only 
runewords were definitely part of my childhood (I started playing during 
the first ladder season of **`1.10`**), but given the evidence, the 
history needs to be factually represented and properly documented in 
Singling. I believe the references below provide enough evidence to 
remove the Ladder Runewords from the project. As mentioned in the 
[Goals](#description--goals) section of Singling, Singling supports only 
**`Blizzard North`** developed versions of the game. When drawing the 
fine line of where exactly the history of **`Blizzard North`** ends, it 
isn't on [**`August 1, 
2005`**](https://en.wikipedia.org/wiki/Blizzard_North#History) when 
**`Blizzard`** announced that they were closing down the corporate 
vehicle of **`"Blizzard North"`**, but when the main people working at 
**`Blizzard North`** actually left. 

###### References For Ladder Runewords Decision

- [David Brevik discusses LOD and Patch 1.10](https://youtu.be/cuNgTnfk-wU?t=3992)
- [Ladder Runewords released server-side](http://www.theamazonbasin.com/wiki/index.php/Ladder#Rune_Word)
- [Post #10](https://web.archive.org/web/20210309030553/https://www.diabloii.net/forums/threads/new-stuff-for-new-ladder-23-new-runewords-if.219389/)
- [Post #5](https://web.archive.org/web/20210221120231/https://www.diabloii.net/forums/threads/new-rune-words.244633/)
- [Post #2](https://forums.d2jsp.org/topic.php?t=80220076&f=21&p=540231951)
	
##### Blizzard North / Flagship Studios Interviews and Presentations

- [David Brevik discusses Diablo was intended to be a Hardcore-only game from the beginning](https://youtu.be/rML7xVqaVr4?t=950)
- [Flagship Studios Developer Interview - Formation of FSS after Blizzard North Exodus](https://www.youtube.com/watch?v=-6AQZVru2to)
- [Mike Huang's Experience at Blizzard North](https://web.archive.org/web/20100224063807/http://diablo.incgamers.com/blog/comments/guest-article-remembering-blizzard-north-and-diablo-ii)

## Other

- [Basis for the introduction of Respecs in Diablo II (1.13c - March 23, 2010)](https://twitter.com/candlesan/status/1441315293909774337)

## References

- [Release Dates - 1](https://www.theamazonbasin.com/wiki/index.php?title=Patch)
- [Release Dates - 2](https://www.theamazonbasin.com/forums/index.php?/forums/topic/125365-diablo-ii-patch-dates/)
- [1.00 Info](https://web.archive.org/web/20210225030823/https://www.diabloii.net/forums/threads/the-time-travelers-vortex-part-2-a-guide-to-version-1-00.933726/)
- [1.05 Info](https://web.archive.org/web/20210629002420/https://www.diabloii.net/forums/threads/a-guide-to-classic-1-06b.745320/)
- [1.07 Info](https://web.archive.org/web/20210628123057/https://www.diabloii.net/forums/threads/repuszs-1-07-guide-repost.472485/)
- [1.08 Info](https://web.archive.org/web/20210225052946/https://www.diabloii.net/forums/threads/1-08-news-info-and-gossip.955142/)
- [1.09 Info](https://web.archive.org/web/20210628230751/https://www.diabloii.net/forums/threads/robbyds-time-travelers-guide-to-1-09-v1-1.753642/)
- [1.10 Info](https://web.archive.org/web/20210921181337/https://www.diabloii.net/forums/threads/1-10-faq-for-sp-v-2-0-repost.472493/)
- [Time Traveler's Vortex - Part 1](https://web.archive.org/web/20210628181556/https://www.diabloii.net/forums/threads/the-time-travelers-vortex-part-1-a-guide-to-spf-time-travel.933724/)
