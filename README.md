# Magisk Module Template

This `README.md` will be shown in Magisk Manager. Place any information / changelog / notes you like.

**Please update `README.md` if you want to submit your module to the online repo!**

Github has its own online markdown editor with a preview feature, you can use it to update your `README.md`! If you need more advanced syntax, check the [Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

For more information about modules and repos, please check the [official documentations](https://github.com/topjohnwu/Magisk/blob/master/docs/modules.md)

---
# **Global Optimized GPS File Replacer**
## Description
This module replaces the default gps.conf file - which is responsible for the correct GPS operation, with a new one correctly edited for a better improvement and faster locking.
The original file found in most ROMs is very wrong and has a lot of bad information and settings for the correct operation of the GPS and A-GPS. That's the reason I did this module.
## Changelog
1 - Now basically the A-GPS data files are XTRA 3.0 files (It provides GPS, GLO and BDS assistance data) served over HTTPS with SSL and without # preceding the address lines while the default on mostly ROMs was XTRA 2.0 (provides only GPS and GLO) served over HTTP without SSL, this allows an attacker to mount a MITM attack on the network level and modify the GPS assistance data while in transit.
2 - I switched the XTRA_VERSION_CHECK from 0 to 3 because it's obvious that xtra3grc.bin are XTRA 3.0 files.
3 - I included the address servers from pool.ntp.org as the main NTP server because it's global, the system will try finding the closest available servers for you.
4 - I set SUPL_HOST google.com as default, before was qxwz.com on some ROMs and this is an A-GPS server in China. Google server is more "Global" and can do the job very well.
5 - I updated the SUPL version from 2.0 to 3.0
6 - I changed the SUPL_MODE from 3 (so bad, this option doesn't even exist) to 0x2 (MSA), under normal circumstances, the MSA method is applicable to situation which the satellite signal is poor, to achieve a single positioning.
7 - Changed the value of GPS CAPABILITIES from 0x37 to 0x35 for correctly MSA mode functionality.
8 - Changed the LTE Positioning Profile Settings from 0 (RRLP) to 3 (LPP_User_Plane and LPP_Control_Plane)
9 - Changed the A-GLONASS Positioning Protocol from 0 to 0x4 (LLP Uplane)
10 - The reason for the 8 and 9 changes is because SUPL 3.0 doesn't support RRC and RRLP anymore.
## Requirements
- A device with Qualcomm Snapdragon chipset based
- Magisk indeed
## Instructions
It's Magisk install-able, don't install it by TWRP but with Magisk instead!
1 - Go on Magisk > Modules > Click on "+" yellow button > Search for this .zip file and long press, select open and after installed then reboot your device.
2 - Make sure your location settings is setup on mode "High accuracy"
3 - Skirt outdoors, can be in the yard of your house or anywhere else with a line of sight to the sky, download some Compass app on Google Play Store (I recommend the Compass Steel 3D) and then calibrate the compass.
4 - Stay in that outdoor place and download GPS Locker on Google Play Store and open the app and wait for the first time fix/lock. This is necessary and essential because the app will recognize some GPS satellites signals for the very first time.

Note 1 - Location mode "Battery saving" is gone due to Google's location accuracy is now a binary setting.
Note 2 - Consider using the GPS Locker app because it is much better than the GPS Test and GPS Data. You just need to open it once and wait for fix, then your gps signal is locked and when you close it the app keep awake running in the background. (just press Cancel in "Unlock GPS on exit" message).
Note 3 - GPS was made to work on outdoor places. For indoor/enclosed places such as inside of your house don't forget that, it will take a few minutes to fix. It drains more battery, but is required if you're an advanced user that use gps all the time.
## Links
[Module XDA Forum Thread](https://forum.xda-developers.com/mi-5/how-to/step-step-definitive-gps-solution-global-t3695769 "Module official XDA thread")

[Latest stable Magisk](http://www.tiny.cc/latestmagisk)
