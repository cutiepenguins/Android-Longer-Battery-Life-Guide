# Android Longer Battery Life Guide
Hello 🤭. In this guide, I will inform you about how to have longer battery life. Let's begin!
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
- If you want to keep using your current ROM, you can skip to [the next step](https://github.com/cutiepenguins/Android-Longer-Battery-Life-Guide/blob/main/README.md#other-suggestions---for-everyone-regardless-of-the-rom).
- Assuming you installed one of these ROMs or any other **Vanilla ROM**, I am continuing with my next suggestion after installing a Vanilla ROM: **MicroG**
### MicroG
- MicroG is an **open source re-implementation of Google services and libraries** that respects your privacy and consumes **way less CPU and other resources** compared to **Google services and libraries**. Also, all you have to do is **installing .apk files from the** [website](https://microg.org/download.html). It is so easy! Also, **Huawei** devices can also use MicroG! However, if you want to use MicroG on **another custom ROM**, you should take a look at [this article](https://github.com/microg/GmsCore/wiki/Signature-Spoofing), otherwise, MicroG **won't work** on your device!!!
  - After installing MicroG, you should change **microG Settings app's** battery optimization to `Unrestricted`.
    - Next, simply log in your Google account inside the app and open your system's **Settings** app.
      - After opening settings, go to `Passwords, passkeys & autofill` and click on your google account. Next, go to `Account preferences` and enable the two options you see.
    - Now go back to **microG Settings app** and enable **Google device registration, Cloud Messaging and Google SafetyNet**.
      - For Location modules, you need to install `Nominatim` from **F-Droid**. This is mandatory to be able to use map.
      - For the network-based geolocation module, I suggest you to install `Apple UnifiedNlp Backend UnifiedNlp location provider (Apple Wi-Fi)` from **F-Droid**. After installing, go back to **microG Settings app** and go to `Location modules`, next, enable `Nominatim` and `Apple Wi-Fi`.
- The last step after configuring MicroG is installing a **store app**. My suggestion is [Aurora Store](https://auroraoss.com/), it's an **open source Play Store alternative** and it **doesn't send any telemetry to Google**.
## Other Suggestions - For Everyone Regardless of the ROM
- My **first** suggestion is **reducing screen resolution**. It **doesn't** help with battery life **drastically** but it sure helps. However, it **drastically improves performance** since your CPU + GPU work under less loads. So, it's good both ways. 
  - If your manufacturer lets you to reduce **screen resolution**, choose the reduced screen resolution. If not, you can still make it using **ADB** but you need a computer for it.
    - You can install, set up and connect your phone to ADB [following this guide](https://www.xda-developers.com/install-adb-windows-macos-linux/)
    -  After connecting, google your phone model and check its native resolution. For my case, my phone **Xiaomi Redmi Note 8's** native resolution is `1080x2340` which makes it **1080p**, so I'll reduce to **720p** to balance quality and battery life.
    - After the step, execute this command to change screen resolution:
      - `adb shell wm size [resolution]` - for **Xiaomi Redmi Note 8**, `720x1565` is an ideal value for resolution. You can experiment it to make it fit your screen.
    - After reducing resolution, you can notice that items on your screen now look way bigger. So, we should change **DPI (dots per inch)** to balance it executing this command:
      - `adb shell wm density [DPI value]` - for **Xiaomi Redmi Note 8**, `270` is an ideal value for DPI. You can experiment it for your screen.
- My **second** suggestion is **using battery saver mode**. However, if it **doesn't** specify that **the battery saver restricts CPU cores**, you don't have to enable it since it only restricts background processes which doesn't help with battery life at all.
  - For example, many **Samsung** phones' battery savers restrict CPU cores while **Redmi Note 8's** battery saver only restricts background processes. So, if your battery saver restricts CPU cores, use it.
  - If not, you can still restrict CPU and GPU usage using a **kernel manager**. However, **your device must be rooted!**. If you won't root your device, unfortunately you can't restrict CPU and GPU usage for a better battery life.
    - If your device **is rooted**, install a kernel manager. My suggestion is `SmartPack Kernel Manager` from **F-Droid**. Simply open the app, grant **root/superuser permissions** and choose the lowest values for your CPU and GPU (you don't have to choose the lowest values if you don't want to maximize battery life because you need performance too). Make sure to enable `Apply on boot` options for both sections.
- **The last** important suggestion is checking your **battery health** and if it's lower than 80%, **replacing the battery**. You can see your battery health installing `AccuBattery` and charging your phone from **14% (or lower)** to **100%**.
- Other suggestions I can make are basic things like **using wallpapers with darker colors, limiting battery usage for apps (app battery optimizations) and avoiding [factors that cause your battery to drain faster](https://github.com/cutiepenguins/Android-Longer-Battery-Life-Guide/blob/main/README.md#factors-that-cause-your-battery-to-drain-faster) etc.**
## Conclusion
This guide was about how to get a longer battery life on your Android device. I hope it has been useful for you. Have a nice day! 🐧
