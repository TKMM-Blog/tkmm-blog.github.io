# TKMM v2.0.0-rc1: Full Changelog

Download from the [official website](https://tkmm.org/downloads/) or use the in-app auto updater.

### Important note to mod authors!
**New icons were added to the game in 1.4.0**, so if a mod contains edits to any of the `__Combined.bntx` files inside the archives from `romfs/UI/LayoutArchive`, those edits will need to be redone using the BNTX files from the latest version. Doing so will ensure your mod's compatibility across all versions from 1.1.0 through 1.4.2.

## Changes
- Support added for TotK versions 1.4.0, 1.4.1 and 1.4.2
- The `Install` button has been renamed to `Add Mod`
- The `Merge` button has been renamed to `Apply` 
- Network and download errors are truncated to avoid log spam
- Internet related errors now occur silently when connectivity is unavailable
- The setup wizard was improved for clearer step by step guidance
- TotK Optimizer "Enable" button is now replaced with an ON/OFF toggle
- Sub-files in SARC archives are now merged with other modded files that have the same canonical path
- RecipeArray now uses direct index merging (*)
- English is now used as the default language if the selected target language is not found in the mod files
- Simplified Chinese and Traditional Chinese translations have been added thanks to carbonatedtea
- Added support for Brazilian Portuguese / USpt (only works with TotK 1.4.0 and higher)
- In manual mode on the setup window, you can now simply input the name of the emulator - making sure it runs in the background will help with detecting all folder paths automatically
- Added support for auto-setup with emulators using the .AppImage format on Linux (the file must match the emulator's name, like `Citron.AppImage` for example)

(*) **Requires changelog rebuild!**

## Fixes
- Resource table values now calculated correctly
- App status updates correctly after merge failures
- Fixed an issue with NAND paths incorrectly detected as invalid
- Fixed split XCI files being misread as NSP
- Fixed TotK Optimizer sliders resetting to 100 when reloading the page
- Fixed errors related to broken json config files (corrupted files cannot be recovered, but they will be reset)
- Fixed issues with moving mods to the top or bottom of the list

## RomfsLite
Support was added for large mods on Switch firmware 20.0.0+ thanks to the RomfsLite feature from the TotK Optimizer (Ultracam) developped by MaxLastBreath.

This feature bypasses the atmosphere romfs building process which runs out of memory with large mods since firmware 20.0.0.

This is accomplished this by injecting code that directly tells the game to load RomFS files from a specific folder.

On top of this, it also allows for hot-swapping mod files while the game is running, which can be extremely useful for mod developers!

If you use TKMM-NX, simply enabling the optimizer is enough, this feature will be enabled by default.

If you use TKMM on PC, you need to enable the option in `Settings` > `Merging` and ensure the optimizer is enabled.

To use this feature on emulators, it is required that you change the merge output to this folder in the emulated SD card: `atmosphere\contents\0100f2c0115b6000`

# TKMM-NX

## Changes
- Logs folder is changed to `tkmm/Logs` on the SD card
- Initial setup now shows more information about what dumps are missing, if any
- Fixed a TKMM-NX crash occuring when clicking certain UI elements (missing library dependency)
- TKMM-NX is now capable of handling OS image self-updates. When updating, it will reboot the Switch completely rather than just close and reopen TKMM

## New menu: Reboot2Config
A new menu has been added which replaces the power options popup when pressing the Home button.

The R2C menu allows you to directly reboot to your desired boot entry, without needing to go back to Hekate.

![Reboot2Config Menu Demo](/img/rc1/reboot2config.gif)

# Bug Reporting

Please report bugs in [#bug-reports](https://tkmm.org/discord) on Discord, or post a [new issue](https://github.com/TKMM-Team/Tkmm/issues/new) on GitHub.

**Full Changelog**: [v2.0.0-beta3...v2.0.0-rc1](https://github.com/TKMM-Team/Tkmm/compare/v2.0.0-beta3...v2.0.0-rc1)