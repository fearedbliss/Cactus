# Cactus Porting Advice

Hello all,

This post will give you some advice when trying to port mods to Cactus. Not
every mod will be compatible due to a variety of reasons. The main goal of Cactus
is to allow the person to easily install and play a mod with just a few clicks.
Cactus itself is exclusively an offline application and will never require an
internet connection or contain internet related features. Therefore the
experience I'm aiming the user to have for installing and running a platform is
as follows:

1. Download and extract the **Platform** into the **Platforms** directory.
2. Add the **Platform** to Cactus.
3. Launch the Platform.

That's it. Every single platform in the database must provide that type of
experience for the user or it won't be accepted.

Cactus was originally designed to be ***A Version Switcher and Character Isolator***,
not a ***Mod Manager***. However, given that Cactus' architecture was properly
implemented to only focus on switching files, and not perform any sorts of dll
or file modifications, it allows for a clean separation of responsibilities
between Cactus, and the platform. This means that as long as the platform takes
care of its own dll hooking mechanisms, and anything else it needs to be a fully
independent platform, Cactus can just focus on switching platforms for the user,
and updating the appropriate registry locations for character isolation. With
this porting advice in place, and the [Cactus Ports Collection](PORTS-COLLECTION.md),
Cactus is now taking on the role as a ***Mod Manager*** in an official capacity,
within Cactus' existing architecture.

Some mods are easier than others to port. With a simple mod, you usually just
need to extract the base Cactus Platform for the version the mod is based upon,
then extract the specific mod over that, and that's basically it. However, if
the mod is depending on external launchers for its hooking mechanism, you will
need to rewire the dll loading paths and make some configuration changes. You
can check out existing mods I've ported for some of the steps and techniques
I did to get them working. Some of the mods that required more complicated
adjustments, and that you can use for your own learning are:

- **D2: Ironman**
- **Escape from the Afterlife**
- **Immersion**
- **Le Royaume des Ombres**
- **Reign of Shadow**
- **Requiem of Sorrow**
- **Underworld**

To name a few. Once you get the hang of it, you will notice that most mods, even
the complicated ones, usually follow the same exact pattern.

Once you are done porting, you can either make your mod publicly available
through your own means, or I can host it for you. Regardless of your distribution
method, if you want me to add it to the database, you can email me at
**`cactus@xyinn.org`**. I'll review your mod, check for some basic compatibility,
and do some basic security checks (viruses, etc). If there are no issues, I can
include it in the database at the appropriate level. Before emailing me, make
sure that you include a markdown mod file with your bundle. You can follow the same
style that's used by mods listed in the [Cactus Ports Collection](PORTS-COLLECTION.md).
Any extra files not related to the execution of the platform can be placed in a
folder called **Other** inside the platform. You can also provide up to **`10`**
screenshots which I will use when listing your mod. You can use the same
auto-generated names that Diablo II has (**`Screenshot1.jpg`** or
**`Screenshot001.jpg`** depending on the version), also let me know which of the
screenshots should be the one used as the splash image for people to see when
they first load up the mod. The rest will be displayed in the screenshots
section in linear order.

Since my server is not guaranteed to be online 100% of the time, I recommend
anyone interested in preserving anything on my server to do so.

Lastly, in addition to all the files and sources I'm already hosting, I'm also
[mirroring](https://xyinn.org/diablo/porting/) some tools and applications I
needed in order to port some mods with more complicated setups.

## Suggestions

1. ***Design your mod so that it all works within the Diablo II root directory.***

	If Cactus didn't exist, the installation should be as simple as dropping
	and replacing your mod files in the Diablo II root directory, and running
	**Game.exe**. Thus, all the required DLLs, Custom MPQs / Patch_D2.mpq
	should be in the platform folder you wish to distribute. The core MPQs
	should NOT be included since the user needs to provide those themselves
	through their legal purchase of the game. You should assume that the user
	has all of the core game MPQs, D2.LNG, and Cactus installed (and what comes
	with Cactus). That's it.

1. ***Do not use any custom installers. Just pack up the platform directly with 7-Zip.***

	It's easier for the user (and for yourself) to just pack up the platform
	directly with **7-Zip** using **Ultra** compression. All other Cactus
	platforms I'm hosting are using this format and you get a lot of space
	savings as well. Plus you don't have to deal with maintaining an installer
	and having to worry about "where" their D2 folder is. The user can figure
	that out given they already have Cactus installed.

1. ***Do not hijack or modify the Save Path (or other keys Cactus manages).***

	Let the game naturally handle it. Cactus takes care of setting the
	**Save Path** for each entry and allowing it to be properly isolated.
	In addition, below is the full list of registry entries that Cactus
	manages, and should not be touched by the developer or user:

	- **`Save Path`**
	- **`NewSavePath`**
	- **`InstallPath`**
	- **`PopupHireling`**

	These can also be found by looking at the [code](https://github.com/fearedbliss/Cactus-Core/blob/main/Cactus/RegistryService.cs).

1. ***Don't use any names in your Platform that are being protected by Cactus.***

	Cactus provides full protection for any files that it distributes as Shared
	Resources, any any other important files such as Core MPQs, **`D2.LNG`**,
	etc. Avoid calling anything in your mod anything listed below since Cactus
	will automatically filter these names out when doing its file processing
	operations. As usual, for safety reasons, more files may be added in the
	future if needed.

	The full list of protected files as of ***Cactus 2.6.3*** is as follows:

	- **`Backups/`**
	- **`Platforms/`**
	- **`save/`**
	- **`Saves/`**
	- **`Shaders/`**
	- **`Cactus.exe`**
	- **`Castle.Core.dll`**
	- **`Castle.Windsor.dll`**
	- **`CommonServiceLocator.dll`**
	- **`default.key`**
	- **`d2char.mpq`**
	- **`d2data.mpq`**
	- **`d2exp.mpq`**
	- **`D2.LNG`**
	- **`d2music.mpq`**
	- **`d2sfx.mpq`**
	- **`d2speech.mpq`**
	- **`d2video.mpq`**
	- **`d2xmusic.mpq`**
	- **`d2xtalk.mpq`**
	- **`d2xvideo.mpq`**
	- **`ddraw.dll`**
	- **`ddraw.ini`**
	- **`dsoal-aldrv.dll`**
	- **`dsound.dll`**
	- **`GalaSoft.MvvmLight.dll`**
	- **`GalaSoft.MvvmLight.Extras.dll`**
	- **`GalaSoft.MvvmLight.Platform.dll`**
	- **`GongSolutions.WPF.DragDrop.dll`**
	- **`MaterialDesignColors.dll`**
	- **`MaterialDesignThemes.Wpf.dll`**
	- **`Newtonsoft.Json.dll`**
	- **`System.Windows.Interactivity.dll`**

	The list of files and folders can also be found in the code, [here](https://github.com/fearedbliss/Cactus-Core/blob/main/Cactus/FileGenerator.cs).

1. ***Don't modify the VideoConfig settings. Render should always be 0.***

	Cactus has been maintaining compatibility with **cnc-ddraw (DirectDraw)**
	since it is stable and supports every version of Diablo II even across OS
	(**cnc-ddraw** in Wine seems to work well), do not modify any **`VideoConfig`**
	settings. You can follow the instructions documented in the [README-RENDERERS](../README-RENDERERS.md#setting-your-video-mode-to-directdraw)
	page. If your mod can use **`-3dfx`** or another video system without
	negatively impacting other mods, then you are safe to do so.

1. ***Run the game through Game.exe or a custom exe directly in the Diablo II root directory.***

	This means that if you want to use a custom loader you can, but don't have
	it do crazy things like nesting the launcher under a sub-folder in the
	Diablo II root directory. The launcher must be in your Diablo II root
	directory, just like **Game.exe**. When in doubt, emulate the original
	behavior of the game. You can also take a look at all of the existing
	Cactus Platforms for reference and try to run your mod the same way.

1. ***Ensure DirectDraw Compatibility. Use cnc-ddraw (DirectDraw) when possible.***

	Make sure that your mod is compatible with **cnc-ddraw (DirectDraw)**.
	Most Cactus users are probably using **cnc-ddraw** over **glidewrapper**
	for various reasons. It is less buggy and has more features while not
	affecting the game in any negative way.

1. ***Ensure DSOAL w/ OpenAL Soft Compatibility.***

	Make sure that your mod is compatible with **OpenAL** and **DSOAL**. Most
	people probably haven't tested **3D Sound** and **Environmental Effects**
	compatibility given that the functionality has been lost in the game due to
	hardware changes over the past decades. You can re-enable these features
	and test against them by dropping the **`dsoal-aldrv.dll`** and **`dsound.dll`**
	files that are included in Cactus, into your Diablo II Root Directory, then
	start the game. You should be able to enable the listed settings above in
	the **Sound Options**. Check out the [3D Sound (DSOAL w/ OpenAL Soft)](../README-3D-SOUND.md)
	for more info.

1. ***Allow the game to run normally without the CD.***

	All Cactus Platforms already contain ***GalaXyHaXz's No-CD pack***, which
	allows the game to run without the CD, essentially using the same method
	as what Blizzard did starting with Patch 1.12.

1. ***Be careful when including glide3x.dll.***

	I've experienced crashes on exiting Diablo II with ported mods that included
	this dll. I've also experienced zombie Diablo II processes hanging around
	in the background after program exit, which causes Cactus to not be able
	to switch versions (since it still detects the game running, so for safety
	purposes it won't let you switch). If your mod is a native Cactus platform,
	and you've already tested that **`glide3x.dll`** works without crashing, and
	there are no hanging issues, then you can include it. Cactus won't protect
	the **`glide3x.dll`**, so for any Cactus users that want to use it, my recommended
	approach is to place this dll inside the Platform itself so it's only used
	for that platform. This also allows you to keep your configuration in that
	platform without worrying that another mod may potentially wipe this file out.
	I strongly recommend to use cnc-ddraw over glidewrapper. cnc-ddraw is a shared
	resource for all mods with Cactus and is protected by Cactus' file protection
	mechanisms. For any mods I port, I will delete the **`glide3x.dll`** if the
	mod works without it. If it doesn't work without it, I'll keep it but leave
	it at **`Gold`** level or lower depending on the issues that it's causing.
	Any mods that cause silent hanging issues after the game exits will be
	downgraded to **`Bronze`** level. Silently hanging the game causes Cactus
	to not be able to switch versions because Cactus protects the users from
	switching between different platforms when the game is running as a safety
	feature. This would mean the user needs to intervene and force kill the
	zombie process from Task Manager. So far it seems you only need to worry
	about the **glidewrapper** implementation since its outdated, but from some
	minor testing, the newer Glide implementations don't seem to have this issue.
	You should still test for these cases though.

1. ***Platform names cannot collide with existing platforms.***

   This is more of a distribution tip, but if there is a mod already called the
   same name as your mod, you should include additional information in the Platform
   name to reduce the chance of collision with other Platforms. For all
   ***internally hosted mods***, I will ensure this is true and will rename any
   other platform folders to guarantee this.

   For example, all of my maintained mods use the following format:
   **`Mod Name (Mod Version)`**. This usually provides enough namespacing so that
   no two mods collide. An example of this is **Median XL**. The Cactus Ports
   Collection contains a few **Median XL** platforms. To avoid collision, the
   platforms are called:

   - **Median XL (1.70)**
   - **Median XL (2012 v005)**

1. ***Do not include any copyrighted material in your Platform (unless it falls under Fair Use).***

	I think it's safe to say that your mod should not include anything that
	people could get legally in trouble for. There have been mods I've seen that
	contain all of the MPQs from the CDs in their source distributables. Do not
	include them. Cactus already requires the user to provide a purchased copy
	of Diablo II from their end, your mod should not have to worry about this.
	Check the protected files list above for a list of files that Cactus protects,
	which include all of the core assets of the game. Anything not included in
	that list is either provided in the Platform, or by Cactus.

1. ***Only include the minimum amount of stuff necessary.***

	I've seen a lot of mods include a bunch of random garbage and stuff that's
	not necessary. Only include the minimum amount of stuff necessary for your
	mod to work. You can also include any documentation or anything else you
	want the users to have.

1. ***Ensure the game works with the English version of the game by default***

	The game was originally made in English, and this is the only copy of the
	game that I have, so all development and testing is done in English. However,
	you can include additional language support as well, either using the
	**`data/local/Use`** technique, or some other strategy. From what I've read,
	using **`Use`** is not enough since the person is also suppose to have the
	corresponding **`D2Lang.dll`**. Given that the **`D2Lang.dll`** is a
	Protected File, I'm not too sure what the solution for this would be. I
	believe including the dll inside the **`data`** directory won't work. Given
	the vast amount of language and file/version support matrix, support for
	non-English languages is done on a limited basis.