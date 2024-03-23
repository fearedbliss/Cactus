# Patch Notes

This will contain a log of changes I make over time, but won't contain any
minor documentation or textual changes that are made in between releases.
I may add something to the notes if I feel it's significant enough to be
mentioned. Due note that when I make textual or other minor changes, I may
re-release the archive with the same version number to maintain up-to-date
documentation in the published packages.

## 2024-03-23-1400

- My auditing for additional addons that were installed by external packagers
  (that most likely weren't in the original mod) is now complete. Any mods that
  still have **PlugY**, or other addons, are there because the Author explicitly
  included it, or there is something in the documentation that references those
  addons. Besides these two scenarios, an addon is only included if there is a
  technical limitation where using an addon is required to get the mod to
  function. This has been previously mentioned.
	- Removed **PlugY** from **Ancestral Recall (1.10)**.
	- Removed **PlugY** from **Back to Hellfire (1.02)**.
	- Removed **PlugY** from **Blackened (3.5 Beta)**.
	- Removed **PlugY** from **Duel Mod (1.0.0)**.
	- Removed **PlugY** from **OBLIVION AfTerStoRy (3.0)**.
	- Removed **PlugY** from **Pandora's Trials (1.1)**.
	- Removed **PlugY** from **Requiem of Sorrow (6.08)**.
	- Removed **PlugY** from **Underworld (2.9)**.
	- Removed **PlugY** from **You Gotta Be Kidding Me (1.11b)**.
- Cleaned up, and updated documentation for **Genesis (2.0+)**.
- Renamed all **Year (Initial Released)** fields to **Year Released**.

## 2024-03-22-2000

- Ported **Pagan Heart (0.995b)** to Cactus at **Platinum** level.
- Ported **Netherworld Rises (0.4.0S)** to Cactus at **Platinum** level.
- Ported **Blazing Fire (4.1F)** to Cactus at **Platinum** level.
- Ported **Rebirthe (0.05.1)** to Cactus at **Platinum** level.
- Ported **Blackened (3.5 Beta)** to Cactus at **Platinum** level.
- Re-ported **Underworld (2.9)** to Cactus at **Platinum** level using more
  original sources from the English edition by Hades. Thus I'm dropping the
  Russian version of the port.
- Ported **The Midlands (0.22c)** to Cactus at **Platinum** level.
	- The included **PlugY 9.00** files are incompatible with its base platform
	  of **1.13c**. Furthermore, testing **14.03** ended up yielding some edge
	  cases where skills wouldn't reset properly. So I've deleted it. I have a
	  strong feeling that a lot of D2SE packagers are bundling PlugY (and other
	  files) into mods that originally didn't have them. Due to this, I'll
	  probably need to start auditing existing platforms, and removing the
	  PlugY versions they have, if necessary.
- Ported **Darkness Weaves (2.0)** to Cactus at **Platinum** level.
- Ported **Lament of Innocence (1.06a)** to Cactus at **Platinum** level.
- Ported **Doggy Mod (0.11 Beta 4)** to Cactus at **Platinum** level.
- Ported **Johnny's Mod (1.22 Beta)** to Cactus at **Platinum** level.
- Ported **Viva X-Files (1.08f)** to Cactus at **Platinum** level.
- Ported **World of Chaos (0.4 Beta)** to Cactus at **Platinum** level.
- Ported **Zenith Affliction (1.0)** to Cactus at **Platinum** level.
- New Version Available: **Middle Earth (1.92)**.
- Improved **The Sin War (3.50)** port, and updated documentation.
- Improved **The Fury Within - Awakening (Alpha 2)** port, updated
  documentation, and removed all addons that most likely weren't part of the
  original mod.
- I'll no longer be providing sources for incompatible mods.
- As mentioned in the comment for **The Midlands**, due to my assumption that
  D2SE packagers have been including PlugY, and other addons into their
  packages, where the original mod didn't include them, I'm no longer including
  PlugY and other addons that don't seem to actually be part of the original
  distribution of the mod. This change will be retroactive and I'll be removing
  these files from all mods over time.
- For any mods ported where I can't find the author/year/ or some other piece
  of information, a **`?`** will be used in its place.
- I've finished porting all of the mods that I wanted to, and that I was able
  to find across the internet. For my next phase, I've dropped any mod that I
  felt I no longer wanted to maintain, and this decision was based on a variety
  of reasons, including my own subjective reasons of how I felt towards the mod,
  and its relationship amongst the other mods in the tree.
  
  The following mods have all been dropped:

	- **Berserker (1.1)**
	- **Boss Hunter (1.00)**
	- **Brothers From Hell (3.0)**
	- **Days Of Purgatory (1.0)**
	- **Diablo II - Extended (1.08d)**
	- **Diablo II - Unforgiven (34)**
	- **Doggy Mod (0.11 Beta 4)**
	- **Dreamaker (2024-02-20)**
	- **FAITH (2.00)**
	- **Glory of Nephilim (2024-02-05)**
	- **Grail (1.11)**
	- **Hail To England (1.0.26.6 Beta)**
	- **Hard Day (1.3.2)**
	- **Have Fun! Mod II (Apocalypse T7)**
	- **Jaina's Mod (1.3)**
	- **Johnny's Mod (1.22 Beta)**
	- **Myth (1.5.6)**
	- **Necromanthus (2021-03-02)**
	- **Netherworld Rises (0.4.0S)**
	- **New Anti Balance (1.8.5 B)**
	- **Rebirthe (0.05.1)**
	- **Reckoning (1.1)**
	- **Rewakening (0.5 Final)**
	- **Rusifikator (5.02.2024)**
	- **SnMX (2.D1)**
	- **Synthesis (Alpha 4)**
	- **The Black Parade (Act 1)**
	- **The Era of Destruction (1.3.5)**
	- **The Puppeteer (0.98.29 - Realm Edition)**
	- **The Wrath (1.12)**
	- **Unholy Wars (2006-03-20)**
	- **UVLoD (2.02)**
	- **Viva X-Files (1.08f)**
	- **Zenith Affliction (1.0)**

## 2024-03-17-1200

- Updated Cactus to **2.6.4**, which contains an edge case bug fix for the
  Backup feature.
- Updated **cnc-ddraw** from **6.2.0.0** to **6.3.0.0**, and added
  **`jinc2-dedither.glsl`** to the **`Shaders/windowed`** directory.
- Removed **Battle for Elements** from the tree due to it having additional
  launchers which are not supported by Cactus. This means that the Cactus
  port was providing an incomplete experience for the player.
- Restructured some of the Ports Collection pages/layout, and created a
  dedicated [**Removed Ports**](<./4. Ports/REMOVED-PORTS.md>) page.
- Made some improvements and simplifications to the **Windows 7** guide.

## 2024-03-16-1100

- I've removed the **`NET_Framework_4.6.2_Offline_Installer_for_Windows_7.exe`**
  from the bundle. I'm still explicitly supporting **Windows 7**, and am not
  dropping support for it. However, depending on how many dependencies your OS
  is missing, it could be tricky getting this running. I've written a guide to
  show people how to get Cactus working on Windows 7. You can find the guide
  [here](./INSTALLING-CACTUS-ON-WINDOWS-7.md). Dropping it from the bundle also
  reduces the file size significantly (from **`99 MB`** back down to the
  **`40 MB`** range - compressed).
- Renamed **`vc_redist.x86.exe`** to **`MSVC_x86_2015-2022_14.36.32532.exe`** in
  the **`3. Other`** directory.

## 2024-03-15-2030

- Ported **Baldur's Gate (1.06 Beta)** to Cactus at **Platinum** level.
- Ported **Middle Earth (1.8)** to Cactus at **Platinum** level.
- Ported **Paradox (0.2.7 Alpha)** to Cactus at **Platinum** level.
- Ported **Cryptforge (3a)** to Cactus at **Platinum** level.
- Ported **D2Scrabble (7a)** to Cactus at **Platinum** level.
- Ported **Ancestral Recall (1.10)** to Cactus at **Platinum** level.
- Ported **You Gotta Be Kidding Me (1.11b)** to Cactus at **Platinum** level.
- Ported **OBLIVION AfTerStoRy (3.0)** to Cactus at **Platinum** level.
- Ported **Duel Mod (1.0.0)** to Cactus at **Platinum** level.
- Ported **Diablo II: Unforgiven (34)** to Cactus at **Platinum** level.
- New Version Available: **Dark Alliance (0.05.07.01)**
- Adjusted the Cactus Ports Collection' Total Mod Counts. Mods within the same
  family will only be counted once. For example, if we have different versions
  of **Median / Median XL**, **Battle For Elements**, etc, they will be counted
  as a single unit rather than being split. This only applies if the mod was
  being developed by the same developer. If we have major differences, and people
  developing the project (i.e **Eastern Sun** and **Eastern Sun Rises**), this
  will still be considered two independent mods.
- Adjusting Cactus Ports Distribution policy a bit. I normally do not distribute
  or port mods that have an explicit message stating that they shouldn't be distributed.
  I'll be making an exception for very old mods that I no longer feel I can get
  consent for since I want to help to preserve these mods, and make them more
  easily accessible. I believe that if I was able to get in contact with
  the original author (after 20+ years), they most likely would agree as well.
  If you are the original author of a mod I ported, and you actually still don't
  want me to redistribute it after 2 decades, please message me, and I'll remove
  it. As of now, these policy change allows me to bring the following mods into
  the collection:
	- **D2Scrabble (7a)**
	- **Ancestral Recall (1.10)**

## 2024-03-11-2030

- Ported **Battle For Elements (1.80)** to Cactus at **Platinum** level.
- I'm happy to announce that **Brother Laz**'s **Median** and **Median XL**
  collection are now available on Cactus! I'm not a **Median / Median XL** player,
  however, I was able to review **Brother Laz**'s patch notes on his site, and
  carefully divided all of the patch history into specific eras, similar to what
  I did for the official versions of Diablo II when working to implement
  [Singling](https://github.com/fearedbliss/Cactus/blob/main/README-SINGLING.md)
  support. I believe this gives us a good snapshot of the mod throughout the years.
  The versions available are also based on if I could even find the files on the
  internet, and also picked the latest stable version from each of these eras,
  except for:

    - **`1.70 | Initial Release Version of Median XL`**
	- **`1.80 | First Stable Version Of The Initial Release`**
	
  This gives us the chance to experience the immediate release (similar to
  Singling providing **1.00** support despite it having lots of bugs, and then
  the **1.05b** release afterwards).
  
  Below are the ported versions, each intentionally using a **1.10** core:

	- **Median 2006 (v1.12)**
	- **Median 2007 (v1.31)**
	- **Median 2008 (v1.57b)**
	- **Median XL (1.70)**
	- **Median XL (1.80)**
	- **Median XL (1.99d)**
	- **Median XL (1.Z9)**
	- **Median XL (Omega v003)**

   Due note that **Median XL (2012 v005)** was already in the Cactus Ports
   Collection. If over time I feel that the version timeline could be split
   up in a better way, I'll make some updates to either add or drop particular
   versions, until the history is correct (if not already).
   I hope that you have a lot of fun ***Time Traveling*** within the
   **Brother Laz Era** of **Median / Median XL**.
   
   Since I'll be focusing on maintaining this era, I've dropped the
   **Median XL (Ultimative XVI)** port.

- Added groupings of related mods to make identification easier.
- The **Year (Initial Release)** field may also appear as **Year Released** if
  I have the year of when the specific patch came out. This is to continue to
  improve the clarity of what this field means.

## 2024-03-10-1400

- Ported **FAITH (2.00)** to Cactus at **Platinum** level.
- Ported **Necromanthus (2021-03-02)** to Cactus at **Platinum** level.
- Ported **Hell on Earth (2.9 Beta)** to Cactus at **Platinum** level.
- Ported **Unholy Wars (2006-03-20)** to Cactus at **Platinum** level.
- Ported **Berserker (1.1)** to Cactus at **Platinum** level.
- Ported **World Youth En (3.0 Remastered)** to Cactus at **Gold** level.

## 2024-03-09-2100

- Ported **Dreamaker (2024-02-20)** to Cactus at **Platinum** level.
- Ported **Jaina's Mod (1.3)** to Cactus at **Platinum** level.
- Ported **Genesis (2.0+)** to Cactus at **Platinum** level.
	- Fixed a porting bug where the Save Path wasn't being protected by Cactus.
- Ported **D2FC (Season 4)** to Cactus at **Platinum** level.
- Ported **Pandora's Trials (1.1)** to Cactus at **Platinum** level.
- Ported **UVLoD (2.02)** to Cactus at **Platinum** level.
- Ported **Reckoning (1.1)** to Cactus at **Platinum** level.
- Ported **Is Alive (27.9.2015)** to Cactus at **Platinum** level.
- Ported **The Black Parade (Act 1)** to Cactus at **Platinum** level.
- Ported **SnMX (2.D1)** to Cactus at **Platinum** level.
- Ported **Immersion (1.05 b104)** to Cactus at **Platinum** level.
- Ported **Seven Lances (1.30 Beta 2)** to Cactus at **Platinum** level.
- Ported **The Puppeteer (0.98.29 - Realm Edition)** to Cactus at **Platinum**
  level.
- Ported **Valhalla (5.03)** to Cactus at **Platinum** level.
- Ported **Perfect Drop Mod (1.07b)** to Cactus at **Platinum** level.
- Ported **Grail (1.11)** to Cactus at **Platinum** level.
- Ported **Trance (2015-12-26)** to Cactus at **Platinum** level.
- Ported **Glory of Nephilim (2024-02-05)** to Cactus at **Platinum** level.
- Ported **Have Fun! Mod II (Apocalypse T7)** to Cactus at **Platinum** level.
- Ported **Le Royaume des Ombres (6.00 Beta)** to Cactus at **Platinum** level.
- Ported **Le Royaume des Ombres (5.03)** to Cactus at **Platinum** level.
- Ported **Rewakening (0.5 Final)** to Cactus at **Gold** level.
- Fixed a minor porting bug with the **Hail To England (1.0.26.6 Beta)** platform.
- I've been thinking of my limited "convenience" installations for certain mods
  the past few days as I've been porting more mods, and decided that I don't want
  to get into the business of installing anything other than what the original
  modder intended (as I usually do) unless it's absolutely necessary to get
  the mod to even run in Cactus. I'll let each player decide what they want and
  customize their platforms to their liking. In a lot of mods, there is usually
  an intention by the author for what mods they want/expect their users to use.
  Sometimes you'll see a **`PlugY.dll`**, **`PlugY.ini`**, or some other PlugY
  file (or any other file for any mod system like D2Mod or BaseMod). In these
  cases I will provide the rest of the necessary files to get that feature
  running. However, if there are no traces for that intent, they won't be added.
  Due to this I've retroactively uninstalled PlugY (and anything else, if any)
  from the mods that I can remember I added stuff to. If I find any other mods
  I've added convenience additions to, I'll be removing them in a future update.
  At the moment the following mods were affected:
  	- **Perfect Drop Mod (1.07b)**
	- **Resurgence (R1.10.L.9)**
- Any mods not compatible with Cactus will no longer be documented, and I've
  removed them from the listings completely. If a mod isn't compatible and the
  author eventually wants to bring it to Cactus, they can do the work to make
  it compatible. I would rather spend the time I would have spent documenting
  why a mod isn't compatible, on getting more mods ported.
- The preview images in the Cactus Ports Collection main page have been removed.
  Since the number of mods ported over to Cactus has significantly increased,
  loading all of those images for every request was getting a bit crazy. The
  images will now only be loaded when you click into the port entry. This also
  provides a cleaner and faster navigation experience.
- Restructured the Cactus Ports Collection front page a bit to allow for quicker
  navigation.
- Now that there are more than **50+** mods successfully ported to Cactus, I
  will be highly selective on what I bring into my tree, and will also start
  retroactively looking at all of the currently ported mods, and dropping any
  mods I don't feel are contributing enough of a difference for me to include
  and maintain them in my tree. A lot of mods sometimes are just repackaging of
  the same standard popular components with only a little bit of a difference
  based on personal taste. This is perfectly fine, and I still encourage everyone
  to express themselves by developing these mods, and distributing them as Cactus
  platforms, but I won't be porting or maintaining them.
  
  Ultimately, I do prefer to have a decentralized community where different
  people can maintain their own Cactus trees independently. This allows for
  differences of opinion, and allows for redundancy of the Cactus platform files
  (and potentially their sources depending if the individual maintaining their
  own Cactus tree decides they want to back those up as well). We are not
  necessarily in competition with each other (well.. we are in a friendly way
  haha), so we can ultimately, together, raise the standard of the Diablo II
  (Original) modding scene, in an independent and distributed fashion.

  Due to the above, I've also decided to no longer link any externally maintained
  mods, and simply focused on my personal tree. I've dropped the only
  currently externally listed mod which is **Diablo 2 Enhanced Edition**.
- Removed the **Not Compatible** level from the Compatibility Key since I don't
  list incompatible mods anymore.
- Removed the **Silver** and **Bronze** levels from the Compatibility Key. If a
  mod cannot be launched via Cactus, or saves cannot be protected, the mod will
  not be ported or listed in this collection. This means that only **Platinum**
  and **Gold** level mods will be available. This establishes a better safety
  floor for any user using ported mods in my tree.

## 2024-03-04-2000

- Upgraded **Cactus** to **2.6.3**, which contains a few bug fixes for some edge
  case scenarios.
- Updated **cnc-ddraw** from **6.1.0.0** to **6.2.0.0**.
- Ported **Battle For Elements (1.70)** to Cactus at **Platinum** level.
- Ported **E=mc2 (R2019 - Heroic Edition)** to Cactus at **Platinum** level.
- Ported **The Era of Destruction (1.3.5)** to Cactus at **Platinum** level.
- Ported **New Anti Balance (1.8.5 B)** to Cactus at **Platinum** level.
- Made some porting fixes to **D2 - Ironman (6.04 Beta)**.
- Made some porting fixes to **Boss Hunter (1.00)**.
- Made some porting fixes to **Diablo II - Extended (1.08d)**.
- Made some porting fixes to **The Sin War (3.50)**.
- Upgraded **Succulent** from **2024-02-12-2000** to **2024-03-04-0800**.
- Adjusted **Disotheb** version from **2 - Hotfix 4** to just **Hotfix 4**, and
  made some minor cleanups.
- I've made the following adjustment to all mods:
	- The **`MOD.md`** file will now just be called the same as the mod file
	  displayed in the repo. These helps me maintain them a bit easier since
	  there is less renaming. It's also better in that sense that it helps
	  reduce file collisions a bit if we are extracting multiple mods to the
	  same folder.
	- All platforms names now also include the version information. Before, only
	  a few mods with the same name would have this feature due to naming
	  collisions. The version helped namespace them to eliminate that. However,
	  this is now the default across the board. However, there are some exceptions.
	  The mod does not need to be namespaced if it was intentionally designed to
	  be upgraded in place, or was intentionally packed and designed that way.
	  In these cases, we can omit the version info and use a flat name in order
	  to allow the user an easier upgrade path. If I cannot reconcile the names
	  without other issues, I'll default to namespacing them again.
	- I've removed any remaining unnecessary files in the **`Other`** folder.
	  If there are no other misc files to pack, then this directory will be
	  omitted.
	- I've started to improve the ***sane defaults*** that mods come with.
	  Usually the defaults provided by upstream are good enough, but if there
	  are some small tweaks I can make to improve cohesiveness within the Cactus
	  ecosystem, I'll make those changes.
	- I've started removing any outdated installation documentation that was
	  provided by upstream but that may cause confusion for Cactus users (given
	  that Cactus already handles all of that stuff). I normally try to quote
	  the author's directly and exactly, but in these cases, I think it makes
	  sense to error on clarity. If you need the original quotes, please open
	  up the original source archives I'm also providing (if available).
	- For some mods (like **Resurgence**), I've included **PlugY** out of the
	  box and pre-configured. I normally don't like adding extensions to other
	  people's mods since I want to keep the experience as close to what they
	  intended as possible. However, after researching online, it seems there
	  were users that wanted this and were struggling to get it set up. This is
	  now included. However, if the original author's contact me and object to
	  a particular extension, I'll revert that change. In the **Resurgence**
	  case, this was also done because the mods in the Cactus Ports Collection
	  are primarily focused on ***Offline Single Player Mods***, so it makes
	  sense to make some changes in alignment with that goal.

## 2024-03-01-2210

- Ported **Hard Day (1.3.2)** to Cactus at **Platinum** level.
- Ported **Synthesis (Alpha 4)** to Cactus at **Platinum** level.
- Ported **The Wrath (1.12)** to Cactus at **Platinum** level.
- Ported **Disotheb (2 - Hotfix 4)** to Cactus at **Gold** level.
- Ported **Resurgence (R1.10.L.9)** to Cactus at **Gold** level.
- **Hellfire II: Guild Pact (1.04 - Beta 55)** is **Not Compatible** with Cactus.
- **Hellfire II: FFXIV Shadowbringers (Beta 54)** is **Not Compatible** with Cactus.
- I'll only be keeping the latest version of a particular mod (which is usually
  what I've already been doing). However, I'll keep an additional version of a
  mod if there is a good reason. For example, the **Median XL (2012, v005)**
  and **Median XL (Ultimative XVI)** are good examples. Due to this, I'll be
  dropping the following mods:

	- **Median XL (1.3.2) (Gold)**
- Added sources links related to Microsoft requiring online activation during
  Windows 11's OOBE stage to the **Windows 11+ will not be supported** section
  of the Cactus documentation. I will not accept the premise that I need to use
  a Microsoft Account, or require online activation at the OOBE stage, for me to
  use my own computer, and I definitely won't accept the use of ***workarounds***
  to bypass that requirement as a justification to use that OS. That requirement
  should not be there in the first place. This is the same thing Microsoft
  already forces people to do on the Xbox One. When you first buy the console,
  one of the first things you need to do is log into their servers. Your console
  is useless until you do that. That's unacceptable. I'm not surprised they are
  moving in that direction with Windows in general, and I'm not accepting it.

	- [**Source 1 - February 16, 2022 - Windows 11 Insider Preview Build 22557**](https://blogs.windows.com/windows-insider/2022/02/16/announcing-windows-11-insider-preview-build-22557/)

	```
	Similar to Windows 11 Home edition, Windows 11 Pro edition now requires
	internet connectivity during the initial device setup (OOBE) only. If you
	choose to setup device for personal use, MSA will be required for setup as
	well. You can expect Microsoft Account to be required in subsequent WIP
	flights.
	```

	- [**Source 2 - May 5, 2022 - Windows 11 Insider Preview Build 22616**](https://blogs.windows.com/windows-insider/2022/05/05/announcing-windows-11-insider-preview-build-22616/)

	```
	Previously, we shared new requirements for internet and MSA on the Windows 11
	Pro edition. Today, Windows Insiders on Windows 11 Pro edition will now
	require MSA and internet connectivity during the initial device setup (OOBE)
	only when setting up for personal use. If you choose to setup device for Work
	or School, there is no change, and it will work the same way as before.
	```

## 2024-02-26-2000

- Ported **Myth (1.5.6)** to Cactus at **Gold** level.
- Ported **Brothers From Hell (3.0)** to Cactus at **Gold** level.
- Ported **Boss Hunter (1.00)** to Cactus at **Platinum** level.
- Renamed **Mod Database** to **Cactus Ports Collection**, inspired by the
  [FreeBSD](https://freebsd.org/) Ports Collection, and
  [Gentoo](https://gentoo.org/) Portage Tree).
- Updated the [**Cactus Setup & Demo Video (2.6.2+) (37 Minutes)**](https://xyinn.org/diablo/videos/01.%20Cactus%20Installation%20Video.mp4)
- Added **Fair Use** exception to copyrighted material porting advice. IANAL though,
  so if push comes to shove, I'll drop the mod.

## 2024-02-25-1630

- Ported **Eastern Sun (3.00)** to Cactus at **Platinum** level.
  
  Due to this, I've removed the **Eastern Sun (3.00 R6D)** from the
  **Not Compatible** list since this entry will replace that entry.

- Ported **Rusifikator / Русификатор текста (5.02.2024) (Russian)** to Cactus at
  **Platinum** level.
- Ported **The Fury Within - Awakening (Alpha 2)** to Cactus at **Platinum** level.
- Re-did the **Back to Hellfire (1.02)** port again and the compatibility has now
  increased from **Bronze** to **Platinum**.
- Renamed the **Mod Database Index** to **Mod Database**.
- All entries in the mod database will now have a **Year (Initial Release)** field
  to document the historical beauty. This field stands for the year the mod itself
  was originally released, not when the specific patch was released. However, if
  you are making a completely new mod, you can use the year of when you released
  the patch so that over time this value continues to get more accurate.
- Removing authors from file names and mod database routing page since this was
  making the URLs, folder paths, and listing strings too long. The authors are
  already credited and listed in every **`MOD.md`** file in the **`Author(s)`**
  section.
- I'll no longer be including version information for externally hosted mods
  since I won't be able to keep track of updates. I'll still include the version,
  hash, and any other info I collected from the last time I tested it.
- Repacked all platforms, and moved misc files into the **`Other`** directory,
  since the root of the platform should only contain files relevant for game
  operation. This also makes it easier to debug it since we don't have any
  non essential stuff / spam at the platform core.
- Downgraded **Hellfire II - Lazarus (Beta 4 - 06.2113)** from **Platinum** to
  **Gold** since I found that it includes a Cactus Protected File (**`D2Music.mpq`**).
  This doesn't seem to be causing issues but that means you won't get the full
  musical experience the modder intended.
- Fixed an issue with the **The Sin War (3.50)** port that prevented **PlugY**,
  **BaseMod**, and **SGD2FreeRes** from loading.

## 2024-02-23-2200

- Ported **D2: Ironman (6.04 Beta) - Hash** to Cactus at **Platinum** level.
- Ported **Underworld (2.9) - Hades (Russian)** to Cactus at **Platinum** level.

   This is the first mod ported to Cactus that's in Russian (and also the first
   in a non-English language). The mod seems to have originally been made in 2005
   and it's difficult to find information about it. Regardless, I'm happy to have
   got it running, polished, and helping with its preservation. Hopefully it can
   bring happiness to the Russian community. If there are any other Diablo II
   mods in ***any*** language, please email me and I can help try to bring
   them over when time permits.

- Ported **Diablo II - Extended (1.08d) - VixyPlaying** to Cactus at
  **Platinum** level.
- Fixed Mod Database preview images being stretched on mobile.
- Continued improving the Mod Database front page. Including clearly splitting
  ***internally hosted*** and ***externally hosted*** mods.
- Namespaced the following mods so they don't collide in the Platforms folder:

   - **Median XL (2012 v005)**
   - **Median XL (1.3.2)**
   - **Median XL (Ultimative XVI)**

  Moving forward, any mods containing the same platform name as another mod will
  have their platform names namespaced, preventing collisions. This collision
  prevention can only be guaranteed for ***internally hosted mods***.
- Added note about **sergi4ua's EQUINE, the Diablo 1 Mod Manager**
  (inspired by Cactus) to the **2024-02-19-1430** patch notes as historical
  information.
- Renamed the **Cactus Mod Database** to **Mod Database Index**.
- Updated Cactus to **2.6.2** which adds the **`default.key`** file to Cactus'
  protected files list. If there is a good reason for me not to protect this
  file, I'm open to removing it. Although I think most people may want this file
  to be kept, and not deleted by a platform.

## 2024-02-22-0200

- Ported **Reign of Shadow (0.92) - SpiKe.** to Cactus at **Platinum** level.
- Ported **Nezeramontias (1.09) - Acromatic Aria** to Cactus at **Platinum** level.
- Corrected the version of **Hell Unleashed** from **1.21** to **1.21z**.
- Repacked all mods with new **`MOD.md`** format and deleted any files that
  weren't necessary, or that could cause potential issues
  (like **`glide3x.dll`**, **`D2VidTst.exe`**, if possible).
- Added an image to each mod at the **Mod Database** front page to make
  navigation and peak curiosity a bit easier.
- Updated Cactus to ***2.6.1***, which brings full protection of all Cactus
  provided files (shared resources like ***cnc-ddraw*** and
  ***DSOAL w/ OpenAL Soft***), including itself. For a full list of changes,
  please check out the [Cactus 2.6.1](https://github.com/fearedbliss/Cactus-Core/commit/aeebd4eb0bcad12e2d3689dd7d3399ac35df3827)
  release message.

## 2024-02-19-1430

- Ported **Requiem of Sorrow (6.08) - TalonRage** to Cactus at **Platinum** level.
- Created dedicated pages for every **Not Compatible** mod in the Cactus Porting
  Database in order to clean up the main database page and provide a smoother
  experience.
- Renamed the **Cactus Porting Database** to **Cactus Mod Database**.
- In addition to Cactus being a **A Modern Version Switcher and Character Isolator**,
  it will now also officially take on the responsability of being a **Mod Manager**.

  For a long time I've used Cactus for my own personal mod development, debugging
  Diablo II in an isolated and clean environment, and for maintaining
  [**Singling**](README-SINGLING.md), and
  [**Succulent**](https://github.com/fearedbliss/Succulent), however, I've been
  hesitant of calling it a Mod Manager since it wasn't designed with that
  responsability in mind. However, it turns out that if you implement a clean
  version switcher that focus on just switching the files around, and does not
  try to hijack any DLLs, or do any sort of game modifications, **and** if you
  also implement proper character isolation between these versions, then the
  natural side effect is that you can also automatically switch between mods as
  well.

  Since I've now successfully ported **11** mods to Cactus at the **Platinum**
  level (not including Succulent which was already a native Cactus platform),
  **6** mods to Cactus at the **Gold** level, and **1** mod at the **Bronze**
  level, created the [**Cactus Porting Advice**](<4. Ports/PORTING-ADVICE.md>) page for
  those interested in porting mods to Cactus, and have also provided an official
  (and pretty beautiful) [**Cactus Mod Database**](MOD-DATABASE.md) with dedicated
  pages for each mod, I'm ready to complete the Cactus ecosystem with
  ***Mod Management*** support.

  Funny enough, I actually found an old [**imgur**](https://imgur.com/gallery/yM4Hg2H)
  post I made on **May 25, 2018** where I called it:

  **`Cactus 1.1.0 - A Modern Diablo II Version Switcher & Mod Manager`**

  and uploaded a list of screenshots showing Cactus in the v1 days already
  switching mods, and being called a Mod Manager. Another interesting note is
  that a fellow Diablo player (***sergi4ua***) created a Diablo 1 Mod Manager,
  inspired by Cactus, **6 years ago**, which was also during **2018**.
  You can check out his mod manager here:

  - [EQUINE, the Diablo 1 Mod Manager](https://www.sergi4ua.com/equine/)
  - [EQUINE GitHub Repo](https://github.com/sergi4ua/equine)

  Overall, this will be a work in progress, where my porting suggestions, and
  other ecosystem improvements will continue to be refined. However, even after
  **24~** years after the game was originally released, the
  ***Diablo II (Original, Not Resurrected)*** ecosystem is better than ever,
  and I'm excited to see where everything continues to travel towards.

  I would like to thank again everyone in the [**Credits**](CREDITS.md) page for
  everything you've all done these past decades, and to all the Diablo II modders
  out there that modded and/or continue to mod this wonderful game.

  ***Long Live Diablo II***

  fearedbliss

## 2024-02-19-0030

- Created dedicated pages for every mod in the Cactus Porting Database. This
  provides an enhanced browsing experience when looking for a mod to play and
  the pages contain important information and screenshots about the mod.

## 2024-02-18-1230

- Made some porting fixes to **`Zy-El (4.4c)`** which promotes it from
  **`Silver`** to **`Gold`** in the Cactus Porting Database.
- Made some porting fixes to **`The Hordes of Chaos (8.1 Beta)`** that promotes
  it from **`Silver`** to **`Platinum`** in the Cactus Porting Database.
- Ported **`Dark Alliance (0.05.06)`** to Cactus and made some porting
  fixes which promotes it from **`Silver`** to **`Platinum`**.
- Ported **`Escape from the Afterlife (1.56 - Hotfix 2)`** to Cactus and made some
  porting fixes which promotes it from **`Not Compatible`** to **`Gold`**.
- Added link to my mirror providing some tools and applications that I needed to
  port mods with more complicated setups.

## 2024-02-17-2030

- Added extensive documentation to all porting pages and to the README-RENDERERS
  page regarding potential video issues that may occur when using mods with Cactus,
  and how to recover from them.
- Ported more mods and added them to the database.

## 2024-02-17-1530

- Added a Patch Notes file to Cactus.
    - I added a bit of retroactive and cleaned up patch notes from my internal
      repo dating back to **2022-11-09-1230**. I stopped there because I could
      keep going back years, and this is good enough.
- Bumping version to re-align all of this retroactive patch notes into the
  package.

## 2024-02-14-0720

- Renamed **Cactus Porting Recommendations** to **Cactus Porting Advice**.

## 2024-02-12-1930

- Re-did Porting Database links and Rating System.

## 2024-02-11-1900

- Added the **Cactus Porting Recommendations** and **Cactus Porting Database**
  pages.
- Added my **Dark Island Strategy (Going Dark)** to docs.

## 2024-02-10-1100

- Updated **cnc-ddraw** from **5.8.0.0** to **6.1.0.0**.

## 2023-10-18-0900

- Updated **cnc-ddraw** from **5.6.0.0** to **5.8.0.0**.

## 2023-08-23-1430

- Including **.NET Framework 4.6.2** for ***Windows 7***.
- Moving **vc_redist.x86.exe** and **MPQ Fixer** to the **`3. Other`** folder.
- Rewrote initial installation section.

## 2023-08-23-0800

- Updated **cnc-ddraw** from **5.1.0.0** to **5.6.0.0**.

## 2023-06-06-0800

- Added **Windows 11+** not support disclaimer.

## 2023-05-01-0830

- Updated **DSOAL** and **OpenAL** binaries to a newer build.

## 2023-04-16-1900

- Updated included **Singling** to **2023-04-16-1900** which includes a new
  implementation of the Main Menu CPU fix which won't cause lag in versions
  before 1.10.

## 2023-04-01-2100

- Upgraded Cactus to **2.6.0**.
    - You can visit the [Cactus-Core](https://github.com/fearedbliss/Cactus-Core)
      repo to see the release notes.
- Updated **cnc-ddraw** from **4.9.0.0** to **5.1.0.0**.
- Fixed some broken links in the Singling Page by going via the wayback machine.
- Added **Backup Manager** documentation to the Cactus Main Page.
- Added the following shaders:
    - **`windowed/lanczos2-sharp.glsl`**
    - **`xbr/xbr-lv2-noblend.glsl`**

## 2023-03-15-0830

- Added **Unlocking All Cinematics** instructions.

## 2022-11-09-1230

- Updated **cnc-ddraw** from **4.4.7.0** to **4.9.0.0**.

***and the rest is history ...***