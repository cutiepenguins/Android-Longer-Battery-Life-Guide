# Android Longer Battery Life Guide
Hello. In this guide, I will inform you about how to have longer battery life. Let's begin!
## Factors That Cause Your Battery to Drain Faster
- **Location services**
- **Bluetooth**
- Keeping **mobile data** and **Wi-Fi** enabled at the same time
- Keeping **brightness too bright**
- Keeping **apps running in the background**
- **Watching videos at high resolutions**
- **Performing resource intensive tasks a lot** - such as gaming, especially gaming with high settings
Of course these are known factors and managing them should be your first step for a longer lasting battery. Now let's get into more detailed parts.
## Major Suggestion - Install A Custom ROM (Optional)
- First of all, I definitely suggest you to install a **custom ROM** because stock ROMs are full of **bloatware (unwanted apps)** and custom ROMs are more **lightweight** and generally **barebone**. The ROMs I can suggest is **LineageOS**, if your device is not supported, I suggest **CrDroid** instead.
- If you want to keep using your current ROM, you can skip to [the next step].
- Assuming you installed one of these ROMs or any other **Vanilla ROM**, I am continuing with my next suggestion after installing a Vanilla ROM: **MicroG**
### MicroG
- MicroG is an **open source re-implementation of Google services and libraries** and all you have to do is **installing .apk files from the** [website](https://microg.org/download.html). It is so easy! Also, **Huawei** devices can also use MicroG! However, if you want to use MicroG on **another custom ROM**, you should take a look at [this article](https://github.com/microg/GmsCore/wiki/Signature-Spoofing), otherwise, MicroG **won't work** on your device!!!
  - After installing MicroG, you should change **microG Settings app's** battery optimization to `Unrestricted`.
    - Next, simply log in your Google account inside the app and open your system's **Settings** app.
      - After opening settings, go to `Passwords, passkeys & autofill` and click on your google account. Next, go to `Account preferences` and enable the two options you see.
    - Now go back to **microG Settings app** and enable **Google device registration, Cloud Messaging and Google SafetyNet**.
      - For Location modules, you need to install `Nominatim` from **F-Droid**. This is mandatory to be able to use map.
      - For the network-based geolocation module, I suggest you to install `Apple UnifiedNlp Backend UnifiedNlp location provider (Apple Wi-Fi)` from **F-Droid**. After installing, go back to **microG Settings app** and go to `Location modules`, next, enable `Nominatim` and `Apple Wi-Fi`.
- The last step after configuring MicroG is installing a **store app**. My suggestion is [Aurora Store](https://auroraoss.com/), it's an **open source Play Store alternative** and it **doesn't send any telemetry to Google**.
## Other Suggestions - For Everyone Regardless of the ROM
- If your manufacturer lets you to reduce **screen resolution**, choose the reduced screen resolution. If not, you can still make it using **ADB** but you need a computer for it.
  - You can install, set up and connect your phone to ADB [following this guide](https://www.xda-developers.com/install-adb-windows-macos-linux/)
  - After connecting, google your phone model and check its native resolution. For my case, my phone **Xiaomi Redmi Note 8's** native resolution is `1080x2340` which makes it **1080p**, so I'll reduce to **720p** to balance quality and battery life.
  - After the step, execute this command to change screen resolution:
    - `adb shell wm size [resolution]` - for **Xiaomi Redmi Note 8**, `720x1565` is an ideal value for resolution. You can experiment it to make it fit your screen.
  - After reducing resolution, you can notice that items on your screen now look way bigger. So, we should change **DPI (dots per inch)** to balance it.
    - `adb shell wm density [DPI value]` - for **Xiaomi Redmi Note 8**, `270` is an ideal value for DPI. You can experiment it for your screen.