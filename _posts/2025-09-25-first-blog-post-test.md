# TKMM v2.0.0-beta4 is Available

Download from the [official website](https://tkmm.org/downloads/) or use the in-app auto updating.

## Changes
- Support added for TotK versions 1.4.0, 1.4.1 and 1.4.2
- TKMM-NX logs folder is changed to `tkmm/Logs` on the SD card
- Initial TKMM-NX setup now shows more information about what dumps are missing
- PC version setup wizard was improved for clearer step by step guidance
- TotK Optimizer "Enable" button is replaced with a toggle
- Network and download errors are truncated to avoid log spam
- Sub-files in SARC archives are merged with other modded files that have the same canonical path
- It is now possible to install TKCL mods embedded inside an archive
- RecipeArray now uses direct index merging (*)
- English is now used as the default language if the selected target language is not found in the mod files
- Simplified Chinese and Traditional Chinese translations have been added thanks to <@961536121899192371> 

-# * **Requires changelog rebuild!**

## Fixes
- Resource table values now calculated correctly
- App status updates correctly after merge failures
- Fixed an issue with NAND paths incorrectly detected as invalid
- Fixed split XCI files being misread as NSP
- Fixed TotK Optimizer sliders resetting to 100 when reloading the page
- Fixed a TKMM-NX crash occuring when clicking certain UI elements (missing library dependency)
- Auto-setup works with .AppImage emulators (must match emulator name, like `Citron.AppImage`)

## Bug Reporting

Please report bugs in [#bug-reports](https://tkmm.org/discord) and tag posts with v2.0.0-beta

||\@ Release Announcements ||

**Full Changelog**: [v2.0.0-beta3...v2.0.0-beta4](https://github.com/TKMM-Team/Tkmm/compare/v2.0.0-beta3...v2.0.0-beta4)