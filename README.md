# AI_Plus_Pulse
Unlock, root and general details about the AI+ Pulse (4G, 64GB) variant - Unisoc T615

# Bootloader Unlock Guide
1. Download ums9230_universal_unlock.zip attached here and extract
2. Download and extract the SPD driver attached here
3. The driver is in the "Win10\Drivers" folder
4. Toggle OEM unlock in developer settings on the phone
5. Power off the device
6. Hold Volume Down (-) and connect the device to your pc
7. Run: unlock_autopatch_9230.bat
8. Wait For Script to complete, and proceed with the instructions while running the .bat file
9. At the end, the device should automaticlly reboot and be unlocked 
10. Note that the boot image will be dumped to a file called "boot.bin"
11. The image will be from the current active slot
Source - https://xdaforums.com/t/unisoc-t615-bootloader-unlock-root.4734366/

# Device Paritioning Details
1. GSI Variant - xx-arm64-ab.img
2. VNDK Version - 33.0
3. VNDK is not in lite mode
4. Manifest Location - Modern
5. SaR - True
6. Seamless Upgrades - True
7. Dynamic Parititons - True
8. Binder Architecture - arm64

# Specifications
1. Display Size = 6.7 Inch
2. SoC - Unisoc T615
3. GPU - Mali G57 MP1
4. Cores - 6 Little + 2 Big
5. Sensors - Proximity, Ambient Light, Accelerometer
6. Camera (Rear) - 50MP Sensor f/2.0 + Dummy Camera
7. Camera (Front) - 5MP Camera

# OTA Links/Resources
1. There was an initial 55MB OTA without any changelog.
2. AI+ uses incremental OTAs, you miss one, you are done for. No more updates till they ship a full OTA.
3. I did not capture the OTA Link, so please feel free to open a PR.
4.  OTA Links - <OTA_1> Missing, <OTA 2> Aug - 13 ( https://android.googleapis.com/packages/ota-api/package/e2579cebef64c415c429badeb2f5c3a7f1d45196.zip )
  Note that OTA 1 was an incremental OTA. Judging by it's size it was probably an OTA for Security Patch (July 2025).
  Also, during the BL unlock process, boot image from your current active slot is dumped.
  Avoid Changing Any other slots/partitions as we do not have a stock ROM dump available as of yet. And yes, this includes VBmeta (use fastboot flash --disable-verity --disable-verification boot_<active_slot> <Boot.img> to disable verity)
5. https://android.googleapis.com/packages/ota-api/package/dba15107a7277505e52af5b83d3fa8bdfab64c55.zip - Update title NxtQuantum OS New Version Release (October patch, incremental update)
6. https://android.googleapis.com/packages/ota-api/package/234865891b3ab005b7e9e834a41f502bafb44de2.zip - Update title - "New version discovered! Experience optimization and security upgrade" (Size is 342 MB, an incremental update)
