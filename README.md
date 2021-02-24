Head over to [the releases page](https://github.com/x-station/xstation-releases/releases) to download the latest files.   

If you'd like to report an issue, please file it in [xstation-issues](https://github.com/x-station/xstation-issues).   

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
