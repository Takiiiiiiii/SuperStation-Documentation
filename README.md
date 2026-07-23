# SuperStation-Documentation 
## (VERY WIP, Pardon our Dust)

<img src="/images/ssonedock.jpg" width="400">

## * [Getting Started](#getting-started)
* [Contents of Each Package](#contents-of-each-package)
* [Recommended first steps once you receive your console](#recommended-first-steps-once-you-receive-your-console)
* [IMPORTANT STOCK SD CARD INFORMATION AND FLASHING PROCESS](#important-stock-sd-card-information-and-flashing-process)
* [WHAT TO DO IF THE FIRMWARE FLASH IS NOT WORKING](#what-to-do-if-the-firmware-flash-is-not-working)
* [The SuperStationᵒⁿᵉ is designed to be relatively plug and play](#the-superstationᵒⁿᵉ-is-designed-to-be-relatively-plug-and-play)
* [Pointers on how to use the SuperStationᵒⁿᵉ Dock](#pointers-on-how-to-use-the-superstation%E1%B5%92%E2%81%BF%E1%B5%89-dock)
* [Can I use the PS1 Controller ports on my SS One? What is SNAC?](#can-i-use-the-ps1-controller-ports-on-my-ss-one-what-is-snac)
   * [Why don't the PS1 Controller Ports on the SS work? ](#why-dont-the-ps1-controller-ports-on-the-ss-work)
   * [I enabled these options and my controller still doesn't work](#i-enabled-these-options-and-my-controller-still-doesnt-work)
   * [What is the notable exception you mentioned?](#what-is-the-notable-exception-you-mentioned)
* [NO COPYWRITTEN MATERIAL is included on the default SD Card Installation](#no-copywritten-material-is-included-on-the-default-sd-card-installation)

## * [Console Mode Instructions and Functionality](#console-mode-instructions-and-functionality)
  
## * [Advanced Configuration Topics](#advanced-configuration-topics)

* [Update_All Guide & Important Config Notes](#update_all-guide--important-config-notes)
  * [YES, Update_All is safe to use on the Super Station One!](#yes-update_all-is-safe-to-use-on-the-super-station-one)
  * [What if Update_All is not replacing an existing BIOS?](#what-if-update_all-is-not-replacing-an-existing-bios)
* [Patching your PSX Bios for Game ID](#patching-your-psx-bios-for-game-id)
* [Can I use an external drive (USB hard drive or NVMe M.2 in a dock) for ROM storage?](#can-i-use-an-external-drive-usb-hard-drive-or-nvme-m2-in-a-dock-for-rom-storage)
* [MiSTer Main Update with VRR Lookahead HDMI - CEC errors displaying after loading a Core](#mister-main-update-with-vrr-lookahead-hdmi---cec-errors-displaying-after-loading-a-core)
* [Why do Saturn games boot to the Saturn dashboard and display "Game Disc Is Unsuitable For This System"? Why does my Playstation show errors of "Unsafe Options" when booting a game?](#why-do-saturn-games-boot-to-the-saturn-dashboard-and-display-game-disc-is-unsuitable-for-this-system-why-does-my-playstation-show-errors-of-unsafe-options-when-booting-a-game)
* [PSX Core Ghosting on Analog Televisions](#PSX-Core-Ghosting-on-Analog-Televisions)
* [Preventing Unwanted (Re)Downloads](#preventing-unwanted-redownloads)
* [MiSTer SD Card Migration to SS One](#mister-sd-card-migration-to-ss-one)
* [Why do my controller inputs feel laggy?](#why-do-my-controller-inputs-feel-laggy)
* [SS1 Color (Black and White) Display Issue over S-Video or Composite](#ss1-color-black-and-white-display-issue-over-s-video-or-composite)
* [CIFS Mounting for network storage and related automatic scripts](#cifs-mounting-for-network-storage-and-related-automatic-scripts)
* [SS Dock Disc Tray Mod (Thanks to user Omn1Slash for the photos)](#ss-dock-disc-tray-mod-thanks-to-user-omn1slash-for-the-photos)
* [SS One Video Dip Switch Descriptions](#ss-one-video-dip-switch-descriptions)
* [PAL Considerations over Analog CRT Sets](#pal-considerations-over-analog-crt-sets)

## Getting Started

If you have just received a SuperStationᵒⁿᵉ, and this is your first MiSTer based device, then welcome to the MiSTer Ecosystem! 
The SuperStation One is, first and foremost, a MiSTer-based device that builds upon years of development, refinement, and standards established by the MiSTer ecosystem and its contributors. As a result, understanding the platform may require familiarity with MiSTer concepts, documentation, and workflows.

For a comprehensive overview of the project, including its functionality, history, and community standards, refer to the [MiSTer Development Wiki](https://github.com/MiSTer-devel/Wiki_MiSTer/wiki). Additional operational guidance is available through the [MiSTer FPGA Documentation website](https://mister-devel.github.io/MkDocs_MiSTer/), which serves as a practical reference for configuring and using MiSTer-based devices.

Additionally, if you are looking for an active community of SuperStationᵒⁿᵉ and MiSTer Pi users, you may also join the [Official Discord Channel](https://discord.com/invite/2EYTb8N) or read related topics on the [Official Retro Remake Reddit](https://www.reddit.com/r/RetroRemake/).

Review the [SuperStation One - New User Guide Video on Youtube](https://www.youtube.com/watch?v=_mMQNsauOxg) for a great summary on what to do when you receive your console. 

[![IMAGE ALT TEXT](https://i3.ytimg.com/vi/_mMQNsauOxg/maxresdefault.jpg)](https://www.youtube.com/watch?v=_mMQNsauOxg) 

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
- A Business Card sized User Placard with a QR Code and basic information.
- Founder's Edition Units also come with a a Superstation sticker, and a Retro Remake sticker.

**If you ordered the Dock by itself, you should have gotten:**
- The Super Station Dock (with NVME cover installed), and screws needed to secure to the console.
- A IR Remote Controller wrapped in plastic with paper usage guide.
- NO Batteries are included!

## Recommended first steps once you receive your console

Before digging into set-up and configuration, make sure your package is complete and has all expected items. If you are missing anything, you can do the following:
- Directly respond to your Order E-mail to contact Customer Service with the missing item in the email.
- [Send a new email](mailto:sales@retroremake.co) with your order number in the subject line and a description of the issue
- Post in the Discord Channel under either the `#superstationᵒⁿᵉ`  or `#superstationᵒⁿᵉ-help`  channels, and tag a mod for additional help.

## IMPORTANT STOCK SD CARD INFORMATION AND FLASHING PROCESS

Some users are experiencing a sudden no boot/black screen issue after adding games to their SD card! **The SD cards shipped with most units are incorrectly partitioned.**  A standard Mister install is supposed to have 2 partitions. The partitions on the SD card were written in a way that they overlap. This can cause a user to unknowingly overwrite critical system data, which eventually leads to boot failure.

You have 2 options: 
1) [Flash the NEW stock SS One image installer that taki put on his github and use the lastest **SuperStation_1.X.img.zip**
](https://github.com/Retro-Remake/SuperStation-SD-Card-Installer/releases/tag/1.1) This will flash a brand new card to the stock retail image, and it should auto expand to the full capacity of your card if you are using a card bigger or smaller than 64GB. Flash this image with balenaEtcher or Rufus. **Follow the instructions on the page!!**

2) [Flash a brand new Mister fusion install](https://github.com/theypsilon/ms-fusion), and then [copy/paste over the superstation default contents](https://drive.google.com/file/d/1DWhEkOmqlfy7-f3_PKBM-b2eUEwDlzj6/view?usp=sharing). Copy your own game/save/savestate files from the SD card if you already started using your SS One before doing this flashing procedure. 

YES, you can re-use the 64gb card that came with your SS one. You need to make sure you COMPLETELY format it to ``ExFAT`` formatted simple volume. Remember to back up your personal stuff to your PC, before you format, to copy back to a fresh SD card install! If you have additional questions or need help flashing the new image, feel free to ask in the [Official Discord Channel!](https://discord.com/invite/2EYTb8N)

## WHAT TO DO IF THE FIRMWARE FLASH IS NOT WORKING

If you experience issues flashing the latest firmware, such as a blank screen after inserting the SD card into the SS One while using HDMI output (and NOT analog video output), try the following troubleshooting steps:

1. **Verify your power supply.**
   The most common cause of booting and flashing issues is an inadequate power supply. Connect the device directly to a wall outlet instead of a power strip, especially if the strip is shared with other high-power draw devices. Use a power supply that meets the minimum requirements of **5V/3A** or **9V/2 or 3A**. **Do not use a Nintendo Switch 1 power supply**, as it is incompatible. A Nintendo Switch 2 power supply or a Steam Deck power supply is known to work reliably, as well as any number of Power Delivery (PD) Phone Brick Power supplies. 

2. **Prepare the SD card correctly.**
   Completely erase and reformat the SD card, removing **all existing partitions**. The card should contain a single partition formatted as **exFAT** (preferred), although **FAT32** is also supported. After formatting, flash the firmware by following the instructions on the flashing page.

3. **Additional SD card tips.**
   As noted in the flashing instructions, the device may occasionally require the firmware image to be written more than once before it is detected. Also verify that your SD card reader is functioning properly and isn't dated or obsolete. Ensure the SD card is fully inserted into the micro SD card slot of the SS One. Incomplete insertion or poor contact with the SD card pins can prevent the device from reading the card.

4. **Connect the HDMI cable directly to a display.**
   Connect the device directly to a monitor or television without using HDMI switches, capture cards, adapters, or other intermediary devices. Confirm that both ends of the HDMI cable are securely connected.  These devices can affect the EDID that the HDMI port sends to the target monitor/ TV, and it can cause black outs as a result. **Make sure to use the HDMI Port ON THE SUPERSTATION UNIT and NOT on the Dock.** The Dock HDMI shaped port is actually an expansion slot for future use, and doesn't send video out. 

5. **Try a different HDMI cable or display.**
   If the included HDMI cable does not work, test with another known-good HDMI cable. If possible, try a different monitor or television. Computer monitors are generally recommended because they support a wider range of display resolutions and are more likely to display video during initial setup or troubleshooting.
   
### If all else fails, please ask in the discord for additional help. PLEASE try these fixes first before asking!!

## The SuperStationᵒⁿᵉ is designed to be relatively plug and play
Before powering on the console for the first time, connect it to a TV or supported monitor using the included HDMI cable. 
Use a modern USB-C Power Delivery (PD) charger and a high-quality USB-C cable (like the one included in your package). The recommended power profile for the SuperStation is 9V/3A, although 5V or 12V will also work, provided the charger supports USB Power Delivery (PD).
This allows you to complete the initial setup and verify that everything is functioning correctly.

The SuperStation by default, runs on the MiSTer Operating System. 
If you prefer, [you can use Retro Remake's custom "Console Mode."](https://github.com/Retro-Remake/Downloader_MiSTer/releases/tag/latest)  This custom application, developed by Retro Remake, can be installed on your SD card and run on the SS One. It provides a streamlined game-launching interface and includes additional features not available in the standard MiSTer installation.

## Pointers on how to use the SuperStationᵒⁿᵉ Dock

The SuperStationᵒⁿᵉ Dock currently has a configuration issue affecting NVMe drive support. This is due to software changes that have not yet been merged into the MiSTer Main OS branch. This issue will be resolved once the required updates are integrated and distributed. Until then, it is recommended that you follow the instructions below to prevent compatibility issues that may occur with future Console Mode updates.

1. If you're starting with a brand new SuperStationᵒⁿᵉ and Dock, [flash firmware version 1.1.](https://github.com/Retro-Remake/SuperStation-SD-Card-Installer/releases/tag/1.1) . It will address all issues until an update is pushed to ``update.sh``.

2. If your SuperStationᵒⁿᵉ is already running firmware version 1.0c and is functioning correctly while running Console Mode, then no additional action is required.

3. If you have SuperStationᵒⁿᵉ and Dock running firmware version 1.0c, and the Dock does **not** have an NVMe drive installed, [replace the ``linux.img`` (375 MB) file on your included SD card](https://github.com/Retro-Remake/SuperStation-SD-Card-Installer/releases/download/1.1/linux.img) with the linked version available on GitHub to prevent reboot and compatibility issues.

## Can I use the PS1 Controller ports on my SS One? What is SNAC?

The SuperStationᵒⁿᵉ features built-in PlayStation-style SNAC adapter modules with controller ports and memory card slots for two players. If you plug in an original PlayStation controller and find that it doesn't work in the menus (or even in games) there are several possible reasons. To understand why, it's important to understand what SNAC is and its limitations.

**SNAC** (Serial Native Accessory Converter) is a specialized interface for MiSTer FPGA that allows the use of original console controllers and peripherals with near-zero latency. Unlike USB controllers, SNAC connects directly to the FPGA's user port, bypassing USB input latency and providing an experience that closely matches original hardware. Because of how SNAC works, it only functions within the MiSTer core designed for the original hardware being emulated. As a result, the built-in PlayStation SNAC ports are only typically usable within the PlayStation MiSTer core, with [one notable exception explained below.](#what-is-the-notable-exception-you-mentioned)

### Why don't the PS1 Controller Ports on the SS work? 

To enable SNAC on the SuperStationᵒⁿᵉ, launch the PlayStation core and open the **Settings** menu by pressing the **Eject/Menu** button on the console. Scroll down to **Pad1**, **Pad2**, and **SNAC Memcard**, then change them to the following:

* **Pad1:** `SNAC-port1`
* **Pad2:** `SNAC-port2`
* **SNAC Memcard:** `Real`

<img src="/images/snac4.jpg" width="400">

This routes controller input to the built-in SNAC ports and enables saving directly to real PlayStation memory cards. You can also use official and third-party PlayStation peripherals natively, including accessories such as the Beatmania controller, Pop'n Music controller, NeGcon, racing wheels, and other compatible devices, just as you would on an original PlayStation.

If you want to use a USB or Bluetooth controller (or any controller that is not connected directly to the built-in PlayStation ports) you must assign **Pad1** or **Pad2** to the appropriate emulated controller type instead of a SNAC port. This allows the PlayStation core to emulate the selected controller using your USB or Bluetooth device. You must also configure the controller mappings using the **Bind Keys** option in the PlayStation core's right-side menu.

<img src="/images/snac2.png" width="400">  <img src="/images/snac3.png" width="400">

### I enabled these options and my controller still doesn't work

If your SuperStationᵒⁿᵉ is paired with the optional dock, the dock includes a built-in MiSTer user port and a physical **SNAC Bypass** switch. When enabled, this switch disables the console's built-in PlayStation SNAC adapters and routes the SNAC signal to the dock's USB-style user port instead. This allows you to use external SNAC adapters with other MiSTer cores.

**IMPORTANT:** 
SuperStationᵒⁿᵉ units ship with **SNAC Bypass enabled by default**. If you're trying to use the built-in PlayStation SNAC ports and they still do not work after configuring the PlayStation core correctly, verify that the physical **SNAC Bypass** switch is set to **Disabled**.

### What is the notable exception you mentioned?

Retro Remake has developed a brand-new Console Mode that allows users to navigate the custom interface using a PlayStation controller by default, with no additional setup required. Console Mode was designed to let users navigate the menu system and access console mode-specific options using only a PS1 controller. The caveat is that, for now, after loading most cores (with the exception of the PlayStation core), you will still need to connect the appropriate controller or input device for the selected core.

For basic menu navigation outside of Console Mode, you may also need to use an external keyboard, another controller, or the IR remote included with the dock.
The software will continue to be updated over time with additional features, expanded user options, and ongoing improvements to Console Mode.

## NO COPYWRITTEN MATERIAL is included on the default SD Card Installation

This means that any BIOS files on the card are "open" versions that can be used to run games with. However, you may find that some Game Cores may still not run games that you add without additional BIOS files that the cores are dependent upon. See advanced configuration below for potential solutions.

-----

# Console Mode Instructions and Functionality

[**GO TO THE CONSOLE MODE WIKI FOR MORE INFORMATION**](https://github.com/Takiiiiiiii/SuperStation-Documentation/wiki/Console-Mode)

https://github.com/Takiiiiiiii/SuperStation-Documentation/wiki/Console-Mode

-----

# Advanced Configuration Topics

### Update_All Guide & Important Config Notes

#### YES, Update_All is safe to use on the Super Station One!

While this script is a powerful tool for updating your device and installing additional features, it can make extensive changes to your MiSTer system! You should definitely review the documentation before using it. While it is generally safe and does not typically damage your system, it may install components and content that you do not need or want. In the case of the SS One, it is most recommended for downloading missing BIOS files required by specific cores.

For a simple walkthrough, [follow this 5 minute video](https://youtu.be/QWj00PfZAy8)
Otherwise, use [Takis BIOS checker to see if you are missing any files](https://takiiiiiiii.github.io/MiSTer_FPGA_BIOS_Checker/) if you desire to manually source your own BIOS files.

<sub>Click the Thumbnail below to watch the Youtube Video Tutorial</sub>

[![IMAGE ALT TEXT](https://i3.ytimg.com/vi/QWj00PfZAy8/hqdefault.jpg)](https://youtu.be/QWj00PfZAy8) 

#### What if Update_All is NOT replacing an existing BIOS?

`Update_All` does not overwrite files that already exist on the SD card without user intervention. Although `Update_All` is the recommended easiest method for obtaining working BIOS files, it will not by default replace the copyright-free "open" BIOS files included with the SuperStation One SD card, such as the Open PSX BIOS.

To help address this issue:

1. Delete the BIOS file you no longer want from the appropriate directory (i.e. 'SD Card/games/psx')
2. If you have **NOT** previously run `update_all.sh`, [download the preconfigured `downloader.ini`](INI_Files/downloader.ini) and place it in the root of your SD card.
3. Run `Update_All` script, and press UP before it runs to set configuration. Follow the [previously posted video tutorial for more information.](https://www.youtube.com/watch?v=QWj00PfZAy8)
4. If you **have** previously run `update_all.sh`, you may choose instead to add the following to the end of your existing `downloader.ini`, delete the existing BIOS files, then run `update_all.sh` again:

```ini
[MiSTer]
file_checking = 'exhaustive'
```

Setting `file_checking` to `'exhaustive'` in the INI instructs `Update_All` to perform a complete file verification and replace files when necessary, such as BIOS files when enabled in the options.

### Patching your PSX Bios for Game ID

If you want to use a physical memory card with GameID support on the PS1 (such as MemCardPro or SD2PSX), you must patch the default PSX BIOS. First, remove the included open-source `boot.rom` from the `games/psx` folder and run **Update All**. Once the update is complete, [install and run this script to patch the default PSX BIOS](https://gist.github.com/IncognitoMan/fd1f9fbd5794af83370a5c6b02b7d6ee)

### Can I use an external drive (USB hard drive or NVMe M.2 in a dock) for ROM storage?

The `downloader.ini` file, which is typically created after running `update_all.sh`, can be configured to store most game-related content on external storage instead of the system SD card. Supported storage devices include:

* USB drives
* Network-mounted CIFS/SMB shares
* NVMe (not SATA) M.2 drives in a compatible USB enclosure or dock

Linux and all system files **must remain on the SD card**. The `update_all.sh` script automatically preserves this behavior.

To enable external storage:

1. If you **have not** previously run `update_all.sh`, [download the preconfigured `downloader.ini`](INI_Files/downloader.ini) and place it in the root of your SD card.
2. Run `Update_All`. Before the script starts, press **Up** to open the configuration menu. For additional guidance, see the [video tutorial](https://www.youtube.com/watch?v=QWj00PfZAy8).
3. If you **have** previously run `update_all.sh`, you can instead append the following to the end of your existing `downloader.ini`, copy the entire `games` directory from the SD card to the external drive, and then run `update_all.sh` again:

```ini
[MiSTer]
storage_priority = 'prefer_external'
```

If the external storage mounts successfully, running `update_all.sh` on your SS One will automatically prioritize the external drive, network-mounted share, or docked NVMe drive for all future game-related downloads.

### MiSTer Main Update with VRR Lookahead HDMI - CEC errors displaying after loading a Core

Recent updates to MiSTer Main have deprecated several configuration values found in the default SS1 MISTER.ini files. After running Update_All, you may see warnings or errors related to, "Lookahead, VRR, HDMI-CEC," etc. To resolve these messages, replace the existing `.ini` files on your SD card with [the updated INI files located on this Github.](/INI_Files) 

* [Default MiSTer Main - Catch all INI for default HDMI Configutations](INI_Files/MiSTer.ini)
* [MiSTer RGHV - Can be used with RGB signals that have a discrete Horizontal and Vertical Sync Terminal](INI_Files/MiSTer_RGHV.ini)
* [MiSTer RGsB - Can be used with RGB signals that Sync on Green](INI_Files/MiSTer_RGsB.ini)
* [MiSTer SVID - Can be used with S-Video and Composite](INI_Files/MiSTer_SVID.ini)
* [MiSTer YPbP - Can be used with YPbPr Component Cables, aka Most NTSC Consumer sets](INI_Files/MiSTer_YPbP.ini)

### Why do Saturn games boot to the Saturn dashboard and display "Game Disc Is Unsuitable For This System"? Why does my Playstation show errors of "Unsafe Options" when booting a game?

It is likely that the in-house testing settings were changed during the SD cards creation. For example, testers may temporarily change core settings (such as Region or the PSX core's Unsafe option) for validation of the SS One Hardare, and may have forgotten to return them to their defaults before the SD card image was finalized.

**It's recommended that if you run into any issues that you reset the core to its default settings. It will help eliminate leftover configuration changes that may interfere with "normal" operation and is often the quickest way to solve it.**

1. Open the Core's On-Screen Display.
2. Select the option to return the core settings to their defaults
3. Save Settings on the Right Page Menu.
4. Reset the core and try launching the game again.

### PSX Core Ghosting on Analog Televisions

If you see ghosted lines in the PSX core, especially when using SNAC ports over an Analog Video connection, replace the [`yc.txt`](INI_Files/yc.txt) file with [the version located on this Github.](/INI_Files) A fixed PSX core is currently in development, but this workaround should resolve the issue in the meantime.

PLEASE NOTE: `yc.txt` also can address and fix potential image quality issues on other Console Cores over Composite and S-Video. A user was able to fix Analog Line issues on the MegaDrive Core by replacing their existing `yc.txt` with the one included in this file repository. 

### Preventing Unwanted (Re)Downloads

You can prevent Update_All from redownloading files that may overwrite your preferred configuration by adding filters to your downloader.ini on your SD card. For example, if you don't want to redownload the example ini and a handful of personal computr based cores you don't want, you could add the argument to your downloader.ini file:

```ini
[MiSTer]
filter = !mister_example-ini !zxspectrum !spectrum !zxnext !zx81 !vectrex
```

This same "!" method can be used to exclude other cores, configuration files, or other content from future Download/Update_All runs. Refer to [this link about how to control the downloader with filters](https://github.com/MiSTer-devel/Downloader_MiSTer/blob/main/docs%2Fdownload-filters.md) and specifics on how to control what does and doesn't get downloaded. 

### MiSTer SD Card Migration to SS One

If you want to transfer over an existing MiSTer installation from another pre-configured device to your new SS One, then you can [use the MIGRATE_sd.sh utility found at this link.](https://github.com/Natrox/MiSTer_Utils_Natrox)

### Why do my controller inputs feel laggy? 

Input latency and display lag can be difficult to troubleshoot because they vary significantly depending on your setup, TV or monitor, and controller. The SS One Dock functions as a hub for connecting additional controllers and other accessories, so it's technically possible it could introduce a small amount of latency on the main system. However, you SHOULD ALWAYS FIRST CHECK the connected display, audio, and controllers before assuming the dock is the cause.

 **The most common cause of perceived input lag is your display.** If you're using a TV, enable Game Mode, Low Latency Mode, PC Mode, or any similar setting to reduce display processing time. CRT displays generally provide the lowest latency, especially when using native analog connections instead of converting a digital signal to analog.

**Audio can also introduce perceived lag.** External speakers (particularly those connected through HDMI eARC instead of an analog audio jack) may add noticeable audio delay. Try using your TV's or Monitors built-in speakers to rule this out.

**Controller latency can also vary dramatically between USB, 2.4 GHz wireless, and Bluetooth connections.** [Check the rpubs input latency website by clicking here](https://rpubs.com/misteraddons/inputlatency) to see how your controller performs and whether its latency is acceptable for your needs.  Additionally, [after running ``update_all``](#update_all-guide--important-config-notes), check your Scripts folder and run ``fast_USB_polling_on`` to force a 1000 Hz polling rate for all supported game pads and joysticks over USB ports. This gives your controller the best chance of minimizing input latency.

SNAC is another option for supported native controllers (such as the original Sony PlayStation controller). Review the section entitled [Can I use the PS1 Controller ports on my SS One? What is SNAC?](#can-i-use-the-ps1-controller-ports-on-my-ss-one-what-is-snac) for more details. 

### SS1 Color (Black and White) Display Issue over S-Video or Composite

By default, `vga_mode=subcarrier` in the Mister.ini, and DIP Switch 3 DOWN is the default SS1 config. It produces a higher quality signal for S-Video and Composite. However, some cores have not yet been compiled with _subcarrier support_ yet, which can result in a black-and-white image when using the default SS1 config. 

To support these cores using a more universal but lower quality method, do the following

1. Flip DIP SWITCH 3 UP on the side of the SS1.
2. Open the main menu, and move Left to select a Mister Inis.
3. Select the `SVID` profile.
4. Set DIP SWITCH 2 DOWN if using a NTSC TV or UP if using a PAL TV.

With time, more stable core releases with subcarrier support will hopefully be rolled out, but this is a way to fix it for now.

### CIFS Mounting for network storage and related automatic scripts

If you intend to use CIFS mounting with your MiSTer based device, note that CIFS shares may fail to mount during boot. [This is a long-standing, well-documented MiSTer issue that you can read about here](https://github.com/MiSTer-devel/Scripts_MiSTer/issues/88)

To fix it, a corrected version of the scripts [can be found here](https://github.com/MiSTer-devel/Scripts_MiSTer).

### SS Dock Disc Tray Mod (Thanks to user Omn1Slash for the photos)

If you experience issues with the disc tray not opening smoothly or becoming stuck during operation, try slightly loosening the screw in photo 3 to allow the tray to slide more freely. Additionally, carefully trimming the plastic in the areas indicated in photos 1 and 2 may help reduce the risk of exposed plastic burrs catching on other drive components.

<img src="/images/dock1.jpg" width="250"> <img src="/images/dock2.jpg" width="250"> <img src="/images/dock3.jpg" width="250">

This issue was caused by a manufacturing defect that has since been corrected in all subsequent dock shipments and is not expected to be an issue moving forward.

### SS One Video Dip Switch Descriptions

This applies to all units produced after December 2025:

1. YC/Composite Region
Up = PAL, Down = NTSC
2. FPGA LUMA Trap
Up = PAL, Down = NTSC
3. YC / Composite Mode
Up = FPGA, Down = Sony

4. Sync on Green
Up = Off, Down = Add

### PAL Considerations over Analog CRT Sets

Potential Useful PAL setup:
1. `menu_pal=1` set in MiSTer.ini,
2. DIP Switch 1 up,
3. Cores set to PAL

Setting cores to Auto or NTSC means black & white games as its running in NTSC mode, so that's an expected outcome for a PAL display
