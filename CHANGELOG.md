# Changelog

All notable changes to NopeSpeaker are listed here, newest first. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions are [semantic](https://semver.org/).
New entries go in [changelog.d/](changelog.d/README.md), one file per pull request - the release folds them in here under the new version and date.

## [Unreleased]

## [0.1.0] - 2026-11-03

### Added

- added: the device list - every paired Bluetooth device, connected ones first, with whether Windows may play audio on it
- added: a switch per audio device that disables or enables its audio nodes (one UAC prompt per change), so Windows stops moving the sound to it when it connects
- added: a declined or failed change says why, with the errors of the elevated script
- added: releases - weekly GitHub Releases with x64 and ARM64 zips, installable with Scoop (`scoop bucket add nopespeaker https://github.com/WizX20/NopeSpeaker`) and winget (`winget install WizX20.NopeSpeaker`)

### Changed

- changed: docs - the README opens with the NopeSpeaker logo
- changed: the app is now called NopeSpeaker (was xBlueTooth) - the exe, the zip and the repository too

### Fixed

- fix: switching a device's audio did nothing - the switch now asks for administrator rights and changes the device
- fix: a switch flipped right after a change was ignored - the switches stay locked until the list shows the new state
- fix: the "Bluetooth settings" link did nothing - it opens the Bluetooth page in Settings
