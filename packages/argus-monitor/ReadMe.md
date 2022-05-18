# Chocolatey Package: Argus Monitor

[![Build Status](https://img.shields.io/travis/itigoag/chocolatey.adobe-acrobat-reader-dc?style=flat-square)](https://travis-ci.org/itigoag/chocolatey.adobe-acrobat-reader-dc) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](licence) [![Chocolatey](https://img.shields.io/chocolatey/v/adobereader?label=package%20version)](https://chocolatey.org/packages/adobereader) [![Chocolatey](https://img.shields.io/chocolatey/dt/adobereader?label=package%20downloads&style=flat-square)](https://chocolatey.org/packages/adobereader)

## Description

If you are looking for a program to control your CPU fan, GPU fans or system fans, then Argus Monitor might be best program for that purpose. With the **fan control** features of Argus Monitor you can control the fans of your PC, and set either a **fixed fan speed** or control them **based on any of the temperature sources** available on your system. It is for instance possible to control the fan speeds of your case fans based on the temperatures of your CPU, the GPU temperature, disk temperatures, RAM temperatures, mainboard temperature sensors or sensor readings provided by an AIO or external fan controller — or a combination thereof.

Argus Monitor is an alternative to the well known tool SpeedFan and at the moment the **best application for software fan control for Windows**.

## Package installation defaults

By default, **installation** of this package:

- Will _NOT_ install a desktop icon.
- Will _NOT_ install the Adobe Reader and Acrobat Manager ("ARM") service.
- Will _NOT_ uninstall language-specific installations.
- Will configure Reader to only **check for updates manually** with confirmation for install.

However, **upgrades** to Adobe Reader via this package:

- Will _NOT_ remove an existing desktop icon or add one when there isn't.
- Will _NOT_ install the AdobeARM service.
- Will _NOT_ remove the AdobeARM service (though it will disable it unless enabled by parameters).
- Will _NOT_ re-enable updates (if disabled via package parameter)

## Package Parameters

- `/DesktopIcon` - The Desktop icon will be installed to the common desktop. (Install only.)
- `/NoUpdates` - No updates via internal mechanisms (including manual checks). Only downloading from Adobe and running installers or updates (or updating this package) will advance the version of Reader. Once set, only uninstalling this package will remove this update block.
- `/OverwriteInstallation` - Uninstall a language-specific installation before installing the Multi-lingual ("MUI") release. _Be aware that this will remove all data and features of an existing installation!_
- `/EnableUpdateService` - Install the AdobeARM service. (Does not override `/NoUpdates`.)
- `/UpdateMode:#` - Sets the update mode (below). (Does not override `/NoUpdates`.)

## Installation

installation without parameters.

```ps1
choco install adobereader
```

installation with parameters.

```powershell
 choco install adobereader --params="'/RemoveDesktopIcons'"
```

## Disclaimer

These Chocolatey Packages only contain installation routines. The software itself is downloaded from the official sources of the software developer. This developer has no affilation with the software developer.

## Author

- [George Symeonides](https://github.com/gsymeoni)


## License

This project is under the MIT License. See the [LICENSE](LICENSE) file for the full license text.

## Copyright

(c) 2022, George Symeonides