(Head over to [the releases page](https://github.com/x-station/xstation-releases/releases) to download the latest files.)   

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
If this is the first time setting up your SD card, follow this short guide:   
- create a folder named "00xstation" on your card (this is the xstation system directory)   
- firmware updates (update.bin) and the loader application (loader.bin) go into this folder   
- copy your games to the SD card   
- try to avoid having more than about 150 items per folder, otherwise scanning the card for games becomes slow   
- it helps to organize games in folders for their starting letter (0-a, b, c, .. y, z, etc)    
