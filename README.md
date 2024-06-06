# ps42-8rc-hackintosh
Hackintosh for MSI PS63 Modern
Specifications
Part	Model	Note
CPU	Intel Core i7-8565U	
Integrated GPU	Intel UHD Graphic 620	
Dedicated GPU	NVIDIA GTX1050 Max-Q	
RAM	DDR4-2400 SO-DIMM 24GB	
SSD 1	Transcend 220s 1TB	
SSD 2	HP SATA M.2 SSD 512GB	Installed macOS on this drive
Screen	15.6' IPS 1920 × 1080	
Wi-Fi/Bluetooth	Intel Wireless AC9560	Works by using itlwm kext
Card Reader	Realtek	
Webcam	720p	Keyboard Toggle (Fn + F6) works perfectly
Hackintosh Status
System Information of my laptop

Here is what I installed and used as a daily driver.

Operating Systems - Dual-boot macOS Catalina 10.15.6 and Windows 10 each on its own SSD.
OpenCore - version 0.6.0
Checklist
Here is a list of what works, what don't.

 CPU Power Management
 Sleep
 Battery Monitoring
 Integrated GPU
 HDMI
Not tested with screens with a resolution greater than FHD
Not tested for audio output
 USB Type-C to HDMI via a dongle
 Sound + Microphone
 Audio Jack (Hotpluggable)
 Speaker
 Wi-Fi (Works but slower than usual)
 Bluetooth
 Webcam
 Trackpad
 macOS native gestures
 Keyboard
 Brightness and volume up/down keys
 Print Screen key (Mapped it to macOS's F13)
 Webcam/Built-in Microphone key (Fn + F6)
 Fingerprint Sensor (There is no workaround.)
 Card Reader (There is no workaround.)
To-Do List
 Add OpenCore Boot Picker GUI
 Install an actual Broadcom Wi-Fi NIC
 Adjust the trackpad so that it feel better to use.
 Upgrade to a newer OpenCore version
 Update macOS to Big Sur
 Make DRM works for Apple TV
 Swap from itlwm (for Intel Wi-Fi) to airportItlwm for better user experiences.
Guide Used
Installation Guide: https://dortania.github.io/OpenCore-Install-Guide/
Post-installation Guide: https://dortania.github.io/OpenCore-Post-Install/
Prerequisites
Bios
Turn off Secure Boot
Turn off CFG Lock
Enter the Bios
Press ALT + right CTRL + F2 + right SHIFT to enable advanced BIOS Menu
Power & Performance
CPU - Power Management Control
CPU Lock Configuration
CFG Lock
SMBIOS
I used MacBook Pro 15, 2018 SMBIOS.

Post Installation Checklist
Checked item means I already followed the guide in that section. Please note that the hierarchy follows this guide.

Universal
 Security and FileVault
 Fixing Audio
 Booting without USB
 Updating OpenCore, kexts and macOS
 Fixing DRM
 Fixing iServices
 Fixing Power Management
 Fixing Sleep
 USB
 USB Mapping
 Fixing USB Power
 Fixing Shutdown/Restart
 GPRW/UPRW/LANC Instant Wake Patch
 Keyboard Wake Issues
 GPU
 Disabling laptop dGPU
 - Thunderbolt
 NICs
 NVMe
 CPU Power Management
 Displays
 NVRAM
 RTC
 IRQ Conflicts
 Audio
 SMBus
 TSC
 Fixing USB
Laptop Specifics
 Fixing Battery Read-outs (Didn't follow because it is already work out-of-the-box)
Cosmetics
 Add GUI and Boot-chime
 Fixing Resolution and Verbose
Multiboot
 Setting up Bootstrap.efi
 Installing BootCamp
Miscellaneous
 Fixing RTC
 Fixing CFG Lock
 Emulated NVRAM
Advices
Since I cannot remember all the details how I configured the EFI. Here are some tips following the guide.

Read the guide multiple times.
Follow the provided guide carefully.
Make a checklist for post-installation tasks.
Always Backup your EFI
Use Git (Like what I do here) for Version Controlling
Not Enough EFI Space?
Backup your EFI Partition then follow this: https://www.youtube.com/watch?v=YaPVaAifjl0&ab_channel=LazyTech to expand your EFI partition capacity.
