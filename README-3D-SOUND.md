# 3D Sound (DSOAL w/ OpenAL Soft)

## Included 3D Sound Versions 

**`OpenAL Soft (dsoal-aldrv.dll)`**
- **`Commit: 622ee190efff`**
- **`Commit Date: 2023-04-30-0353`**
- **`Build Date : 2023-04-30-1629`**

**`DSOAL (dsound.dll)`**
- **`Commit: 52224b17832f`**
- **`Commit Date: 2023-04-05-1035`**
- **`Build Date : 2023-04-30-1629 `**

## Requirements

- **Visual C++ 2015 - 2022 Redistributable (x86)**

## Description [(Video)](https://xyinn.org/diablo/videos/04.%203D%20Sound%20Comparison%20-%20DSOAL%20with%20OpenAL%20Soft%20(Included%20in%20Cactus).mp4)

These files will allow you to enable the following in-game settings: 
**`3D Sound`**, **`Environmental Effects`**, and **`3D Bias`**. This fix 
is equivalent to restoring lost game functionality caused by modern 
hardware no longer natively supporting these features (Such as Diablo 
II's Glide support requiring the use of a glide wrapper to enable the 
**`3DFX (Voodoo)`** card's effects like **`Perspective`** mode). In this 
instance, the lost settings were originally provided by **`Creative 
Sound`** cards like **`Sound Blaster`**. 

Have fun listening and playing with these amazing, and practically lost 
features. This works for all versions of Diablo II. No Diablo II files 
are required to be modified for this to work, it's an additive only 
change just like using the **`ddraw.dll`** for **`cnc-ddraw`**, and can 
be used on Vanilla Diablo II. 

The Cactus default installation already includes these two files and you 
simply need to enable the options you want in game. 

## Screenshot

![Sound Settings](https://i.imgur.com/2oTPc47.jpeg)

## Wine (Tested on Linux)

Follow the [Wine (Tested on Linux)](README-RENDERERS.md#wine-tested-on-linux)
section in the README-RENDERERS file for instructions on how to do this,
but add **`dsound`** to the list rather than **`ddraw`**. 

## Notes

### VCRUNTIME140.dll error when starting

If you get this error when starting the game, this means you haven't installed the
**Visual C++ 2015 - 2022 Redistributable (x86)** as written in the Cactus installation
documentation. Please install it and try again.

### Crash on startup when using **`-ns`** and **`dsound.dll`**

![Error](https://i.imgur.com/ygCLcrr.png)

There's a bug with Diablo II where if you start the game with **`-ns`** 
and you are using the **`dsound.dll`**, the game will crash with an 
**`ACCESS_VIOLATION (c0000005)`** error. Simply remove the **`-ns`** 
when starting with the 3D sound system and everything should work. 
Alternatively, you can rename the **`dsound.dll`** to something else and 
then you'll be able to use **`-ns`** but you will lose **`3D Sound`**. 

This issue doesn't affect users that are using Singling since Singling 
actually skips the introduction cinematics completely, which 
coincidentally also skips the sound issue altogether. 

This bug also doesn't seem to be a **`DSOAL`** issue since I was only 
able to get debug logs from DSOAL when **`-ns`** wasn't used, which 
indicates that Diablo II itself had an issue starting up the sound 
system in the first place. 
