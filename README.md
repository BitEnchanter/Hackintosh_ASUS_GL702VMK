# Hackintosh ASUS ROG STRIX GL702VSK
Hackintosh Files for High Sierra 13.6 @ ASUS GL702VMK
Thanks @zubenelakrab for your amazing work.

**Specs:**
* Intel Core i7-7700HQ (Intel Core i7)
* 16GB RAM
* NVIDIA GeForce GTX 1060 (Laptop) - 6143 MB
* 128GB x M.2 (Root partition Type: APS) + 1TB x SATA (Backup partition)

**Working:**
* NVIDIA GTX 1060
* Audio (Internal Speakers + HDMI Audio)
* Sensors 
* Ethernet
* Audio Jack
* USB 3.0/3.1, Thunderbolt, USB Type C, HDMI, Mini Display Port, Card Reader
* Webcam
* Built-in WIFI card
* CPU/GPU Fans
* Battery
* 1080P Display (1920 x 1080) **No GSYNC.*
* Built-in microphone

**Not working:**
* Touchpad
* Built-in Bluetooth card(There's driver but it can't function correctly with my iPhone and Airpods Pro)
* Keyboard Backlight
* Some FN keys
* Temperature Sensors

**Tips**
After install kexts check permissions and update kextcache 

a. to repair permissions use Kext Wizard or 

```
sudo chmod -Rf 755 /S*/L*/E*
sudo chmod -Rf 755 /L*/E*
sudo chown -Rf 0:0 /S*/L*/E*
sudo chown -Rf 0:0 /L*/E*
```

b. to update kextcache

```
sudo kextcache -i /
```

# Abbreviations
* /L/E = /Library/Extensions
* /S/L/E = /System/Library/Extensions

# Creating USB Stick

# Fixing USB Stick KEXTS

1. Mount your USB Stick EFI Volumen
2. Replace all kexts in your EFI volumen with EFI.zip kexts (*/EFI/CLOVER/kexts/Other/*)
3. Delete any other folder in /EFI/CLOVER/kexts (keep only Other)
4. Restart & Boot with your USB Stick

# Pre-Install 

DISABLE(Lock) Secure Boot, Fast Boot Intel VT-d, virtualization support and CSM support in your BIOS. 

# Installing

Change the clover config from nvda_drv=1 to nv_disable=1 until you finish Nvidia Web Driver installation

# Post-Install

If the nvidia web driver isn't working after reboot just press space during clover bootloader stage and choose boot with selected options.

# High Sierra updates
High Sierra can be updated from App Store but after this action kexts path permissions must be fixed using Kext Wizard (or command-line)
