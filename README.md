Head over to [the releases page](https://github.com/x-station/xstation-releases/releases) to download the latest files.   

If you'd like to report an issue, please file it in [xstation-issues](https://github.com/x-station/xstation-issues).   

## XStation Firmware + Loader [1.4.5] - 2021-12-11

- adjusted Libcrypt patching for PAL titles, fixes Ape Escape and Parasite Eve 2
- seek to sd access has a small holdoff period now, works a bit smoother
- consistent use of 64bit variables when working with the main timer

xLoader:
- swapped fastboot method to the "warm boot" style, fixing the games broken in the last release
- it's winter! :)

## Usage
Extract update.bin and loader.bin to your SD card 00xstation folder.
Start your console into the loader (press and hold reset for a second if the loader doesn't start automatically).
Enter the options menu and select Update Firmware, then press Start.
The firmware will be installed and the console will reboot.
You may confirm the new version in the loader's options menu.

## XStation Firmware + Loader [1.4.4] - 2021-10-01

- revert SD card seek shortcuts as some games require all data (example: Dr. Slump)
- tweaked small seek behaviour to still avoid some accesses
- games like this and load faster (Music Maker, Excalibur, likely all games with lots of small seeks)
- avoid data alignment issues when the SD card takes too long to seek
- drive resets: fix Parappa (NTSC-J) stage end FMVs
- accessing the CD lead-out area works properly now (Wing Commander 4, some homebrew disks)
- fixed multiple concurrent commands order and delays (Destruction Derby 2)
- fix FF8 PAL-E (Libcrypt)
- TOC parsing: support any number of PREGAP tags (unofficial TR2 translation)
- tweaked how queues are remembered across cold boots

xLoader:
- folder based browsing supports disk queues now 
- Memory Card manager with Memcard Pro support: copy, delete or undelete files
- two known fastboot issues fixed (Crisis Beat and Elemental Gearbolt), leaving one title to be investigated yet (GT2 Revision 1)
- when editing a disk queue: press Start to fastboot the queue
- VRAM cleared on startup and fastboot, avoids visual glitches

## Usage
Extract update.bin and loader.bin to your SD card 00xstation folder.
Start your console into the loader (press and hold reset for a second if the loader doesn't start automatically).
Enter the options menu and select Update Firmware, then press Start.
The firmware will be installed and the console will reboot.
You may confirm the new version in the loader's options menu.

## XStation Firmware + Loader [1.3.0] - 2021-05-20

- implement folder based browsing
  - can be enabled in the loader options
  - doesn't require game list scanning
  - multi disc queues not yet implemented (use regular mode for now)
- rewritten core to remove old dependencies for better maintainability
- avoid SD card access while seeking
- overall faster seek times
- use an SPI peripheral for the DSP sub bus (faster, more efficient)
- TOC parsing: malformed TRACK and INDEX tags fixed
- fix gamelist scanning errors / duplicate files for macOS Finder users

## Usage
Extract update.bin and loader.bin to your SD card 00xstation folder.
Start your console into the loader (press and hold reset for a second if the loader doesn't start automatically).
Enter the options menu and select Update Firmware, then press Start.
The firmware will be installed and the console will reboot.
You may confirm the new version in the loader's options menu.

## XStation Firmware + Loader [1.2.0] - 2021-03-22

### Core changes:
- fix a race condition that could lock-up the xStation when starting some games (Thanks SubElement!)
- preparation for folder based browsing and scan speedup
- free about 20k of memory, use it as additional sector cache

### Loader changes:
- much faster file scanning
- when holding L2 + R2, all other inputs are ignored (for PS1Digital)
- pressing Start fast boots the last played game
- further improve error condition checks

## Usage
Extract update.bin and loader.bin to your SD card 00xstation folder.
Start your console into the loader (press and hold reset for a second if the loader doesn't start automatically).
Enter the options menu and select Update Firmware, then press Start.
The firmware will be installed and the console will reboot.
You may confirm the new version in the loader's options menu.

## XStation ESP32 Firmware + Loader [1.1.0] - 2021-02-24

### Bug Fixes & Improvements
- SD card access reduced when seeking, helping support more cards
- data stream timings are now aligned to the I2S master clock only, no more reliance on the ESP32 crystal
- Tales of Destiny 2 can now disc swap correctly
- fixed Spyro 3 PAL (libcrypt)
- improved Gex: Enter the Gecko FMV performance
- improved seek accuracy and timing, helping titles that tend to hang on real hardware stay stable on xStation

### Features
- Support for MemCard Pro and PS1Digital Game ID sending
- automatically corrects bad EDC/ECC when needed (homebrew, fan translations, patched games)
- PAL / NTSC selector for the loader
- snappier button response in the loader

## Usage
Extract update.bin and loader.bin to your SD card 00xstation folder.
Start your console into the loader (press and hold reset for a second if the loader doesn't start automatically).
Enter the options menu and select Update Firmware, then press Start.
The firmware will be installed and the console will reboot.
You may confirm the new version in the loader's options menu.

## XStation ESP32 Firmware + Loader [1.0.5] - 2020-11-26

### Bug Fixes & Improvements
- Improved accuracy of the SUBQ output signal 
- SD card drive strength tweaks for SD card extenders
- Additional SENS subtimings + new sled move algorithm, improves general accuracy and particularly load times in Gran Turismo 2
- Image parser now ignores "leading dot" system directories such as .Trash
- Small loader tweaks, fixing Saga Frontier fastboot

## XStation ESP32 Firmware [1.0.4] - 2020-10-30

### Bug Fixes & Improvements
- Reset line better debouncing for PU-8 slow rise times
- Libcrypt protected games now work, no user attention required
- Fixed remembering path names with special characters

## XStation Loader [1.0.4] - 2020-10-30
### New Features
- NeGcon, Mouse and GunCon support

### Bug Fixtures & Improvements
- Brushed up artwork
- Further 3rd party accessories tweaks

## XStation ESP32 Firmware [1.0.2] - 2020-10-19

### Bug Fixes & Improvements
- Faster DSP command parsing for improved stability
- Fixed "Fantastic Pinball Kyuutenkai" black screening
- Interrupt priority balancing


## XStation Loader [1.0.2] - 2020-10-19
### New Features
- Added a Dark Theme
- You can now choose your theme from the Options menu
- All options saved to SD card

### Bug Fixtures & Improvements
- Restructured the Options Menu
- Improved third-party controller support
- Fixed an issue with "Castlemania SotN" through fastboot
- Many more fastboot improvements


### SD Card Setup
If this is the first time setting up your xStation, please follow [this short guide](https://github.com/x-station/xstation-releases/blob/main/xStation_User_Guide.pdf).   
