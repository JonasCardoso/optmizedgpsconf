# Global Optimized GPS File Replacer
This module provides an improved GPS functionality with a better and faster accuracy location reference.

## How it works?
   The stock android **_gps.conf_** file found in *"/system/etc/gps.conf"* or *"/system/vendor/etc/gps.conf"* is replaced with a new one correctly edited for a better improvement and faster satellite signals fix/lock.  
   This file is responsible for the correct GPS operation and functionality.  
   The default file found in most ROMs is very wrong and has a lot of bad information and settings for the correct operation and functionality of the GPS and A-GPS.  
   
## Requirements
- A device with Qualcomm Snapdragon chipset based.
- Rooted with Magisk and Magisk Manager indeed installed.

*__Note:__ Tested on the Xiaomi MI 5 running Android Nougat 7.1.2/LineageOS 14.1 and MIUI 9 Stable 9.5.2.0 and Android Oreo 8.1.0/LineageOS 15.1 and MIUI 10 Global Beta 8.6.21 with Magisk v16.4 (Beta).*

## Instructions
__It's Magisk install-able, don't install it by TWRP but with Magisk instead!__

#### Option 1 - Manually
1. Go to Magisk Manager **_Modules_** section.
2. Click on **_+_** yellow button and search/find for this **_"optimizedgpsconf.zip"_** file and long press on it.
3. Select open and after installed then reboot your device.
4. After rebooted your device, make sure your location settings is setup on mode **_Device only_**.
5. Skirt outdoors, can be in the yard of your house or anywhere else with a line of sight to the sky and stay in that outdoor place.
6. Download some Compass app on Google Play Store *(I recommend the **Compass Steel 3D**)* and then calibrate the compass.
7. Download **_GPS Locker_** app on Google Play Store and open the app and wait for the first time fix/lock. *This is necessary and essential because the app will recognize some GPS satellites signals for the very first time.*

#### Option 2 - Download
1. Go to Magisk Manager **_Downloads_** section.
2. Search/Find **_"Global Optimized GPS File Replacer"_**.
3. Tap on the download button and then on **_INSTALL_**.
4. Wait a moment to finish downloading and installing.
5. When finished tap on **_REBOOT_**.
6. Same **_4, 5, 6 and 7_** steps of **_Option 1 - Manually_**.

   *__Note 1:__ Location mode __"Battery saving"__ is gone due to Google's location accuracy is now a binary setting. So consider using the __"High accuracy"__ mode one.*  
   *__Note 2:__ Consider using the __GPS Locker__ app because it is much better than the __GPS Test__ and __GPS Data__. You just need to open it once and wait for fix, then your gps signal is locked and when you close it (just press __Cancel__ in __"Unlock GPS on exit"__ message) the app keep awake running in the background.*  
   *__Note 3:__ GPS was made to work in outdoor places. For indoor/enclosed places such as inside of your house don't forget that, it will take a few minutes to fix. It drains more battery, but is required if you're an advanced user that use gps all the time.*  
   
## Changelog
#### ~~Version 1.0~~
- ~~Initial release~~ 

#### Version 2.0
- Last update and final version. *Now it works fine for both Android Nougat & Oreo ROMs and is correctly replacing the gps.conf file in corresponding directory path.*

#### Version 2.1
- Template 1500 -> 17000.

## Links
- [Module XDA Xiaomi MI 5 Forum Thread](https://forum.xda-developers.com/mi-5/how-to/step-step-definitive-gps-solution-global-t3695769)
- [GitHub Module Page](https://github.com/Magisk-Modules-Repo/Global-Optimized-GPS-File-Replacer)
