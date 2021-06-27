## Cactus
##### By: Jonathan Vasquez [(fearedbliss)](https://twitter.com/fearedbliss)
##### Build: 2021-06-27-1500
##### [The Cactus Sanctuary](https://odysee.com/@TheCactusSanctuary:f) - Diablo I & II Time Travelling Videos - (Original, Not Resurrected)

## Main Menu (Example)

![Cactus](https://i.imgur.com/MipOjMu.png)

## Download

Visit the [Cactus (Core)](https://github.com/fearedbliss/Cactus-Core) repo
to download the source code for the version switcher. The Cactus Bundle
however is no longer available on GitHub but can be downloaded directly from my server
(uptime is not guaranteed). [7-Zip](https://www.7-zip.org/download.html) must be
used to extract the archive since I'm using high compression. All releases are
hashed and PGP signed with the key: **`34DA 858C 1447 509E C77A D49F FB85 90B7 C4CA 5279`**,
which can be easily found at the link below. 

### [Download Cactus](https://xyinn.org/diablo/Cactus.7z)
### [PGP Public Key](http://keys.gnupg.net/pks/lookup?op=get&search=0xFB8590B7C4CA5279)
### [Latest Release Hash](https://xyinn.org/diablo/Cactus.7z.SHA256.txt)
### [Latest Release Hash Signature](https://xyinn.org/diablo/Cactus.7z.SHA256.txt.sig)

## Description / History

Cactus started out as just a simple application that allowed you to 
easily and efficiently Time Travel between every version of Diablo II 
that ever came out, while maximizing disk space and enabling full 
character isolation between versions. However, even though Cactus itself 
still is just that, the Cactus Repository has evolved to become a 
centralized and historical archive, that aims to preserve every single 
Diablo II version that exists (**`Official Retail`** and **`Official Beta`** 
Releases). Cactus is a complete rewrite from scratch of my previous 
application called: **`Bliss Version Switcher`**. However, since Cactus is 
written in C#, it behaves as a native Windows application and allows it 
to integrate natively with the system. On the other hand, Bliss Version 
Switcher was written in Java and thus there were many limitations that 
lead to the Cactus rewrite.

This repository also includes several other utilities that I have either 
created or collected, which can help you play **`Vanilla`** Diablo II 
better. All Cactus Platforms are **`Vanilla`** by default. The only fix 
I made to all Platforms below **`1.12`** is to remove the CD requirement 
since modern computers no longer have a CD drive (Blizzard already did 
this exact thing for **`1.12+`**). Other than that, the only other 
modifications I provide are through **`Singling`**, which is 
**`completely opt-in`**, and only contains
**`non-gameplay modifications for Single Player and LAN`**, things like:

- Players Command (1.00 - 1.08) [(Video)](https://odysee.com/@TheCactusSanctuary:f/37_-Diablo-II--Players-Command-for-1.00%2C-1.05b%2C-1.07%2C-and-1.08-now-available-in-Singling-_-Cactus.-y-5YFUf5ibQ:0)
- CPU Fixes (Main Menu, Single Player, and LAN)
- Ladder Runewords 
- Multiple Instances
- Hardcore Character Creation (w/o needing to beat Softcore)
- Faster LAN Game Creation/Joining
- Scrolling Letters Fix
- MPQ Fix
- FPS Unlock
- Disabled Battle.net Button (So you don't get banned or accidentally update your game)
- Skipped Introduction Cinematics

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

Furthermore, if you will be playing online, you should make a copy of 
the Vanilla Platform and use that one to connect to Battle.net (for 
example, copying the **`1.14d`** platform and calling it something like 
**`1.14d BNET`**). You can use your other platforms with the Singling 
changes for local play. For a detailed overview, caveats, and patch 
rationale, you can read the Singling [README](README-SINGLING.md). 

Lastly, the **`cnc-ddraw`** video renderer is provided to improve video 
compatibility for all versions between **`1.00 - 1.13d`**. Blizzard 
removed **`DirectDraw`** support starting with **`1.14`**, and thus 
Cactus will only provide video support for versions before that. 

Cactus requires a purchased copy of Diablo II **`(Original, Not Resurrected)`**
from Blizzard in order to have all of the game assets stored in the 
MPQs. Once you have these, they will be re-used for all Cactus 
Platforms. 

For further information, please read the documentation below for 
anything you are interested in exploring.

## Cactus Repository

The following opt-in modifications and utilities are available in this repository:

#### [Singling](README-SINGLING.md)

A collection of non-gameplay modifications and fixes in order to improve the
Vanilla Diablo II Single Player & LAN Experience.

To use Singling, simply copy the Singling files for the version you want to
play from the **`2. Singling/1. Files`** folder, and replace the ones for
the equivalent version in your Platforms directory. To revert, use the files
in **`2. Singling/2. Stock`** instead.

#### [Renderers](README-RENDERERS.md)

Cactus includes and promotes the **`cnc-ddraw`** video renderer for 
Diablo II versions **`1.00 - 1.13d`**, which can help you run the game 
on newer systems with a higher window resolution (not a higher internal 
resolution), and the ability to use shaders to upscale the quality of 
the graphics in the game. Since Blizzard removed **`DirectDraw`** 
support in **`1.14+`**, you'll need to find an alternative video 
renderer for those versions. 

Please read the [**`README-RENDERERS`**](README-RENDERERS.md) for 
further explanation on this, for information on how to set it up, or for 
any known technical limitations. Definitely read the 
**`Recommendations`** section at least, or you will most likely 
encounter crashes if you've never played versions before **`1.14`** 
before. Blizzard has done major changes with how video configuration 
works starting in **`1.14`**. 

- [**`cnc-ddraw`**](https://github.com/CnCNet/cnc-ddraw) - This renderer
  reimplements the DirectDraw API for GDI, OpenGL, and Direct3D to improve
  compatibility with Windows XP - 10, and Wine. This renderer also supports
  the use of custom shaders - which will allow you to upscale the game so it
  looks a lot better - and even provides hotkeys (such as **`[Alt] + [Enter]`**)
  to switch between full screen and window mode.

## License

Released under the [Apache License 2.0](LICENSE.txt).

## Requirements

- .NET Framework 4.6.1 +

## Installation Instructions

### Install Cactus And Prepare MPQs

This section will help you install Cactus to the correct location and also help you
fix your MPQs so that they are compatible with the older versions of Diablo II.

**`Note:`** This fix is only needed if you want to play versions **`1.08 - 1.13d`**,
   if you are not planning to play those versions, you don't need to fix your MPQs.
   
1. Copy all of the files in the **`1. Files`** folder into your Diablo II root folder.
2. Run the **`FIX_MPQS_RUN_AS_ADMIN.bat`** inside the **`MpqFixer`** that you copied, as
   **`Administrator`**.

### Adding/Running A Platform

1. Run **`Cactus.exe`**
2. Click **`Add`**
3. Type in the name of the Platform you want to run. This should match a folder in the **`Platforms`**
   folder. (Example: If you want to run **`1.09b`**, type **`1.09b`**).
4. Enter the path to the executable you want to launch in your Diablo II **`root`** folder.
   Cactus copies all of the files from the **`Platforms/[NAME]`** folder to the Diablo II root folder,
   so most of your entries will have identical paths (Example: **`D:\Games\Diablo II\Game.exe`**).
   Do not put something that points to an executable in the **`Platforms`** folder since that will not work
   and will give you an **`Object reference not set to an instance of an object`** error. The executable has
   to be in the root of the Diablo II folder as described above.
5. Enter the Flags you want (Example: **`-ns`**)
6. Make sure **`Expansion`** is selected (Unless you are playing **`1.00-1.06b`** or didn't purchase **`Lord of Destruction`**).
7. Click **`Add`**.
8. Select your newly added Platform and press **`Launch`**.

The game should start. If you are having video issues, please make sure you
have read the [**`README-RENDERERS`**](README-RENDERERS.md) and ensure that
it was configured properly.

## Moving Cactus To A New Computer

If you want to move all of your Platforms, Characters, and Diablo II folder
to another machine, you will need to:

1. Copy your entire Diablo II folder to your new machine.
2. Edit the **`Entries.json`** file and change the **`Path`** for all of your entries
   so that it now has the **`Path`** on your new machine.
   - The **`Base Directory`** for all Paths need to match. The exes can be different.
   		- GOOD: **`D:\Games\Diablo II\Game.exe`** and **`D:\Games\Diablo II\SomeOther.exe`**.
   		- BAD: **`D:\Games\Diablo II\Game.exe`** and **`D:\Diablo Immortal For PC\Game.exe`**.
3. Open **`Cactus`** and edit the **`Last Ran Platform`**.
4. Uncheck the **`Last Ran`** box and Click **`Edit`**.
5. Now **`Launch`** whatever Platform you want.

Unchecking the **`Last Ran`** box will cause Cactus to reconfigure itself (Including registry locations).

## Updating Files In The Platforms folder

If you update any files in your Platforms folder, then uncheck the **`Last Ran`**
box from the corresponding platform, and run it again. This will cause Cactus
to re-install the files with the new ones.

## OMAHGOD! My Characters Are Gone! Cactus Deleted Them!!!

Cactus comes with [built in safety features](https://github.com/fearedbliss/Cactus-Core/blob/master/Cactus/FileGenerator.cs#L37)
specifically designed to protect critical directories and files, which 
includes the save directories. Thus it is impossible for Cactus to have 
deleted them. Cactus also only operates within the Diablo II root 
directory so it also wouldn't be possible for Cactus to delete saves 
that are in **`1.14d+`**'s new save directory that is in your personal 
folder. 

Since Cactus is a **`Version Switcher with Full Character and Version Isolation`**,
it will update the registry location of where the game should look for 
the saves. For example, if you are playing a **`Platform`** called 
**`1.05b (Chinchilla)`** (The files for this Platform would logically be 
located under **`Platforms/1.05b (Chinchilla)`**), then Cactus will save 
your characters in the **`Saves/1.05b (Chinchilla)`** directory located 
inside your Diablo II folder. So when the game starts, your characters 
are properly isolated and protected. If this is the first time you 
launched a game with Cactus, and you previously just had a regular 
Diablo II installation, then it would seem as if all your characters got 
deleted, or magically dissapeared. However, they are simply located in 
the original location that your computer saved them to. If you were 
playing **`1.14d+`**, they most likely are located at: 

**`%USERPROFILE%/Saved Games/Diablo II`** 

If you were playing **`1.13d`** or below, they are inside the Diablo II 
folder itself under a folder called **`save`**. 

Lastly, always remember to keep backups when running Third Party Tools 
or Modifications. 

## Screenshots

![1.00](https://i.imgur.com/uugMn48.jpg)
![1.05b](https://i.imgur.com/901u4V7.jpg)
![1.07](https://i.imgur.com/zHD9s5L.jpg)
![1.08](https://i.imgur.com/sUiFKqN.jpg)
![1.09b](https://i.imgur.com/JZ9bIOy.jpg)
![1.10](https://i.imgur.com/Vw4yaDM.jpg)
![1.13d](https://i.imgur.com/XiQheXy.jpg)
![1.14d](https://i.imgur.com/pojq3Jw.jpg)
