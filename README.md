# X88-pro-10-unbrick

### My guide to unbrick X88 pro 10 through mask mode

---

Using Multitool I converted this Android box to a Linux box, but sometimes things do not go as we want. I had to reinstall Linux various time, and not all the flash were successful. I googled and find the information I needed, but they are scattered, so I thought I could write a guide to have it all together.

#### What do you need?

+ Driver Assistant
+ USB A to USB A data cable, probably better if USB 2.0 
+ Firmware file

Here you have two alternatives, both equivalent:
1. FactoryTool (Windows Only)
2. AndroidTool (Windows and Linux, maybe MacOS)
		notice I will provide files only for Windows as I tried them both on the same OS, but you should be able to find them on Google
## Preparing your pc
Download Driver Assistant, extract the archieve and run the exe; click "Install" and wait for it to finish. Reboot your pc.
Download FactoryTool or AndroidTool, extract the archieve and run the exe. 
+ FactoryTool relative path: /FactoryTool_1.66/FactoryTool.exe
+ AndroidTool relative path: /AndroidTool/AndroidTool_Release/AndroidTool.exe

## Enter Mask Mode
Mask Mode is, if I understand right, similiar to a computer BIOS.
### How do we enter?
I found this image on Armbian forum.
![IMG-20230105-202824](https://github.com/CtrlValCanc/X88-pro-10-unbrick/assets/85836574/115b83b4-10ed-4079-8b70-41a61e8b079a)
You need to make contact between this (yellow and blue) two pins (I personally used some tweezers).
While keeping doing contact, we put the DC cable so the device turns on. 
You then should be hearing the classic Windows "plugged in" noise. 
Check your software to see if it's connected.
+ In Factory Tool, you should see under "Device Type" _MaskRom_ or something similiar. Everything that's not Hub should be right.
+ In Android Tool, you should see "Found One MASKROM Device".

## Factory Tool

+ Open FactoryTool.exe
+ At the top left, you see "Firmware". Click it and navigate to your firmware image (X88pro_B_rk3318_d4_11.0_SP6330_20210125_r1(X88pro10 1.0.1).img).
+ Check Restore (and not upgrade).
+ Choose your MaskRom device and press "Run"
It should take some time and then you should be greeted with a green "Success".
Notice: it might fail because it waits for a MaskRom device. While the program is going, check if it waits for a MaskRom device. If yes, you can redo the steps in _Enter Mask Mode_ and see if it works.

## Android Tool

+ Choose "Upgrade Firmware" tab
+ Navigate to your firmware image (X88pro_B_rk3318_d4_11.0_SP6330_20210125_r1(X88pro10 1.0.1).img).
+ Choose Switch (!!NOT SURE ABOUT IT!!) or Upgrade
+ Wait for it to end.


Now the device should boot and show the purple-blue "X88 PRO 10" boot image.

If not, try again.


