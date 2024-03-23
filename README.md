## Cactus <img src="https://i.imgur.com/mSwZJmr.png" height="35"/>

***A Modern Version Switcher, Character Isolator, and Mod Manager for Diablo II (Original, Not Resurrected)***

***By: Jonathan Vasquez (fearedbliss)***

***Build: 2024-03-23-1400***

[**Patch Notes**](PATCH-NOTES.md) | [**Videos**](https://xyinn.org/diablo/videos) | [**Ports Collection**](<./4. Ports/PORTS-COLLECTION.md>)

## Download

The Cactus (Core) source code can be downloaded at the
[Cactus (Core)](https://github.com/fearedbliss/Cactus-Core) repo.

The complete Cactus package is available as a direct download from my server
(uptime is not guaranteed). [7-Zip](https://www.7-zip.org/download.html) must be
used to extract the archive since I'm using Ultra compression. All releases are
hashed and PGP signed with the key: **`34DA 858C 1447 509E C77A D49F FB85 90B7 C4CA 5279`**,
which can be found at the link below.

- ### [Download Cactus](https://xyinn.org/diablo/Cactus.7z)
- ### [PGP Public Key](https://keys.openpgp.org/search?q=34DA+858C+1447+509E+C77A+D49F+FB85+90B7+C4CA+5279)
- ### [Latest Release Hash](https://xyinn.org/diablo/Cactus.7z.SHA256.txt)
- ### [Latest Release Hash Signature](https://xyinn.org/diablo/Cactus.7z.SHA256.txt.sig)

## License

Released under the **[Simplified BSD License](LICENSE.txt)**.

## Requirements

- **Windows 7 or 10 Only. [11+ will not be supported.](#windows-11-will-not-be-supported)**
- **.NET Framework 4.6.2+ (Cactus)**
- **Visual C++ 2015 - 2022 Redistributable (x86) (DSOAL w/ OpenAL Soft)**

## Screenshots

### Light Mode
![Cactus](https://i.imgur.com/Vni33AK.png)

### Dark Mode
![Cactus](https://i.imgur.com/WEzmHxC.png)

### Out Of The Box Experience
![Cactus](https://i.imgur.com/8MWskJQ.png)

### Settings (19 Material Design Colors Available + Light/Dark Mode)
![Cactus](https://i.imgur.com/mCaLfkv.png)

### Add Entry
![Cactus](https://i.imgur.com/CiY58Da.png)

### Edit Entry
![Cactus](https://i.imgur.com/ooiBWnH.png)

## History

Cactus started out as just a simple application that allowed you to
easily and efficiently Time Travel between every version of Diablo II
that ever came out, while maximizing disk space, and enabling full
character isolation between versions. However, even though Cactus itself
still is just that, the Cactus Repository has evolved to become a
centralized and historical archive, that aims to preserve every single
Diablo II version that exists (***Official Retail*** and ***Official Beta***
Releases), and has also become an ecosystem where mod developers can distribute
their mods on. Cactus is a complete rewrite from scratch of my previous
application called ***Bliss Version Switcher***. However, since Cactus is
written in C#, it behaves as a native Windows application and allows it
to integrate natively with the system. On the other hand, Bliss Version
Switcher was written in Java and there were many limitations that lead to the
Cactus rewrite.

This repository also includes several other utilities that I have either
created, or collected, which can help you play ***Vanilla*** Diablo II
better. All Cactus Platforms are ***Vanilla*** by default. The only fix
I made to all Platforms below 1.12 is to remove the CD requirement,
since modern computers no longer have a CD drive. Blizzard already did
this exact thing for all versions starting with 1.12. Other than that,
the only other modifications I provide are through
[**Singling**](README-SINGLING.md), which only contains
***non-gameplay modifications*** and is ***completely opt-in***.

If you will be playing online, you should make a copy of the Vanilla Platform
and use that one to connect to Battle.net (for example, copying the **1.14d**
platform, and calling it something like **1.14d BNET**). You can use your other
platforms with the Singling changes for local play.

The **cnc-ddraw** video renderer, and **DSOAL w/ OpenAL Soft** are included as
a ***shared resource*** for all platforms. cnc-ddraw is provided to improve
video compatibility for all versions between 1.00 - 1.13d. Blizzard removed
DirectDraw support starting with 1.14, and thus Cactus will only provide
video support for versions before that. DSOAL w/ OpenAL Soft is provided to
enable you to use the following lost in-game sound functionality: 3D Sound,
Environmental Effects, 3D Bias.

Cactus can also be used for ***easily playing mods in an isolated and safe fashion.***
Please check out the ***[Cactus Ports Collection](PORTS-COLLECTION.md)*** for a
list of mods that have either been ported to Cactus, attempted to be ported to
Cactus, or were made to run on Cactus natively. You'll also find the compatibility
statuses for each mod listed, and a dedicated page containing important info.

Cactus requires a purchased copy of ***Diablo II (Original, Not Resurrected)***
from Blizzard in order to have all of the game assets stored in the MPQs. Once
you have these, they will be reused for all platforms.

For more information, please read the documentation below for anything you are
interested in exploring.

## Cactus Repository

The following opt-in modifications and utilities are available in this repository:

### [Singling](README-SINGLING.md)

A collection of non-gameplay modifications and fixes in order to improve the
Vanilla Diablo II Single Player & LAN Experience.

To use Singling, simply copy the Singling files for the version you want to
play from the **`2. Singling/1. Files`** folder, and replace the ones for
the equivalent version in your Platforms directory. To revert, use the files
in **`2. Singling/2. Stock`** instead.

### [Renderers](README-RENDERERS.md)

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

### [3D Sound (DSOAL w/ OpenAL Soft)](README-3D-SOUND.md)

Cactus includes the files required to allow you to enable the following
lost in-game sound functionality: **`3D Sound`**, **`Environmental Effects`**,
and **`3D Bias`**.

Please read the [**`README-3D-SOUND`**](README-3D-SOUND.md) for more information.

## Installation Instructions

- [**Cactus Setup & Demo Video (2.6.2+) (37 Minutes)**](https://xyinn.org/diablo/videos/01.%20Cactus%20Installation%20Video.mp4)

### Required Files

After you finish installing Diablo II (or restoring the files from a backup),
you only need to keep the following files in your **`Diablo II Root Directory`**.
Everything else can be deleted since it will come from Cactus. Once you are done,
continue with the Cactus installation steps.

```
- D2.LNG
- D2Char.mpq
- D2Data.mpq
- D2Exp.mpq      (1.07+)
- D2Music.mpq    (Not needed for 1.00)
- D2Sfx.mpq
- D2Speech.mpq
- D2Video.mpq
- D2XMusic.mpq   (1.07+)
- D2XTalk.mpq    (1.07+)
- D2XVideo.mpq   (1.07+)
```

### Install Cactus, Dependencies, and Prepare MPQs.

This section will help you install Cactus to the correct location, its
dependencies, and also help you fix your MPQs, so that they are compatible with
the older versions of Diablo II. I only test on, and support **`Windows 7`**,
and **`Windows 10`**. However, these instructions may also work on versions in
between, but you may need to make some adjustments.

1. Copy all of the files in the **`1. Files`** folder into your
   **`Diablo II Root Directory`**.

	- It's important that Cactus runs from inside your
	  **`Diablo II Root Directory`**, or you will get weird behavior in various
	  situations like running **`-direct -txt`** mods, or taking screenshots.

1. If you need to fix your MPQs, then also copy the **`MpqFixer`** located in
   the **`3. Other`** directory into your **`Diablo II Root Directory`**. This
   fix is only needed if you want to play versions **`1.08 - 1.13d`** and you
   also happened to install Diablo II from the new Blizzard Installer. If you
   are not planning to play those versions, or you installed Diablo II from the
   original **`1.00, 1.03, 1.07`** discs, you don't need to fix your MPQs.

   You can then run the **`FIX_MPQS_RUN_AS_ADMIN.bat`** inside the
   **`MpqFixer`** directory that you copied, as **Administrator**.

1. Run the **`MSVC_x86_2015-2022_14.36.32532.exe`** file in the **`3. Other`**
   directory to install the required libraries for **`3D Sound`**. If you run
   the game without these being installed, you will get a **`VCRUNTIME140.dll`**
   error message.

   - **`(Windows 7)`** You will need to have **Service Pack 1** installed, or
     this step will fail. Follow the guide in the next step to get everything
	 working.
   - If you don't want this functionality, just delete the **`dsoal-aldrv.dll`**,
     and **`dsound.dll`** from your **`Diablo II Root Directory`**.

1. **`(Windows 7)`** Cactus requires **`.NET Framework 4.6.2`** to function,
   but that version does not come included in Windows 7 by default. You can
   follow my [Installing Cactus on Windows 7](./INSTALLING-CACTUS-ON-WINDOWS-7.md)
   guide to get this working.

### Adding/Running A Platform

1. Open **`Cactus`**.
1. Click **`Settings`** and set your **`Diablo II Root Directory`** to your Diablo II folder. **`(Example: C:\Games\Diablo II)`**
1. Click **`Add`**.
1. Type in the name of the **`Platform`** you want to run. This should match a folder in the **`Platforms`**
   folder. (Example: If you want to run **`1.09b`**, type **`1.09b`**).
1. **`Optional (Recommended)`**: Type in a **`Label`** for this platform. If you label your platform, it will have its own dedicated
   save directory, allowing you to have multiple entries using the same platform but with different save locations.
   If you don't use a label, all the characters with this platform name will be stored in the same location (flat structure).
   You can have multiple entries using the same platform with and without labels as well. A label cannot be
   removed from an entry once created, but it can be renamed. A label cannot be added to an entry once created.
1. Enter the name of your **`Launcher`**. **`(Example: Game.exe)`**
1. Enter the Flags you want (Example: **`-ns`**).
1. Click **`Add`**.
1. Select your newly added Platform and press **`Launch`**.

The game should start. If you are having video issues, please make sure you
have read the [**`README-RENDERERS`**](README-RENDERERS.md) and ensure that
it was configured properly.

**`NOTE`**: Make sure to leave the Cactus application running throughout your
play sessions (you can minimize it). Cactus keeps track of the running Diablo II
processes it launches as to protect you from accidentally switching to a different
platform, and causing your **`Save Path`** to be updated to an incorrect location.

## Windows 11+ will not be supported.

Due to Microsoft mandating people to have an online connection and a Microsoft
account for Windows 11 (at the OOBE stage), any version over Windows 10 will
not be supported. Given the Xbox One has the same type of requirement, I'm not
surprised Microsoft is going in that direction.

- [**Source 1 - February 16, 2022 - Windows 11 Insider Preview Build 22557**](https://blogs.windows.com/windows-insider/2022/02/16/announcing-windows-11-insider-preview-build-22557/)

```
Similar to Windows 11 Home edition, Windows 11 Pro edition now requires internet
connectivity during the initial device setup (OOBE) only. If you choose to setup
device for personal use, MSA will be required for setup as well. You can expect
Microsoft Account to be required in subsequent WIP flights.
```

- [**Source 2 - May 5, 2022 - Windows 11 Insider Preview Build 22616**](https://blogs.windows.com/windows-insider/2022/05/05/announcing-windows-11-insider-preview-build-22616/)

```
Previously, we shared new requirements for internet and MSA on the Windows 11
Pro edition. Today, Windows Insiders on Windows 11 Pro edition will now require
MSA and internet connectivity during the initial device setup (OOBE) only when
setting up for personal use. If you choose to setup device for Work or School,
there is no change, and it will work the same way as before.
```

Windows 10 Pro doesn't have this requirement at all, and is the OS I primarily
use on my gaming computer. Windows 10 Home does have this requirement though,
but can be bypassed by unplugging your internet connection before the OOBE.
***I'm including Windows 10 support due to there still being a direct path
to use the OS with no workarounds through the Pro edition.*** Windows 10 reaches
EOL on [October 14, 2025](https://learn.microsoft.com/en-us/lifecycle/products/windows-10-home-and-pro).

However, I have gone dark already using my **Dark Island** strategy, which
means that I'm using Windows exclusively in **Offline Mode**, with all forms
of communication to the public internet disabled. I never allowed it to reach
the internet from the very beginning, including during the installation stage.
I only play **Offline Single Player DRM Free Games**, so this strategy works
for me, and it also means that the EOL status of Windows 10 will have no
consequences for me. I'm basically using Windows like a N64 or Gameboy,
which is why I sometimes call this machine a Wintendo. I never needed
internet for those systems then, and still don't today, yet I can still use
and play those games decades later. Going dark years before the EOL, gives me
plenty of time to make sure that I backup everything that I need, to reproduce
my environment post EOL. If you are interested in my Dark Island strategy,
you can read the next section.

Furthermore, I will be exiting Windows development completely for newer versions
of Windows. I will continue to maintain Cactus/Singling/Etc for Windows 7 and 10.

Please do not file any bug reports if you are running my software on Windows 11+,
they will be promptly closed as **`NOT SUPPORTED`**.

### Dark Island Strategy (Going Dark)

With this strategy, what we want to do is block Windows from accessing the
internet, but we still want LAN communication (for sideloading games and
other applications). If you don't need LAN communication, then you can
just disable all of your network interfaces, and use an external drive to
load apps into your airgapped machine. This would be the best approach, but
a bit less convenient for sideloading. The LAN-only approach gives you a
good balance of external isolation and internal convenience. You could
also do this at the firewall level, but for me it's just one computer,
isolated to just gaming. Security isn't the most important thing in this
environment. We can just change the Network Adapter settings in the OS.

You can do this even without reinstalling, but if you want to have a fresh
installation of Windows 10 with no further updates being forced upon you
by Microsoft, I recommend re-installing Windows 10 and make sure that you
unplug your ethernet cable (and don't connect to wifi) before you start the
installer. You must use **Windows 10 Pro** (or a higher edition) since this
allows you to make a local offline account. Then follow the steps below:

1. Start -> Settings
1. Network & Internet -> Advanced network settings -> Change adapter options
1. Right click your ethernet adapter interface -> Properties. (If you are on
   wifi, then select your wireless interface). Basically anything that will be
   connecting to your LAN and that you don't want internet access to work for.
1. Uncheck **Internet Protocol Version 4 (TCP/IPv6)** (or configure it if you
   need it). I personally disabled IPv6 completely because I just need IPv4 for
   this purpose, and I also don't want the machine to accidentally connect to
   the internet, if I ever enable IPv6 on my modem (and/or if the ISP also has
   working IPv6).
1. Right click **"Internet Protocol Version 4 (TCP/IPv4)"** -> Properties
1. Check "Use the following IP address" (this should automatically also set
   **Use the following DNS server addresses**).
1. Set the **IP address** to an IP on your local network that doesn't conflict
   with your DHCP (maybe a static ip outside of the DHCP range). The
   **Subnet mask** should automatically be set to **255.255.255.0**. Leave the
   **Default gateway** and **Preferred DNS Server** empty.
1. Press OK and Close

That's basically it! Enjoy your life, be free, be happy. Let's play. Go dark!

I've been using this approach using the
**`Win10_22H2_English_x64v1.iso (2023 Update)`** with hash
**`bbb1b234ea7f5397a1906ee59187087c78374f35`** and it works great. Another thing
to keep in mind is that since you are never allowing your OS to communicate to
the outside world, Windows won't be able to reach its activation servers, which
means that the activation timer won't start. You essentially have a free and
legal copy of Windows. Not only that, but you also don't need to deal with
forced updates, forced telemetry, and any other spying that's going on. With
this set up, you get a beautiful, quiet, stable, and privacy respecting version
of Windows 10, simply by disconnecting it from the internet completely.

#### Optional VM (Not Recommended)

Now at this point, we have two options:

1. **(Recommended)**: Use another computer as your main computer (or for
   downloading games for your **Wintendo**).
2. **(Poses a security risk)**: Setup a Virtual Machine in
   [VirtualBox](https://www.virtualbox.org/) for downloading games and any
   other internet related tasks. Due to the potential security risk, if you do
   go with this approach, I recommend restricting your usage of the VM to just
   downloading games from GOG. You may be fine using this strategy for normal
   computing though if you know what you are doing.

If you switch your virtual machine's network configuration from **NAT** to
**Bridged Adapter**, you can share your host's network adapter with the guest
directly. The Windows host will still have settings that prevent it from
accessing the internet, and the guest will have its own completely different
settings that allows it to access the internet. This means that we can download
all of our games from GOG in the guest, and transfer it with no issues to our
host via the LAN network at full speeds. I had issues with transferring files
between the Host and Guest via VirtualBox's **Shared Folders**, for any games
that required a large amount of disk space. But transferring over LAN was fine
(i.e transferring the files from the guest to the NAS and then back to the
host). Due to the security risk of attacks escaping from the VM, I don't
recommend this approach. Use a separate machine instead for your regular
computing and keep the gaming machine as isolated as possible.

## Template & Labeling System

The Cactus Template & Labeling System allows you to be able to easily
start using a few pretty cool and very interesting workflows, while
allowing you to re-use your existing platforms, thus minimizing the
amount of disk space used.

For example, let's say we want to play **`Solo Self Found`** as defined
as **`Only using items that the character has found with their own hands`**,
this pretty much means untwinked play. However, let's say you
are also ok with using mules as a form of an extended stash for your
main character. Thus, any items your main character finds, can be placed
in storage, and will only be used by that main character specifically.
If you were to do this manually, for each particular main character you
made, it would quickly get out of hand since all the main characters and
each individual main character's set of mules, would all be in the same
folder. This is where the Templating & Labeling System kicks in. Now, we
could simply make a new entry in Cactus pointing to an existing
platform, and give it a particular label (Say the name of that specific
main character) and play the game. A dedicated save folder with the given
label will be created under the Saves directory for this platform.

For example, I want to make a character called **`Isaac`**. Isaac will
have their own set of mule characters as well and we'll call them
**`Mule_A`**, **`Mule_B`**, and **`Mule_C`** for simplicity. This
character will also be on **`1.09b`**. Thus, we can make a new entry for
our **`1.09b`** platform with the label **`Isaac`**. Once we start the
game, we will have the following structure in our Diablo II root
directory (let's assume I already made the characters in-game):

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s
```

As you can see, this entry is fully isolated using its platform and
label combination. Now, let's say you and your friends want to have some
type of tournament on **`1.09b`**. No problem! You can quickly add
another entry for the **`1.09b`** platform with another label, such as
**`Tournament 2022`** and start it up. The same exact **`1.09b`**
platform files that we used before will be re-used, and we will have a
new save directory. Let's create a new character called **`Bethany`**
and give Bethany a few mules as well. We'll call the mules the same as
before, and since they are isolated, we can reuse the same muling naming
scheme with no conflicts. So now our structure looks like this:

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

This is just one of the new workflows that our Templating & Labeling
System enables. This workflow requires a modified **`D2gfx.dll`** to
allow multiple instances of the game, allowing you to mule between
your main character and your mules via LAN. Singling provides this
feature for the versions it supports. For all other versions, you'll
need to find a copy of it online.

Another workflow which I really like is using this labeling system to
separate my **`Classic`** and **`Expansion`** characters. By using two
separate labels to the same platform, we can have two separate save
paths for them. If we did this, we would have the following:

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Classic/

/Saves/1.09b/Expansion/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

You can pretty much label your platforms whatever you want as long as
the name can be used for the folder on your hard drive. If you are using
some illegal symbols like **`/`**, then Cactus will properly detect that
and give you the appropriate message so that you can fix it. You can
also omit the label if you want and that works perfectly fine with the
above scenarios. Let's say you wanted to have a **`1.09b`** platform and
have everything in there without caring about labels (essentially a flat
layout, although you can also have a flat layout with a label, it just
depends on how you want to organize stuff), go ahead and create an entry
with the platform name **`1.09b`** and leave the label blank. Launching
the game will just point the save path to the **`/Saves/1.09b/`** folder
and your files will be placed in there. Assuming we then created a
character called **`Leslie`**, we would then have the following
structure:

```
/Platforms/1.09b/

/Saves/1.09b/
/Saves/1.09b/Leslie.d2s

/Saves/1.09b/Classic/

/Saves/1.09b/Expansion/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

It's just another folder after all ;). The nice thing about this is that
since all of these are sharing the same platform, switching between
these entries is extremely fast since no files need to change on your
hard drive, but rather we simply just update the registry save path, and
you are back in the action. Have fun!

## Backup System

By clicking the **`Backup`** button, Cactus will automatically create a backup
of the following files in the **`Backups`** directory, inside your
**`Diablo II Root Directory`**:

- **`/Platforms/`**
- **`/Saves/`**
- **`/Entries.json`**
- **`/LastRequiredFiles.json`**
- **`/Settings.json`**

The **`Backups`** directory is considered a **`Protected Directory`** by Cactus,
and will not be deleted.

Lastly, you can change the backup location to any location you have write access
to, by modifying the **`Backups Directory`** setting in the **`Settings`**.

## Using Cactus like a Service

Cactus has some basic tracking of processes that it launches in order to
ensure that there are no accidental launches of other versions or
combinations of the game that would cause your Save Path location to be
changed mid-game. Thus it is essential for Cactus to remain running
while you are playing. If you are always going to be running Diablo II
via Cactus, you may want to go into the Cactus Settings and toggle the
**`Minimize to System Tray`** option so that it doesn't take up space in
your taskbar. I personally like having it show in the taskbar but that's
just preference ;D.

## Moving Cactus To A New Computer

If you want to move all of your Platforms, Characters, and Diablo II folder
to another machine, you will need to:

1. Copy your entire Diablo II folder to your new computer.
1. Open **`Cactus`**.
1. Click **`Settings`** and change your **`Diablo II Root Directory`** to match the location on your new computer.
1. Click **`Reset`**.
1. Now **`Launch`** whatever Platform you want.

Clicking **`Reset`** will cause Cactus to reconfigure itself by removing
some files from your **`Diablo II Root Directory`** and wiping the
**`Last Ran`** box on the entry that has it. Once you launch the game,
the registry will point to the appropriate save location, and your platform
files will be copied back to your Diablo II root folder. In some rare cases
(only on first install), you may need to do a little bit of manual organization
in your Diablo II root folder to get things aligned properly. Once aligned, it's
all tracked and automatic.

## Unlocking All Cinematics

If you moved Cactus to a new computer, or you did a fresh install, you can unlock
all of the cinematics by doing the following:

1. Launch Diablo II, and then close it.
1. Open the Registry Editor (**`regedit.exe`**).
1. Go to **`Computer\HKEY_CURRENT_USER\SOFTWARE\Blizzard Entertainment\Diablo II`**.
1. Set the **`Aux Battle.net`** key to **`216.148.246.35`**.
1. Congrats! All of your cinematics are now unlocked.

## Updating Files In The Platforms folder

If you update any files in your Platforms folder, then click the
**`Reset`** button, and run it again. This will cause Cactus to
re-install the files with the new ones.

## OMAHGOD! My Characters Are Gone! Cactus Deleted Them!!!

Cactus comes with [built in safety features](https://github.com/fearedbliss/Cactus-Core/blob/master/Cactus/FileGenerator.cs)
specifically designed to protect critical directories and files, which
includes the save directories. Thus it is impossible for Cactus to have
deleted them. Cactus also only operates within the Diablo II root
directory so it also wouldn't be possible for Cactus to delete saves
that are in **`1.14d+`**'s new save directory that is in your personal
folder.

Since Cactus is **`A Modern Version Switcher, Character Isolator, and Mod Manager`**,
it will update the registry location of where the game should look for the
saves. For example, if you are playing a **`Platform`** called
**`1.05b`** with a **`Label`** called **`Chinchilla`**, the files for
this platform would logically be located under **`Platforms/1.05b/`**,
and the saves would be located under **`Saves/1.05b/Chinchilla/`**. Both
directories are located inside your Diablo II folder. Thus, when the
game starts, your characters are properly isolated and protected. If
this is the first time you launched a game with Cactus, and you
previously just had a regular Diablo II installation, then it would seem
as if all your characters got deleted, or magically dissapeared.
However, they are simply located in the original location that your
computer saved them to. If you were playing **`1.14d+`**, they most
likely are located at:

**`%USERPROFILE%/Saved Games/Diablo II`**

If you were playing **`1.13d`** or below, they are inside the Diablo II
folder itself under a folder called **`save`**.

Lastly, always remember to keep backups when running Third Party Tools
or Modifications.

## Cactus switches versions but I don't see the Diablo II window and there are no errors either.

If switching versions with Cactus doesn't actually launch the game but you also
don't notice any errors, this could be an indication that either your Video Settings
are not correct, or that you may need to run Cactus in Admin Mode. I've noticed that
if I have Diablo II installed on the **`C:\`** drive (i.e **`C:\Games\Diablo II`**),
I would need to run Cactus at least once in Admin Mode for it to work properly, but
if I installed Diablo II on another drive (i.e **`D:\Games\Diablo II`**), it would
work fine without Admin privileges. I'm pretty sure this is due to the **`C:\`**
drive generally being a protected drive.

Another thing to note is that I observed that I only needed to run Cactus once in Admin
Mode for this to "stick" and continue working even if I opened Cactus in the future without
Admin rights, although I haven't tested if this persists across reboots, but it possibly may.
I've also noticed that even when there was a problem, some versions would work,
and some wouldn't. Specifically versions **`1.00 - 1.06b`** worked, but **`1.07 - 1.13d`**
didn't.

Lastly, make sure that there are no zombie Diablo II processes running in the background (Task Manager),
that can cause the version switcher to either not switch away or something else. I know that
the new telemetry executables added to **`1.14d`** (i.e **`SystemSurvey.exe`** and **`BlizzardError.exe`**)
are not needed for the game to actually function, and can lock the process for a bit after you close
the game. The Cactus platforms do not contain these files since I've deleted them, however, if you
are installing from a fresh copy of Diablo II from Blizzard, it will have them.

## File Read Error on Diablo II Start Up

![Error](https://i.imgur.com/DQMcHlM.png)

If you are receiving the above error, it may be possible that some of
your MPQs are still hidden from Cactus' previous behavior before version
**`2.2.0`**. For newer versions of Cactus, Cactus will automatically
rename the following MPQs back to normal whenever you either
**`Launch`** a platform, or if you already have an entry that was
**`Last Ran`**, when you press the **`Reset`** button as well. If for
whatever reason that still doesn't work, you can go to your Diablo II
root directory and make sure that the following **`4`** Expansion MPQs
are properly named: **`d2exp.mpq`**, **`d2xvideo.mpq`**,
**`d2xmusic.mpq`**, and **`d2xtalk.mpq`**. If you see any of them with
the **`.bak`** extension, simply remove that extension and everything
should be good. If you are receiving this error but those files are in
place, then it is something else not related to Cactus.

## Game Screenshots

![1.00](https://i.imgur.com/uugMn48.jpg)
![1.05b](https://i.imgur.com/901u4V7.jpg)
![1.07](https://i.imgur.com/zHD9s5L.jpg)
![1.08](https://i.imgur.com/sUiFKqN.jpg)
![1.09b](https://i.imgur.com/JZ9bIOy.jpg)
![1.10](https://i.imgur.com/Vw4yaDM.jpg)
![1.13d](https://i.imgur.com/XiQheXy.jpg)
![1.14d](https://i.imgur.com/pojq3Jw.jpg)
