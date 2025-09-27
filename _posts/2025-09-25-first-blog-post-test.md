# TKMM v2.0.0-rc1: Full Changelog

Download from the [official website](https://tkmm.org/downloads/) or use the in-app auto updater.

**Full GitHub history since last update**: [v2.0.0-beta3...v2.0.0-rc1](https://github.com/TKMM-Team/Tkmm/compare/v2.0.0-beta3...v2.0.0-rc1)

### Important note to mod authors
**New icons were added to the game in 1.4.0**. If one of your mods contains edits to any of the `__Combined.bntx` files inside the archives from `romfs/UI/LayoutArchive`, those edits will need to be redone using the BNTX files from the latest version. Doing so will ensure your mod's compatibility across all versions from 1.1.0 through 1.4.2.

### Important note to mod users
As was voted on Discord a few months prior, this update made many changes to the changelog formats, this means that all your mods will need to be reinstalled in the new version. For TKCL mods, you will need to wait until the authors have updated their mod with the new TKCL format.

<p align="center">
  <img src="https://blog.tkmm.org/img/rc1/discordvote.png" alt="Discord Vote" />
</p>

# Changes
- Support added for TotK versions 1.4.0, 1.4.1 and 1.4.2
- The `Install` button has been renamed to `Add Mod`
- The `Merge` button has been renamed to `Apply` 
- Network and download errors are truncated to avoid log spam
- Internet related errors now occur silently when connectivity is unavailable
- The "Enable" button on the TotK Optimizer page is now replaced with an ON/OFF toggle
- RecipeArray now uses direct index merging
- English is now used as the default language if the selected target language is not found in the mod
- Simplified Chinese and Traditional Chinese translations have been added thanks to carbonatedtea
- Added support for Brazilian Portuguese / USpt (only works with TotK 1.4.0 and higher)
- Sub-files in SARC archives will now be merged with files that have the same canonical path in other archives
- The setup wizard was improved for clearer step by step guidance
- In manual mode on the setup window, you can now simply input the name of the emulator - making sure it runs in the background will help with detecting all folder paths automatically
- Added support for auto-setup with emulators using the .AppImage format on Linux (the file must match the emulator's name, like `Citron.AppImage` for example)

# Fixes
- Resource table entries should now be properly estimated, issues that required using the external RESTBL calculator are now fixed
- Fixed the app status not updating correctly after merge failures
- Fixed an issue with NAND paths incorrectly detected as invalid
- Fixed split XCI files being misread as NSP
- Fixed TotK Optimizer sliders resetting to 100 when reloading the page
- Fixed errors due to broken json config files (corrupted files cannot be recovered but will be reset)
- Fixed issues with moving mods to the top and bottom of the list

# RomfsLite
The issues due to lack of memory when launching TotK with mods (introduced since Switch firmware 20.0.0) are now a thing of the past! Thanks to the RomfsLite feature from the [TotK Optimizer](https://www.nxoptimizer.com) (Ultracam) developped by [MaxLastBreath](https://ko-fi.com/MaxLastBreath).

This is accomplished by injecting code that tells the game to directly load RomFS files from a specific folder (basically, `romfs` renamed to `romfslite`). On top of this, it also allows for hot-swapping mod files while the game is running, which can be extremely useful for mod developers (this requires reloading a save after swapping files).

We recommend using the version that is integrated to TKMM, which you can enable by going to the TotK Optimizer page (star icon on the navigation bar).

- If you use TKMM-NX, simply enabling the optimizer is enough, this feature will be enabled by default.

- If you use TKMM on PC, you need to enable the option in `Settings` > `Merging` and ensure the optimizer is enabled.

- To use this feature on emulators, it is required that you change the merge output to this folder in the emulated SD card: `atmosphere\contents\0100f2c0115b6000`

# Default mod
A new mod is dynamically built by TKMM and added to the merge output. It adds an indicator on the title screen so that you can directly know whether mods are properly installed.

![Default Mod](/img/rc1/defaultmod.png)

*This mod is added at the lowest priority, which means that if another mod edits the same text entry, that mod will overwrite it.*

## TKMM-NX

# Changes
- The Logs folder location has been changed to `tkmm/Logs` on the SD card
- The WiFi settings page is now the first step of the setup wizard
- Initial setup now provides more information about what dumps are missing, if any
- Fixed a crash occuring when clicking certain UI elements (missing library dependency)
- TKMM-NX is now capable of handling OS image self-updates - when updating, it will reboot the Switch completely rather than just close and reopen TKMM

**A new config file was added at** `tkmm/config.ini` **which allows customization of a few things:**
- the scale of the application, in case the text or UI elements are either too big or too small
- the volume for the sound card, in case the sound played when taking a screenshot is either too loud or too quiet

# New menu: Reboot2Config
The [R2C menu](https://github.com/LordBubblesDev/R2CSharp) replaces the power options popup when pressing the Home button. It allows you to directly reboot to your desired boot entry, without needing to go back to Hekate.

![Reboot2Config Menu](/img/rc1/reboot2config.gif)

## Bug Reporting

Please report bugs in [#bug-reports](https://tkmm.org/discord) on Discord, or post a [new issue](https://github.com/TKMM-Team/Tkmm/issues/new) on GitHub.

## Contributors to this update
- [Arch Leaders](https://github.com/ArchLeaders)
- [Lord Bubbles](https://github.com/LordBubblesDev) 
- [Aster](https://github.com/AsteroidPizza39) (for gathering as many toasters as possible so we could warm the regards)
- [carbonatedtea](https://github.com/k-carbonatedtea) (Simplified Chinese and Traditional Chinese translations)