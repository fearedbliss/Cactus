# Renderers

## Included Renderer Versions

- **`cnc-ddraw - 6.3.0.0`**

## Recommendations

Due to the increasing number of issues associated with Diablo II's Glide 
implementation for versions below **`1.14`** on modern versions of 
Windows, and due to Blizzard removing **`DirectDraw`** support starting 
with **`1.14`**, Cactus no longer includes **`glidewrapper`**. 
**`cnc-ddraw`** is the recommended renderer for all versions before 
**`1.14`**, and thus I recommend everyone to downgrade to **`1.13d`** (or 
lower). Besides compatibility fixes implemented in **`1.14`**, both 
versions are identical. Cactus will only provide video support for 
versions **`1.00 - 1.13d`**.

**`cnc-ddraw`** is more compatible and performs better on Windows, and 
has more features than **`glidewrapper`**. Specifically the ability to 
dynamically resize the window resolution (not the internal resolution), 
set any custom window resolution, easily switch between window mode and 
full screen via a hotkey, and upscale the game's textures to look much 
better through the use of shaders, are just a few of the features it 
has. Since **`cnc-ddraw`** is a **`DirectDraw`** implementation, any 
Glide related errors will no longer affect you. 

If you still want to play Diablo II **`(Original, Not Resurrected)`** on 
**`1.14d+`**, please download an alternative video renderer of your choosing.

### For people that never ran a version older than 1.14 on their machine

Blizzard implemented some fundamental changes with how video 
configuration works in **`1.14+`**, and this will cause issues if you 
are going back down and your system is missing these settings. 

If you have never played a version older than **`1.14`** on your 
computer, that means you would have never had ran **`D2VidTst.exe`** and 
thus you won't have the required registry settings for the game to work 
in older versions. Please follow the instructions for the 
**`cnc-ddraw`** section to set **`DirectDraw`** as your default renderer 
which would in turn allow **`cnc-ddraw`** to be picked up by the game 
and used. Once this is done, all your versions (except **`1.14+`**) 
should automatically work with this renderer. 

If this isn't set up properly, you will experience crashes or weird 
behaviors such as an **`Access Violation`**, etc. 

## **`cnc-ddraw`**

In order to use **`cnc-ddraw`**, you will need to make sure that your 
Diablo II video renderer is set to use **`DirectDraw`**. Diablo II 
versions starting at **`1.14`** no longer support DirectDraw and thus 
you will need to use an alternative instead. 

The required files for **`cnc-ddraw`** are already included as part of the
Cactus Base Installation, specifically **`ddraw.dll`**, **`ddraw.ini`**,
and the **`Shaders`** directory. Thus, all of these files will be located in
the root of your Diablo II directory.

### Setting your video mode to DirectDraw

### Configuration

To make sure we are starting from a clean slate, we will delete the entire
**`VideoConfig`** key located in the registry and we will set the renderer
to DirectDraw directly.

1. Open up the **`Registry Editor`** by running **`regedit`**.
1. Delete the **`HKEY_CURRENT_USER\Software\Blizzard Entertainment\Diablo II\VideoConfig`**
   key if it exists.
1. Create a new key called **`VideoConfig`** under the **`Diablo II`** key. 
1. Create a new **`DWORD (32-bit) Value`** called **`Render`** under the
   **`VideoConfig`** key. This should already be set to **`0`** for you.

That's it! Try the **`Quick Testing`** instructions below to see if the dll is
being used and working.

#### Quick Testing

Try running Diablo II (Make sure you don't have any other settings
that can conflict with the renderer such as using **`-3dfx`**, **`-opengl`**,
or **`-w`** flags) and see if the game starts up. If the game starts up, see if
you can easily switch between full screen and window mode by pressing
**`[Alt] + [Enter]`**. If you can't switch between these modes, then the dll is
not being used to render the game. If it doesn't, you will need to continue
inspecting things yourself.

### Wine (Tested on Linux)

If you are running Diablo II on Linux, you will want to make sure that your
**`WINEPREFIX`** is overriding the **`ddraw`** dll so that it can pick up the
custom **`ddraw.dll`** in the Diablo II root directory.

For example, on my system I'm using a specific prefix that just contains
Diablo II, located at **`${HOME}/prefix/diablo_2`**. If you are using the
default prefix, then you don't need to include the **`WINEPREFIX`** part for any
of the following commands. If you are, adjust the prefix location to point to
the one on your machine.

1. Open up the wine configuration by typing:
 
    ```
    $ WINEPREFIX="${HOME}/prefix/diablo_2" winecfg
    ```

1. Set the **`Windows Version`** at the bottom to **`Windows XP`** so that your
   **`Mouse 3`** button works properly.
1. Click the **`Libraries`** tab at the top.
1. In the **`New override for library`** textbox, Write in **`ddraw`** (With no
   extension) and click **`Add`**.
1. You will receive a warning saying: **`Changing the load order of this
   library is not recommended. Are you sure you want to do this?`**.
   Click **`Yes`**.
1. You should see a new element in the list below that says:
   **`ddraw (native, builtin)`**. Click **`Ok`**.

Once this is done, you can run the steps in the **`Configuration`** section
above. You can also run the **`regedit`** command in Wine as well by doing:

```
$ WINEPREFIX="${HOME}/prefix/diablo_2" regedit
```

**`Note`**: Cactus is a Windows-only application. However, you can still 
use the rest of the files provided in the Cactus Repository on Wine with 
the above configuration. 

### Tweaking **`cnc-ddraw`**

You can tweak **`ddraw.ini`** to change any settings such as the window
resolution (not the internal resolution), renderer, shaders, etc.

#### Tweaking Shaders (The Game Look)

Cactus contains a carefully curated set of shaders from the upstream repository.
I'm using the **`jinc2-sharper`** shader as the default since it is an overall
good looking shader that still very closely resembles the original game.
You can play around with the included shaders and settings until you find a
combination that works for you.

To change the shader, just open the **`ddraw.ini`** file and change the
shader line to a different shader located in the **`Shaders`** directory:

```
shader=Shaders\windowed\jinc2-sharper.glsl
```

You can get more shaders from
[libretro's repository](https://github.com/libretro/glsl-shaders), however only
**`.glsl`** will work, if at all. **`cnc-ddraw`** states that they've only
implemented **`preliminary shader support`**.

### Hotkeys and Other

Since **`cnc-ddraw`** already has support to switch between full screen and
window mode for the game, you need to make sure you don't use the **`-w`** flag
since it's no longer necessary.

The following hotkeys are also available for you in game:

- **`[Alt] + [Enter]`** - Switches between Full Screen and Window Mode.
- **`[Ctrl] + [Alt]`** OR **`[Right Alt] + [Right Ctrl]`** - Unlocks the cursor.

If you happen to also play Diablo 1, you can use **`cnc-ddraw`** for it as well!
  
## **`glidewrapper`**

**`glidewrapper`** is no longer included with Cactus. Please read the 
**`Recommendations`** section at the beginning of this page for further 
info. 

## General Problems

### Scrolling Letters

- Both **`Glide`** and **`DirectDraw`** have this problem, however the problem
  is experienced differently on both implementations. For **`Glide`**, it is
  much worse and more noticable. It seems it will happen not only when you
  start Diablo II, but it will also happen when you switch games as well
  (start a game, save and exit, and make a new game). For **`DirectDraw`**,
  this seems to only happen when you start Diablo II, but not in between games.
  Singling includes the [Scrolling Letters Fix](https://xyinn.org/diablo/videos/10.%20%5bDiablo%20II%5d%20Scrolling%20Letters%20Fix%20&%20Demo%20(Included%20in%20Singling_Cactus).mp4)
  for both implementations.

### Error 22/25: A critical error has occurred while initializing X

If you get any of the following errors, your setup is probably broken and will
need to be repaired:

- **`Error 22: A critical error has occurred while initializing DirectDraw`**
- **`Error 25: A critical error has occurred while initializing Direct3D`**

Try re-installing Cactus from scratch and try again.

If you are still experiencing issues even after you verified your Diablo II
Root Directory files are good, you should follow [these](https://github.com/fearedbliss/Cactus?tab=readme-ov-file#installation-instructions)
instructions to reset your video configuration in the registry.

A full re-install and wipe of the Diablo II registry located at the location
below is most likely not required:

**`HKEY_CURRENT_USER\SOFTWARE\Blizzard Entertainment\Diablo II`**
