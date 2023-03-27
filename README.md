# Opencore EFI for an MSI H410i Pro Wifi hackintosh, which runs macOS 10.15 (Catalina)

Configured for this hardware:

>MSI h410i Pro Wifi

>Intel Core i5-10400

>Intel UHD Graphics 630

>Non-apple 500GB NVME drive

>Generic case with two USB 3.0 ports

Some troubleshooting and manual editing may be required for software:

>If you want to run a different version of macOS than Catalina, I doubt much configuration will be needed, but it is required, so follow this guide: https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html

>Because this EFI is using the Release version of Opencore and its kexts, you may need to swap everything for their debug counterparts.

>Changing the Serial Number, Board serial, Apple ROM, and GUID (**REQUIRED**)

And of course, different hardware will require different configs. While I can't cover everything, here's some common changes to your system that may require changing the EFI:

>Changing the System product name to something else, the current one works for me but may need to be changed for the version of macOS or the hardware being run.

>A case with different ports, which will require modifying the USB map. You shouldn't need any new kexts, but I'm pretty sure you need to install Windows or linux, then run SSDTime to compile the SSDTs related to USB. Guide: https://dortania.github.io/OpenCore-Post-Install/usb/#macos-and-the-15-port-limit

>A processor with a different iGPU model, guide: https://dortania.github.io/OpenCore-Post-Install/gpu-patching/intel-patching/

>A SATA drive, which means you need to delete NVMEFix.kext

There are a few minor issues with this EFI. I probably won't fix them because I don't need to for my build, but you may want to take note of these:
>Cannot do 60hz on HDMI at any resolution over 1440p (I recommend installing RDM after macOS is set up so you can actually change the resolution instead of macOS just changing the scaling). You'll have to use displayport if you want 4K at 60hz.

>No startup chime (because I was too lazy to setup AudioDXE), guide: https://dortania.github.io/OpenCore-Post-Install/cosmetic/gui.html#setting-up-opencore-s-gui


# My BIOS Settings
>going to write soon
