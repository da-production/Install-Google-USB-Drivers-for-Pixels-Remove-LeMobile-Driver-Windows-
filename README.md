# Install-Google-USB-Drivers-for-Pixels-Remove-LeMobile-Driver-Windows-
 I am not responsible for any damage caused or any data lost. Please make sure you understand the procedure and also make backups of anything important!
 
## Steps:
Developer Options and Enable USB Debugging 
Downloads (Google USB Driver and SDK Platform Tools)
Removing the LeMobile USB Drivers
Installing Google USB Driver to the ADB Interface (Part A)
Install Google USB Drivers to Windows (Important! Part B)
Testing the ADB connectivity (rebooting to the bootloader)
Checking the drivers/device in the bootloader
Add the SDK Platform Tools to the PATH environment variable

### Developer Options and Enable USB Debugging :
First up you need to enable the developer options to do this go to 'about phone' and then tapping on 'build number' seven times or more until it says you are now a developer once done head back and now you can see developer options go to and enable USB debugging then plug-in your phone to your computer and then you should see a little icon in your phone say USB debuggin connected.

### Downloads (Google USB Driver and SDK Platform Tools) :

[Google USB Drivers Windows](https://developer.android.com/studio/run/win-usb)
Follow the instructions 
[Standalone SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools.html)

### Removing the LeMobile USB Drivers : (If you don't LeMobile USB Driver in your Devices Manager you can skeep this step)

open Devices Manager you do have the Lee mobile android device drivers installed
open command prompt as administrator and tape:
```
pnputil /enum-drivers
```
now search whichever has Provider Name: leMobile and locate the 'Published Name' exemple: oem???.inf
then tape: (replace the ??? with right number)
```
puputil /delete-driver oem???.inf /force
```
in the Devices manager right click on Android Composite ADb interface and 'updated' > 'Browser for driver software on your computer' give the path where you have extracted the USB drivers 

### Install Google USB Drivers to Windows (Important! Part B your phone must be plug-in to your computer) :
go to  where you have extracted the USB drivers and right click android_winusb.inf > install
user the platform tools that you downloaded and use ADB command to reboot your own into the bootloader to you can finish configuring a bootloader drivers as well

### Testing the ADB connectivity (rebooting to the bootloader) :
tape cmd in your address bar  of the Explorer window inside ```the platform tools folder``` 
tape ``` adb reboot bootloader``` and this will start the ADB daemon and of course in your phone you might get pop up to allow USB debbugging and tap on always allow from this computer > ok 
tape ```adb reboot bootloader``` to Reboots your phone in the bootloader
and you'll wait for moment it as it does that okay your in the bootloader

### Checking the drivers/device in the bootloader :

then tape: ```fastboot devices``` to check out devices in fastboot which it is and then you can reboot your phone just tape ``` fastboot reboot```

### Add the SDK Platform Tools to the PATH environment variable :(if doesn't existe)
Follow these steps:
My Computer->Property->Advanced->Environment Variables->Edit Path Variable and add “D:\ android-sdk-windows\tools” into the Path Variables. In your computer properties-advance-environment variables-system variable ,and you find variable "path", add your android/tools path in it
 
