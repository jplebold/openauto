# Josh's Notes

reated: 6/1/2019

Notes:
- following instructions from https://github.com/f1xpl/openauto/
- had to install aasdk as well (as the wiki instructions indicated)
- the git repo's were cloned to /opt/openauto
- have to connect the phone via usb to the pi for this to work. USB is not supported by the pi out of the box - (https://github.com/f1xpl/openauto/wiki/udev-rules-(USB-permissions). I manually added just 1 entry to udev for Samsung, after being concerned about lax permissions with the instructions in wiki (https://github.com/f1xpl/openauto/issues/59)
- i changed one of the source files within OpenAuto, which is to 'fix' an issue where the phone would connect then openauto would quickly crash/lose the phone. Details are https://github.com/f1xpl/openauto/issues/157, the specific fix is committed in my local git log, but is the fix described in this comment: https://github.com/f1xpl/openauto/issues/157#issuecomment-473604273
   - i then found a 'cleaner fix' which adds an actual timestamp. i've made the adjustments to my local code and git log. details here: https://github.com/Oper92/openauto/commit/f05074e26758be7edac1208c7c3e7eb3e7292605


# OpenAuto

### Support project
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=R4HXE5ESDR4U4)

**OpenAuto Pro version** provides features like brightness control, volume control, support of Kodi and integration with the Raspberry PI OS (Raspbian Desktop). [See how it works at OpenAuto Pro overview video](https://www.youtube.com/watch?v=9sTOMI1qTiA)

If you are looking for the car power supply with ignition state detection [go to the Blue Wave Studio page](https://bluewavestudio.io/index.php/bluewave-shop)

For support of other platforms please contact me at f1xstudiopl@gmail.com

### Community
[![Join the chat at https://gitter.im/publiclab/publiclab](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/openauto_androidauto/Lobby)

### Description
OpenAuto is an AndroidAuto(tm) headunit emulator based on aasdk library and Qt libraries. Main goal is to run this application on the RaspberryPI 3 board computer smoothly.

[See demo video](https://www.youtube.com/watch?v=k9tKRqIkQs8)

### Supported functionalities
 - 480p, 720p and 1080p with 30 or 60 FPS
 - RaspberryPI 3 hardware acceleration support to decode video stream (up to 1080p@60!)
 - Audio playback from all audio channels (Media, System and Speech)
 - Audio input for voice commands
 - Touchscreen and buttons input
 - Bluetooth
 - Automatic launch after device hotplug
 - Automatic detection of connected Android devices
 - Wireless (WiFi) mode via head unit server (must be enabled in hidden developer settings)
 - User-friendly settings

### Supported platforms

 - Linux
 - RaspberryPI 3
 - Windows

### License
GNU GPLv3

Copyrights (c) 2018 f1x.studio (Michal Szwaj)

*AndroidAuto is registered trademark of Google Inc.*

### Used software
 - [aasdk](https://github.com/f1xpl/aasdk)
 - [Boost libraries](http://www.boost.org/)
 - [Qt libraries](https://www.qt.io/)
 - [CMake](https://cmake.org/)
 - [RtAudio](https://www.music.mcgill.ca/~gary/rtaudio/playback.html)
 - Broadcom ilclient from RaspberryPI 3 firmware
 - OpenMAX IL API

### Remarks
**This software is not certified by Google Inc. It is created for R&D purposes and may not work as expected by the original authors. Do not use while driving. You use this software at your own risk.**
