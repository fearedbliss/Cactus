# Installing Cactus on Windows 7

## Synopsis

The following guide will show you how to get Cactus running on Windows 7.
We will primarily be running this from a fresh installation of
**Windows 7 RTM (x64)**, which means the **Day 1** release of Windows 7, without
any updates, or service packs. Starting from this point will provide maximum
installation coverage. For the record, I still own a legal retail copy of
**Windows 7 Ultimate RTM**, and still have the box, and discs :).

Cactus runs on **.NET Framework 4.6.2**, which is only supported on a minimum
version of **Windows 7 SP1**. So along the way, we will be updating our
**Windows 7 RTM** install to **SP1**, and installing any additional
dependencies. All of these are necessary since Microsoft made updates over the
years, and thus we need to get up to a minimum point of compatibility before it
works. The instructions below include only the minimum, and recommended updates
to get this to work. No other updates will be included.

Lastly, after you finish installing all of these updates, and getting everything
working, you may want to take a snapshot of your OS so that you don't need to do
all of this again in the future. You can also try and create your own Windows 7
ISOs by ***slipstreaming*** these updates into it. I'll let you research tools,
and techniques for doing this. But it may actually be easier for most people to
just take a snapshot at this point, rather than slipstreaming.

## Required Files

These are all the files you'll need to get this working. I'll be providing
direct links to Microsoft's Update Catalog for these files, and I'm also
[mirroring](https://xyinn.org/diablo/windows) them as well.

- [**KB2533552 (Update for Windows 7)**](https://catalog.s.download.windowsupdate.com/msdownload/update/software/crup/2011/05/windows6.1-kb2533552-x64_0ba5ac38d4e1c9588a1e53ad390d23c1e4ecd04d.msu)
- [**KB976932 (Windows 7 Service Pack 1 for x64-based Systems)**](https://catalog.s.download.windowsupdate.com/msdownload/update/software/svpk/2011/02/windows6.1-kb976932-x64_74865ef2562006e51d7f9333b4a8d45b7a749dab.exe)
- [**KB4490628 (2019-03 Servicing Stack Update for Windows 7 for x64-based Systems)**](https://catalog.s.download.windowsupdate.com/c/msdownload/update/software/secu/2019/03/windows6.1-kb4490628-x64_d3de52d6987f7c8bdc2c015dca69eac96047c76e.msu)
- [**KB4474419 (2019-09 Security Update for Windows 7 for x64-based Systems)**](https://catalog.s.download.windowsupdate.com/c/msdownload/update/software/secu/2019/09/windows6.1-kb4474419-v3-x64_b5614c6cea5cb4e198717789633dca16308ef79c.msu)
- [**Microsoft Root Certificate Authority 2011**](https://www.microsoft.com/pki/certs/MicRooCerAut2011_2011_03_22.crt)
- [**.NET Framework 4.6.2 Offline Installer**](https://go.microsoft.com/fwlink/?linkid=2099468)

### Notes

- **`KB2533552`** - The whole thing actually worked without me installing this,
  but Microsoft recommended it in the Microsoft Update Catalog as part of the
  SP1 update. We'll go ahead and install it to make sure we don't get any
  unforeseen consequences.

- **`.NET Framework 4.6.2 Offline Installer`** - We'll use the offline installer
  rather than the web version so that we are more future proof, and also so that
  you don't have to re-download the whole thing if something goes wrong during
  its install process.

## Installation

### Updating from RTM to Service Pack 1

If you are already running **Service Pack 1**, you can go to the next section.

To check if you are on SP1, you can:

- Click **Start**
- Type **`winver`**, and press **`[Enter]`**

If it says **`Version 6.1 (Build 7601: Service Pack 1)`**, then you are good
and can continue to the next section.

If it says: **`Version 6.1 (Build 7600)`**, then you are on RTM, and need to
install the following two updates:

- Install **`KB2533552 (Update for Windows 7)`**
- Install **`KB976932 (Windows 7 Service Pack 1 for x64-based Systems)`**

It will take some time to install SP1, so go make some tea, and come back.

### Update for SHA-2 Support

You'll now install the updates for SHA-2 support which will be required for the
Microsoft Root Certificate Authority 2011 to function properly, since it's using
SHA-2.

- Install **`KB4490628 (2019-03 Servicing Stack Update for Windows 7 for x64-based Systems)`**
- Install **`KB4474419 (2019-09 Security Update for Windows 7 for x64-based Systems)`**

### Install the Microsoft Root Certificate Authority 2011

- Double click the **`MicRooCerAut2011_2011_03_22.crt`** certificate
- Click **`Install Certificate...`**
- Click **`Next -> Next -> Finish`**

You should see a successful import message.

### Install .NET Framework 4.6.2

Finally, we can click the **`.NET Framework 4.6.2`** installer to install .NET
successfully. Once it's finish, you can launch Cactus. Have fun!