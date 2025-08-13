# AI_Plus_Pulse
Unlock, root and general details about the AI+ Pulse (4G, 64GB) variant - Unisoc T615

# Bootloader Unlock Guide
1. Download ums9230_universal_unlock.zip attached here and extract
2. Download and extract the SPD driver attached here
3. The driver is in the "Win10\Drivers" folder
4. Toggle OEM unlock in developer settings 0 On the phone
5. Power off the device
6. Hold Volume Down (-) and connect the device to your pc
7. Run: unlock_autopatch_9230.bat
8. Wait For Script to complete, and proceed with the instructions while tunning the .bat file
9. At the end, the device should automaticlly reboot and be unlocked
10. Note that the boot image will be dumped to a file called "boot.bin"
11. The image will be from the current active slot

# Device Paritioning Details
1. GSI Variant - xx-arm64-ab.img
2. VNDK Version - 33.0
3. VNDK is not in lite mode
4. Manifest Location - Modern
5. SaR - True
6. Seamless Upgrades - True
7. Dynamic Parititons - True
8. Binder Architecture - arm64
