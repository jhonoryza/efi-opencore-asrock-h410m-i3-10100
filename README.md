# OpenCore EFI AsRock H410M Core i3-10100 igpu
hackintosh

## Guide
- After making bootable mac installer, run mount efi partition tool to your usb partition to open efi partition
- Copy from this repo EFI folder to efi partition
- Reboot and boot from your usb installer
- Using disk utility format hardrive with apfs format
- Install macos
- After successfully install, Run mount efi partition tool again to mount efi partition from your installed hardrive
- Copy EFI folder from usb installer to efi partition
- Now you can boot to macos without usb installer

## Tools
- [https://github.com/corpnewt/MountEFI](https://github.com/corpnewt/MountEFI) as mount efi partition
- [https://github.com/corpnewt/ProperTree](https://github.com/corpnewt/ProperTree) as plist editor
- [https://github.com/corpnewt/GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) as smbios generator
- [https://github.com/headkaze/Hackintool](https://github.com/headkaze/Hackintool) as hackintool
- force-display.zip as script to fix magenta display in dvi or hdmi output

## Force Display Fix Guide
- unzip force-display.zip
- Start by running the .rb script. example: ruby .rb
- It only generates a couple of files in your user’s directory and does not require any special rights to read the current monitor / tv configuration. (TV must be connected).
- Boot to into the recovery system (Cmd+R during boot).
- All your files are accessible here and you have write permissions to the “Overrides” folder. Your system disk is just not mounted to / but to /Volumes/ (e.g. “/Volumes/Macintosh HD/”)
- Open a terminal and copy the DisplayVendor-directory. Remember that every path is now prefixed by “/Volumes/Macintosh HD/”.
- E.g. I had the Ruby script in a folder “EDID-Fix” on my desktop.
-bash-3.2# cp -r /Volumes/Macintosh\ HD/Users/marcus/Desktop/EDID-Fix/DisplayVendorID-* /Volumes/Macintosh\ HD/System/Library/Displays/Contents/Resources/Overrides/
- Reboot to your system

##  Configuration

| Items       | Model               |
| ----------- | ------------------- |
| Motherboard | AsRock H410M |
| CPU         | Intel Core i3-10100 |
| RAM         | KLEVV 2x16G 2666 MHz |
| GPU | UHD 630 |
| Sound Card  | Realtek ALC887      |
| Ethernet    | (Onboard)           |
| WLAN        | Intel Dual Band Wireless-AC 3168 |


##  Function
- [x] Onboard sound card
- [x] Onboard network card
- [x] Nuclear is hard to solve
- [x] wifi/Bluetooth ([ Great God's intel network card driver ](https://docs.oiw.workers.dev/itlwm/))
- [x] sleep/wake up
- [x] USB2.0 / USB 3.0
- [x] DRM
- [x] Nuclear display dp/hdmi output

##  Tutorial
https://dortania.github.io/OpenCore-Install-Guide/

## Create Bootable USB Mac Installer
- [https://github.com/corpnewt/gibMacOS](https://github.com/corpnewt/gibMacOS)
- [https://intozoom.com/gibmacos-create-bootable-usb/](https://intozoom.com/gibmacos-create-bootable-usb/)
- [https://diskmakerx.com/download/](https://diskmakerx.com/download/)


