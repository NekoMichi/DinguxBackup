# DinguxBackup
DinguxBackup is a small utility that backs up save data and configs for GMenu2x and various emulators on OpenDingux devices.

**How to install**

Download the latest version of backup.opk and copy it to /media/data/apps/ on the primary SD card of the device. A new "SaveBackup" app should now appear under the applications section.

![screenshot01](/screenshots/screenshot01.png)

**Prerequisites**

SaveBackup exports save data to the secondary SD card so make sure there is one inserted before running. If there is no secondary card or if the secondary slot is faulty, the script will display an error and then prompt the user to quit.

**Where is backup data stored?**

SaveBackup will create a new folder on the secondary SD card called "backup" and export saves there. They can then be accessed on other devices.

**What data does the app backup?**

SaveBackup will only backup data from specific apps and emulators. They are:
- GMenu2x settings
- Screenshots taken by pressing Power and X
- FCEUX (NES emulator)
- Gambatte (GameBoy emulator)
- ReGBA (GameBoy Advance emulator)
- PCSX4all (PlayStation 1 emulator)
- PicoDrive (Sega Master System/Genesis/Game Gear emulator)
- PocketSNES (Super NES emulator)

**Known issues/quirks**
- The first time this app is run, it may take longer than usual as it needs to generate the initial backup folder structure and files. Subsequent runs will be much faster as it only backs up files that have changed since the last backup.
- After running the backup app for the first time, some emulators might take a little longer than usual to start up. This only happens once and should not any save progress.
