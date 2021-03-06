# Change Log

The following enhancements and changes have been made to Atari Dev Studio:

## 0.3.5

* Updated to latest dasm release v2.20.13 (Windows, Linux, macOS) 
* Added options in the settings for choosing to use the **Default** (built-in) compiler or using a **Custom** one you have provided (batari Basic, 7800basic, dasm). This change will allow you to keep your custom compiler path without having to remove it to revert back to the default built-in one. 
* Removed setting **atari-dev-studio.compiler.options.defaultCompiler** as it is no longer required (didn't appear to work anyway). Compilation of a file is determined by the language chosen in the editor.

## 0.3.4

* Updated to latest batari Basic release v1.4 (Windows, Linux, macOS)
* Updated to latest 7800basic release v0.7 (Windows, Linux, macOS)
* Re-enabled basic language completion for 7800basic 

## 0.3.3

* #14 [Done] Fixed clock tables for Horizontal Motion documentation (thanks andyjp)
* #15 [Done] Added region folding for 7800basic and batari Basic (thanks MikeBrownEmplas) Usage: ;#region " XXX ", ;#endregion. Code based on the [#region folding for VS Code](https://marketplace.visualstudio.com/items?itemName=maptz.regionfolder) extension by maptz
* #15 [Done] Extended bank1-bank8 -> bank1-bank24 for 7800basic and batari Basic (thanks MikeBrownEmplas)
* Updated bB score_graphics.asm for DPC+ fix (TwentySixHundred/Karl G)

## 0.3.2

* Updated to latest batari Basic release v1.2 (Windows, Linux, macOS)

## 0.3.1

* Officially (finally!) included compiler and emulator packages for macOS (tested on Mojave).
* Added Stella 6.0.2 (macOS)
* Updated to latest dasm release v2.20.12 (Windows, Linux and macOS).
* Updated internal dev packages 

## 0.3.0

* Updated Stella to 6.0.2 (Windows, Linux)
* Removed the intellisense for 7800basic (for now) until we can include code keyword (ie. labels, function, variables)

## 0.2.9

* Added option to activate the A7800 emulator debugger
* Added simple intellisense for 7800basic (keywords, functions, consts etc)

## 0.2.8

* Fixed issue with rem keyword mis-highlighting when used within variables (batariBasic and 7800basic)
* Added missing 7800basic keywords: tallsprite
* Updated existing and added additional hover tooltips for 7800basic keywords

## 0.2.7

* Added missing 7800basic keywords: hsgamename, noflow, trackersupport
* Added additional hover tooltips for 7800basic keywords

Sprite Editor
* Updated Editor window to be resizable
* Re-arranged Toolbar order

## 0.2.6

* Updated internal dev packages (security notification)

## 0.2.5

* Added hover tooltips for 7800basic keywords (a large majority)
* Updated 7800basic to 0.6 Jul 13 2019 22:37:29

## 0.2.4

* Updated Stella to 6.0.1 (Windows, Linux)

## 0.2.3 

* Added missing 7800basic keywords: P6C3

Sprite Editor
* Added features to load, save and reset your palettes (via a new toolbar on the Palette window)
* Added a fix for the occasional re-popup of load and save dialogs when communicating with VSCode
* Fixed issue where items on the New Project window did not reflect the expected value on first start
* Fixed issue exporting to .png files 

## 0.2.2

* Added missing 7800basic keywords: function, BACKGRND, PXC1,PXC2,PXC3 for palettes 0-7 

Sprite Editor
* Added resize sprite feature allowing sprites sizes to be changed
* Added ability to export the selected sprite to .png
* Wrapped the toolbar to be 2 icons wide by default and adjusted initial layout location of all windows

## 0.2.1

Sprite Editor
* Fixed an issue selecting a palette color
* Indented spinner value on New Project wizard to match combobox
* Added information about the Sprite Editor to the README
 
## 0.2.0

* Updated 7800basic compilation routine to validate for additional errors and added cleanup of 7800hole.x.asm files after compilation
* Changes to RemoveCompilationFilesAsync routine as the CleanUpCompilationFiles flag wasn't working as expected
* Added missing 7800basic keywords: converttobcd, extrawide, joy0fire, joy1fire, joy0any, joy1any

Sprite Editor
* Added New Project wizard to configure your sprites allowing you to select the size, region (palette) and total colors
* Added additional messaging to status bar when using features
* Fixed issue where toolbar was not updated properly after loading project

## 0.1.9

* #13 [Done] - SmallRoomLabs updated hover text to markdown format [thanks SmallRoomLabs] 
* Updated 7800basic compilation routine to validate for additional errors

Sprite Editor
* Updated Project area to store loaded file and auto save or prompt
* Added menu bar back to display filename of active file
* Updated Palette selector to display user colors  across then down to allow for future expansion
* Changes to file format to allow sprite size to be stored
* Further internal changes

## 0.1.8

* #12 [Done] - SmallRoomLabs added a process to display hover tooltips to dasm language for 6502 and VCS opcodes [thanks SmallRoomLabs]
* Extended hover tooltip process to work across all languages
* Minor internal changes to Sprite Editor for future enhancements

## 0.1.7

* #6 [Done] - Added new drop-down selector in settings to choose what you want to display on the Status Bar (Full, Minimum, None) [thanks SmallRoomLabs]
* #7 [Done] - Autoclose any existing Stella windows before opening a new one (new option in settings to override) [thanks SmallRoomLabs]
* #8 [Fixed] - When a dasm compilation fails clean up files generated by compiler (.sym/.bin/.lst) [thanks SmallRoomLabs]
* #9 [Fixed] - Fixed issue autosaving files before compile (async) [thanks SmallRoomLabs]
* #11 [Done] - Updated label determination in dasm assembly syntax [thanks SmallRoomLabs]

Sprite Editor
* Added ability to export all sprites in project to .png (2 bit 7800basic)
* Added ability zoom editor with mousewheel
* Added ability to set transparent background color in editor (not exported to .png) to help when designing sprites

## 0.1.6

Sprite Editor
* Added ability to load and save sprites
* Added (auto) load and save of the workspace configuration (window layout)
* Added ability to select and hold down mouse button to change palette colors on the fly for selected color
* Fixed issue where holding down mouse button and leaving the sprite editing area left drawing mode on

## 0.1.4, 0.1.5

* Introduction of a Sprite Editor (basic functionality only). The Sprite Editor is based on Spritemate by Ingo Hinterding ([github](https://github.com/Esshahn/spritemate)) and was suggested by RandomTerrain. I've taken the original source and rebuilt and restructured it. It cannot do anything other than the basics - just wanted to see if it ran OK on other PCs. 

## 0.1.3

* Updated 7800basic language definition with all (known) keywords, commands and variables. Note: there is every chance I have either missed some or labled incorrectly.
* Update readme to include imore information about installing and a note about turning off the short-cut buttons on the Status Bar

## 0.1.2

* Added option in settings to show/hide commands on Status Bar (thanks SmallRoomLabs)
* Updated readme with information about debugging

### Issues
* #1 [Fixed] - Duplicated filename after re-configuration of code (thanks SmallRoomLabs)
* #5 [Fixed] - Added new setting to turn on/off the status bar commands (thanks SmallRoomLabs)

## 0.1.1

* Added new Help references and Learn areas for batari Basic and 7800basic to Welcome page
* Removed templates from Welcome page (for now)
* Updated readme with more information about the product
* Updated all internal references to accessing the settings to a const to better maintain future changes

### Issues
* #1 [UnderReview] - Added compiler notification to help with permission error when compiling dasm on macOS (thanks SmallRoomLabs)
* #2 [Fixed] - Removed popup message (thanks SmallRoomLabs)
* #3 [Fixed] - Updated breadcrumb to Settings to correct path and catered for cross-platform (thanks SmallRoomLabs)
* #4 [Fixed] - Updated syntax highlighter (thanks SmallRoomLabs)

## 0.1.0

* Initial release