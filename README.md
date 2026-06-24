# SuperStation-Documentation
## Getting Started
![Super Station One Console and Dock](https://retroremake.co/cdn/shop/files/SuperDock.jpg)
If you have just received a SuperStationᵒⁿᵉ, and this is your first MiSTer based device, then welcome to the MiSTer Ecosystem! 
There are many things to learn about how MiSTer works as a platform, and the resources online are numerous. If you need an exhaustive reference to what the project entails, please review the subjects covered [here](https://github.com/MiSTer-devel/Wiki_MiSTer/wiki). You will find a lot of basic information about functionality of the project and expectations when using MiSTer based devices.

Additionally, if you are looking for an active community of SuperStationᵒⁿᵉ and MiSTer Pi users, you may also join the [Official Discord Channel](https://discord.com/invite/2EYTb8N) or read related topics on the [Official Retro Remake Reddit](https://www.reddit.com/r/RetroRemake/). 

## Contents of Each Package

**If you ordered the console by itself, you should have gotten:**
- The Super Station Console
- An HDMI cable
- A USB-C Braided Cable (Power Supply not included!)
- SD Card (preinstalled into the unit and flashed with a stock image that includes Homebrew apps)
- A Business Card sized User Placard with a QR Code and basic information
- Founder's Edition Units also come with a a Superstation sticker, and a Retro Remake sticker.
  
**If you ordered a BUNDLE, which includes the console and dock, you should have gotten:**
- The Super Station Console
- The Super Station Dock (already attached to the SS One console).
- An IR Remote for controlling navigation and the functions of the DVD Drive
- An HDMI cable
- A USB-C Braided Cable (Power Supply not included!)
- SD Card (preinstalled into the unit and flashed with a stock image that includes Homebrew apps)
- A plastic cover for the Dock port.
- A Business Card sized User Placard with a QR Code and basic information
- Founder's Edition Units also come with a a Superstation sticker, and a Retro Remake sticker.

## Recommended first steps once you recieve your console.

Before digging into set-up and configuration, make sure your package is complete and has all expected items. If you are missing anything, you can:
- Directly respond to your Order E-mail to contact Customer Service with the missing item in the email.
- [Send a new email](mailto:sales@retroremake.co) with your order number in the subject line and a description of the issue
- Post in the Discord Channel under either the #superstationᵒⁿᵉ  or #superstationᵒⁿᵉ-help  channels, and tag a mod for additional help.

## The SuperStationᵒⁿᵉ is designed to be relatively plug and play. 
The SuperStation runs on the MiSTer Operating System. If you prefer, [you can use Retro Remake's custom "Console Mode."](https://github.com/Retro-Remake/Downloader_MiSTer/releases/tag/latest)

Before powering on the console for the first time, connect it to a TV or supported monitor using the included HDMI cable. 
Use a modern USB-C Power Delivery (PD) charger and a high-quality USB-C cable (like the one included in your package). The recommended power profile for the SuperStation is 9V/3A, although 5V or 12V will also work, provided the charger supports USB Power Delivery (PD).
This allows you to complete the initial setup and verify that everything is functioning correctly.

# Advanced Configuration Topics

## Update_All Guide & Important Config Notes

**YES, Update_All is safe to use on the Super Station One.** 

It is recommended for downloading missing BIOS files required by specific cores.
For a simple walkthrough, [follow this 5 minute vid](https://youtu.be/QWj00PfZAy8)
Otherwise, use [Takis BIOS checker to see if you are missing any files.](https://takiiiiiiii.github.io/MiSTer_FPGA_BIOS_Checker/)

**Patching your PSX Bios for Game ID**

If you want to use a physical memory card with GameID support on the PS1 (such as MemCardPro or SD2PSX), you must patch the default PSX BIOS. First, remove the included open-source `boot.rom` from the `games/psx` folder and run **Update All**. Once the update is complete, [install and run this script to patch the default PSX BIOS](https://gist.github.com/IncognitoMan/fd1f9fbd5794af83370a5c6b02b7d6ee)

**MiSTer Main**

Recent updates to MiSTer Main have deprecated several configuration values found in the default SS1 MISTER.ini files. After running Update_All, you may see warnings or errors related to, "Lookahead, VRR, HDMI-CEC," etc. To resolve these messages, replace the existing `.ini` files on your SD card with the updated versions attached to this post.

**PSX Core Ghosting**

If you see ghosted lines in the PSX core, especially when using SNAC ports over an Analog Video connection, replace the `yc.txt` file with the version attached to this post. A fixed PSX core is currently in development, but this workaround should resolve the issue in the meantime.

**Preventing Unwanted (Re)Downloads**

You can prevent Update_All from redownloading files that may overwrite your preferred configuration by adding filters to your downloader.ini on your SD card. For example, if you don't want to redownload the example ini, add the argument to your downloader file:
```[MiSTer]
filter = !misterexampleini```
-# This same "!" method can be used to exclude specific cores, configuration files, or other content from future Download/Update_All runs.*
