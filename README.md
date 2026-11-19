# MagicOS CN Tool — HONOR Tools for Windows

**MagicOS CN Tool** is an independent Windows utility by **Haradreamer** for working with Chinese-region HONOR smartphones running MagicOS. It provides a graphical interface for commonly used Android Debug Bridge (ADB) tasks.

[Русская версия / Russian README](README.ru.md) · [Installation & ADB troubleshooting](docs/INSTALLATION.md) · [Changelog](CHANGELOG.md)

## Download

**[Official GitHub Releases](https://github.com/Haradreamer/Honor-Tools-CN/releases)**

This is the official public **distribution and support repository**. Download only the versioned release files attached to a published Release. **If no asset is attached, the installer has not yet been published here.** The development source and private materials are not included.

## What it does

Depending on the installed version, MagicOS CN Tool offers:

- **USB and Wi-Fi ADB connection** to supported HONOR devices.
- **Chinese pre-installed app and service management**, including disabling selected packages and restoration workflows.
- **Google Play setup tools** for supported Chinese MagicOS devices.
- **ADB command terminal** for manually running commands.
- **Device and connection checks** and guided settings.

Function availability varies by version, phone model and firmware. The tool cannot guarantee that every feature works on every HONOR phone. **Isle and AutoFace are separate apps**, distributed independently.

## Requirements

- A Windows PC.
- A compatible HONOR phone with **Developer options** and **USB debugging** enabled.
- A working USB data cable and ADB driver, or an already authorized wireless ADB connection.
- User confirmation of the phone's **Allow USB debugging** authorization prompt.

## Quick start

1. Download the latest verified Windows release from the [Releases page](https://github.com/Haradreamer/Honor-Tools-CN/releases).
2. Extract its archive, if applicable, and follow the release's instructions.
3. Enable **Developer options → USB debugging** on your HONOR phone.
4. Connect using a USB data cable and approve the RSA debugging prompt on the phone.
5. Open MagicOS CN Tool, check connection status and review actions before applying changes.

For detailed help, see the [setup guide](docs/INSTALLATION.md).

## Safety and privacy

**Read before using:** Disabling system packages or modifying settings can cause missing functionality, failed updates or unexpected behavior. Keep a list of changed packages and make a backup of important data. Prefer reversible **disable** operations over deleting system packages. Only run ADB commands you understand.

ADB commands are carried out through the connected computer/device. Do not connect devices you do not own or have permission to administer.

No general privacy claim is made about every past and future build; examine the applicable release notes and file permissions for the version you install.

## Compatibility and feedback

Originally focused on **Chinese MagicOS builds**, including development and testing on HONOR flagship devices. Behavior on global or other Chinese firmware revisions can differ.

To report a problem, open a [GitHub Issue](https://github.com/Haradreamer/Honor-Tools-CN/issues) with the HONOR model, region, MagicOS version, tool version, USB/Wi-Fi connection method and a redacted error log.

## Related projects

- [Isle — Magic Capsule enhancements](https://github.com/Haradreamer/Isle-HONOR-app)
- [AutoFace — face confirmation automation](https://github.com/Haradreamer/Honor-AutoFace)
- [Original community support thread on 4PDA](https://4pda.to/forum/index.php?showtopic=1119615&view=findpost&p=145819882)

## Support the developer

The software is developed independently by **Haradreamer**. Optional support: [Boosty](https://boosty.to/haradreamer).

**Disclaimer:** Not affiliated with HONOR, HUAWEI or Google. Android, ADB, MagicOS and related trademarks belong to their respective owners.
