# SuperStation-Documentation
## Getting Started
![Super Station One Console and Dock](https://retroremake.co/cdn/shop/files/SuperDock.jpg)
If you have just received a SuperStationᵒⁿᵉ, and this is your first MiSTer based device, then welcome to the MiSTer Ecosystem! 
There are many things to learn about how MiSTer works as a platform, and the resources online are numerous. If you need an exhaustive reference to what the project entails, please [review the subjects covered here](https://github.com/MiSTer-devel/Wiki_MiSTer/wiki). You will find a lot of basic information about functionality of the project and expectations when using MiSTer based devices.

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

## NO Copyright Material is included on the SD Card Installation

This means that any BIOS files on the card are "open" versions that can be used to run games with. However, you may find that some Game Cores may still not run games that you add without additional BIOS files that the cores are dependent upon. See advanced configuration below for potential solutions. 

# Advanced Configuration Topics

## Update_All Guide & Important Config Notes

### **__YES, Update_All is safe to use on the Super Station One.__** 

It is recommended for downloading missing BIOS files required by specific cores.
For a simple walkthrough, [follow this 5 minute vid](https://youtu.be/QWj00PfZAy8)
Otherwise, use [Takis BIOS checker to see if you are missing any files.](https://takiiiiiiii.github.io/MiSTer_FPGA_BIOS_Checker/)

### **__Update_All is not replacing an existing BIOS__**

If `Update_All` is not replacing a BIOS file, first delete the BIOS you no longer want from the appropriate directory. Then, add the following to the top of `downloader.ini` (located in the root of the SD card) and run `update_all.sh`:

```ini
[MiSTer]
file_checking = 'exhaustive'
```

This forces `Update_All` to perform a complete file verification and replace files when necessary.

### **__Patching your PSX Bios for Game ID__**

If you want to use a physical memory card with GameID support on the PS1 (such as MemCardPro or SD2PSX), you must patch the default PSX BIOS. First, remove the included open-source `boot.rom` from the `games/psx` folder and run **Update All**. Once the update is complete, [install and run this script to patch the default PSX BIOS](https://gist.github.com/IncognitoMan/fd1f9fbd5794af83370a5c6b02b7d6ee)

### **__Can I use an external drive (USB hard drive or M.2 in a dock) for ROM storage?__**

Yes. To prioritize an external USB drive or an M.2 drive in a dock, add the following to the top of `downloader.ini` (located in the root of the SD card), then run `update_all.sh`:

```ini
[MiSTer]
storage_priority = 'prefer_external'
```

Next, copy the entire `games` directory from the SD card to the external USB drive or M.2 drive. If the drive mounts correctly, SS1 will automatically prioritize the external or docked drive.

### **__MiSTer Main Update with VRR Lookahead HDMI - CEC errors displaying after loading a Core__**

Recent updates to MiSTer Main have deprecated several configuration values found in the default SS1 MISTER.ini files. After running Update_All, you may see warnings or errors related to, "Lookahead, VRR, HDMI-CEC," etc. To resolve these messages, replace the existing `.ini` files on your SD card with the updated INI files located on this Github. 

### **PSX Core Ghosting**

If you see ghosted lines in the PSX core, especially when using SNAC ports over an Analog Video connection, replace the `yc.txt` file with the version located on this Github. A fixed PSX core is currently in development, but this workaround should resolve the issue in the meantime.

### **Preventing Unwanted (Re)Downloads**

You can prevent Update_All from redownloading files that may overwrite your preferred configuration by adding filters to your downloader.ini on your SD card. For example, if you don't want to redownload the example ini and a handful of personal computr based cores you don't want, you could add the argument to your downloader.ini file:

``[MiSTer]
filter = !misterexampleini !zxspectrum !spectrum !zxnext !zx81 !vectrex ``

This same "!" method can be used to exclude other cores, configuration files, or other content from future Download/Update_All runs. Read [the following link](https://github.com/theypsilon/Update_All_MiSTer) for more information about configuring Update_All.

### **__MiSTer SD Card Migration to SS One__**

If you want to transfer over an existing MiSTer installation from another pre-configured device to your new SS One, then you can [use the MIGRATE_sd.sh utility found at this link.](https://github.com/Natrox/MiSTer_Utils_Natrox)

### __**SS1 Color (Black and White) Display Issue over S-Video or Composite**__

By default, `vga_mode=subcarrier` in the Mister.ini, and DIP Switch 3 DOWN is the default SS1 config. It produces a higher quality signal for S-Video and Composite. However, some cores have not yet been compiled with _subcarrier support_ yet, which can result in a black-and-white image when using the default SS1 config. 

### __To support these cores using a more universal but lower quality method, do the following:__

1. Flip DIP SWITCH 3 UP on the side of the SS1.
2. Open the main menu, and move Left to select a Mister Inis.
3. Select the **S-Video** profile. 
4. Set DIP SWITCH 2 DOWN if using a NTSC TV or UP if using a PAL TV.

With time, more stable core releases with subcarrier support will hopefully be rolled out, but this is a way to fix it for now.

### __**CIFS Mounting, for network storage and related automatic scripts.**__

If you intend to use CIFS mounting with your MiSTer based device, note that CIFS shares may fail to mount during boot. [This is a long-standing, well-documented MiSTer issue that you can read about here](https://github.com/MiSTer-devel/Scripts_MiSTer/issues/88)

To fix it, a corrected version of the scripts [can be found here](https://github.com/MiSTer-devel/Scripts_MiSTer/issues/88#issuecomment-4402795197)

### __**SS Dock Disc Tray Mod (Thanks to user Omn1Slash for the photos).**__

If you experience issues with the disc tray not opening smoothly or becoming stuck during operation, try slightly loosening the screw in photo 3 to allow the tray to slide more freely. Additionally, carefully trimming the plastic in the areas indicated in photos 1 and 2 may help reduce the risk of exposed plastic burrs catching on other drive components. 

![Dock Photo 1](/dock1.jpg)
![Dock Photo 2](/dock2.jpg)
![Dock Photo 3](/dock3.jpg)

This issue was caused by a manufacturing defect that has since been corrected in all subsequent dock shipments and is not expected to be an issue moving forward.

### **SS One Video Dip Switch Descriptions**

This applies to all units produced after December 2025:

1. YC/Composite Region
Up = PAL, Down = NTSC
2. FPGA LUMA Trap
Up = PAL, Down = NTSC
3. YC / Composite Mode
Up = FPGA, Down = Sony
4. Sync on Green Up = Off, Down = Add

### **PAL Considerations over Analog CRT Sets**

Potential Useful PAL setup:
1. `menu_pal=1` set in MiSTer.ini,
2. DIP Switch 1 up,
3. Cores set to PAL

Setting cores to Auto or NTSC means black & white games as its running in NTSC mode, so that's an expected outcome for a PAL display

