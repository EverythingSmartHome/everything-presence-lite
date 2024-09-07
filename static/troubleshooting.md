---
layout: default
title: Troubleshooting
nav_order: 13
---

# FAQ

{: .no_toc }


{: .warning-title }
Please make sure you have updated your EPL to the latest available firmware by going to [Updating](https://everythingsmarthome.github.io/everything-presence-lite/updating.html){: .btn .btn-blue }


Lets cover off some of the commonly asked questions.
{: .fs-6 .fw-300 }

## Everything Presence Lite

**Will the EPL detect moving animals or objects?** Yes the EPL will detect any moving thing; a pet, fan or even even moving objects such as blinds.

**Help, my sensor is giving false detections!** The vast majority of the time, the sensor is detecting movement accurately, but users aren't aware of how tiny a movement it is able to detect. Make sure to check out the [tuning guide](https://everythingsmarthome.github.io/everything-presence-lite/tuning.html) for tweaking the settings to get the best results!

**Can the sensor detect the direction of motion or zones?** 
No, it will only show a detected or not detected status. 

**I prefer to 3D print my own case** No worries you can find the files you need here [https://www.printables.com/model/624830-everything-presence-lite-official-case](https://www.printables.com/model/624830-everything-presence-lite-official-case "https://www.printables.com/model/624830-everything-presence-lite-official-case")

**My EPL stops updating occupancy after some time, light levels are still reported fine.**
There was a problem with earlier firmware versions of the LD2450 mmWave sensor used by the EPL which can cause a loss of communication until power-cycling the whole device.

1. In Home Assistant, enable the mmWave Bluetooth entity if disabled, then toggle it **ON**.
2. Install and open Hi-Link's HLKRadarTool app [Android](https://play.google.com/store/apps/details?id=com.hlk.hlkradartool)/[iOS](https://apps.apple.com/us/app/hlkradartool/id1638651152), stand physically close to the EPL, then connect to the LD2450 and perform an OTA firmware update to at least version 2.04.23101915
3. If the iOS version of HLKRadarTool crashes, try [RadarTools](https://apps.apple.com/gb/app/radartools/id6502672452) instead
4. In Home Assistant, toggle the mmWave Bluetooth entity **OFF** to prevent unauthorised access to the LD2450 and disable the entity if it's no longer needed
