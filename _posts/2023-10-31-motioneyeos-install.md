---
layout: post
title: "MotionEyeOS Raspberry Pi Zero W Install"
date: 2023-10-31 17:45:36 -0500
categories: [raspberrypi,motioneyeos,camera]
tags: [raspberrypi,raspberry,motioneyeos,camera,nvr] #all tags MUST be lowercase
---

##### Things you will need first:

- [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/files/latest/download)
- The [latest motioneyeos](https://github.com/ccrisan/motioneyeos/releases) image
- [Notepad++](https://notepad-plus-plus.org/download/v7.4.2.html)

 1. Download the latest motioneyeos image.
 2. Extract the image to your hard drive (using Winzip, 7Zip, etc.)
 3. Write the image to your microSD card using Win32DiskImager.
 4. DO NOT EJECT THE SD CARD yet.
 5. Open Windows Explorer and browse to your drive containing the microSD card. You should see files such as:
    - bootcode.bin
    - loader.bin
    - start.elf
    - kernel.img
    - cmdline.txt
 6. Right-click in the right window pane and select `New Text Document`.
 7. Now, right click on this file and rename it `wpa_supplicant.conf`. Make sure to remove the `.txt` file extension.
 8. Once again, right click on this file and select `Edit with Notepad++`.
 9. Make sure you set the EOL conversion to UNIX LineFeeds (Edit-->EOL Conversion-->Unix LF).
10. Paste the following contents into your blank file (obviously changing the ssid and psk to match yours):

```
        country=US
        update_config=1
        ctrl_interface=/var/run/wpa_supplicant
        
        network={
            scan_ssid=1
            ssid="MyWiFiSSID"
            psk="S3cr3tp@$$w0rc|"
        }
```

 1. Change the country code to the country in which this device is currently operating. You can get the list of country codes [here](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2).
 2. Save the file.
 3. Eject your microSD card safely.
 4. Insert this microSD card into your device, e.g. Pi Zero W.
 5. Optionally, attach a camera to your device.
 6. Apply power to your device.
 7. If you have a monitor attached to the device, you should see the wireless network service starting, wpa_supplicant being read and 'brcmfmac Done'.
 8. Shortly, you should see your IP address being displayed along with your gateway and DNS servers.
 9. Using your favorite browser, browse to the IP address that was displayed and log in to the device using the default motioneyeos credentials of: admin / \[blank password\]
10. You can shut down the motioneye os remotely by select the advanced settings-->shutdown

**Note:** If you do not have a display attached to your 
zero, you can use nmap to scan your home network for any new devices / 
ip's.  Look for one labeled "(Raspberry Pi Foundation)"

##### Initial Login

The web user interface allows you to configure pretty much everything. You'll probably want to enable the advanced settings option. Here are the most important things you should take care of when configuring your motionEyeOS for the first time:

    set a password for the two users (admin and user)
    set the correct timezone for your region
    enable the wireless connection, if you have one
    configure your video device(s) (resolution, framerate etc)
    configure the file storage if you want your pictures/movies saved on a network or USB drive
    enable still images and/or motion movies if you want any information to be recorded

The installed camera devices are normally automatically detected and configured for you, but you can however add more devices (including remote devices) from the settings panel.