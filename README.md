# X88-pro-10-unbrick-linux-armbian

### My guide to unbrick X88 pro 10 with Linux (armbian) installed through mask mode

---
This guide explains how to unbrick or reinstall Linux (Armbian) on the X88 Pro 10 TV box using Mask Mode.

I had to reinstall Linux several times on this device, and since the information I found online was scattered, I decided to write a complete step-by-step guide.

#### What do you need?

+ Driver Assistant
+ USB A to USB A data cable, better if USB 2.0 
+ Firmware file

You can use one of two equivalent flashing tools::
+ FactoryTool (Windows Only)
+ AndroidTool (Windows and Linux, possibly MacOS).  
In this guide, I’ll focus on Windows, but you can easily find the Linux equivalents online.

## Preparing your pc
Download Driver Assistant
1. Extract the archive and run the .exe file
2. Click Install and wait for it to finish
3. Reboot your PC

Download FactoryTool or AndroidTool
1. Extract the archieve and run the exe.
2. FactoryTool relative path: /FactoryTool_1.66/FactoryTool.exe
3. AndroidTool relative path: /AndroidTool/AndroidTool_Release/AndroidTool.exe


## Enter Mask Mode
Mask Mode is similar to a computer’s BIOS: it allows you to communicate with the device even if the system won’t boot.

### How to enter Mask Mode
I found this image on Armbian forum.
![IMG-20230105-202824](https://github.com/CtrlValCanc/X88-pro-10-unbrick/assets/85836574/115b83b4-10ed-4079-8b70-41a61e8b079a)
1. Locate the two pins shown in the picture (yellow and blue).
2. Use a metal tweezer or small wire to short the two pins.
3. While keeping them shorted, connect the USB cable to power on the device.

#### Alternatively, some users report that inserting a toothpick into the AUX port (until you hear a “click”) can also trigger Mask Mode.

Once connected, your computer should play the usual “device plugged in” sound.
Check your software to see if it's connected.
+ In Factory Tool, you should see under "Device Type" _MaskRom_ or something similiar. Everything that's not Hub should be right.
+ In Android Tool, you should see "Found One MASKROM Device".

## Factory Tool

1. Open FactoryTool.exe
2. At the top left, you see "Firmware". Click it and navigate to your firmware image (X88pro_B_rk3318_d4_11.0_SP6330_20210125_r1(X88pro10 1.0.1).img).
3. Check Restore (and not upgrade).
4. Choose your MaskRom device and press "Run"
5. Wait for the process to complete: you should be greeted with a green "Success".
   
Notice: it might fail because it waits for a MaskRom device. While the program is running, check if it waits for a MaskRom device. If yes, you can redo the steps in _Enter Mask Mode_ and see if it works.

## Android Tool

1. Choose "Upgrade Firmware" tab
2. Navigate to your firmware image (X88pro_B_rk3318_d4_11.0_SP6330_20210125_r1(X88pro10 1.0.1).img).
3. Choose Switch (!!NOT SURE ABOUT IT!!) or Upgrade
4. Wait for it to end.


Now the device should boot and show the purple-blue "X88 PRO 10" boot image.

If it doesn’t boot correctly, simply repeat the process: sometimes it takes a couple of tries.


