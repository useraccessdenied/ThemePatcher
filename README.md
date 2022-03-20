# ThemePatcher
Tired of buying themes in Oppo or Realme device? Use This Patcher to unlock all the paid themes , for free !

This script lets you unlock all the paid themes, fonts and wallpapers for free from the Theme store in any Oppo or Realme device.
## Disclaimer
This Patcher only works in Oppo or Realme devices (ColorOs and RealmeUi) and **was not tested** to any other device. BE CAREFUL BEFORE USING IT TO OTHER DEVICES.

## How to use
This script is for **Windows** and needs **ADB** (Android Debug Bridge) installed to work. [Install ADB](https://developer.android.com/studio/releases/platform-tools)

While setting up , If you get any prompt in your android device asking you to **allow usb debugging** , click on the allow button.

You need to repeat the following actions every time you want to get a paid theme/font/live wallpaper as free.

1. Tap on the build number **seven times** in your android device to enable developer options.

2. Go to developer options , then turn on **usb debugging** and also turn on **Disable Permission Monitoring** *if it exists*.

3. Connect your phone to the Windows pc using an usb cable.

4. Open **File Explorer** in the pc , then navigate to the directory in which you have **ADB** installed.
 
5. Download the provided file **ThemePatcher.bat** into that exact directory.

6. Open Theme Store in the android device, choose whatever paid themes you like and click **Free trial**.

7. Open the file **ThemePatcher.bat** you just downloaded in your pc.
 
8. ThemePatcher should now automatically detect your device and all of the installed trial themes , fonts or live wallpapers... And will automatically convert them to permanent themes !

Once you're done, just close the terminal window and unplug your android device from the pc...

## Alternate method
If you don't have **ADB** installed and want to do it through [WebADB](https://app.webadb.com) , you cannot run the entire batch file.

In that case- enable developer options, enable usb debugging and disable permission monitoring, then connect your android device to WebADB website.

After that, copy these code snippets and run inside the interactive shell -

1. Patch themes
```
settings put system persist.sys.oppo.theme_uuid -1
settings put system persist.sys.oplus.theme_uuid -1
settings put system persist.sys.trial.theme 0
settings put secure persist.sys.oppo.theme_uuid -1
settings put secure persist.sys.oplus.theme_uuid -1
settings put secure persist.sys.trial.theme 0
```

2. Patch fonts
```
settings put system persist.sys.trial.font 0
settings put secure persist.sys.trial.font 0
```

3. Patch live wallpapers
```
settings put system persist.sys.oplus.live_wp_uuid default_live_wp_package_name
settings put system persist.sys.oppo.live_wp_uuid -1
settings put system persist.sys.trial.live_wp 0
settings put secure persist.sys.oplus.live_wp_uuid default_live_wp_package_name
settings put secure persist.sys.oppo.live_wp_uuid -1
settings put secure persist.sys.trial.live_wp 0
```
Keep in mind , you need to run the entire code of a specific category to correctly patch it. Otherwise, it may not work.

Thank you.
