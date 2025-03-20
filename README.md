# Android Longer Battery Life Guide
Hello 🤭. In this guide, you will be informed about how to have longer battery life on your Android device. Let's begin!
## Factors That Cause Your Battery to Drain Faster
- **Location services**
- **Auto Sync**
- **Bluetooth**
- Keeping **mobile data** and **Wi-Fi** enabled at the same time
- Keeping **brightness too bright**
- Keeping **apps running in the background**
- **Watching videos at high resolutions**
- **Performing resource intensive tasks a lot** - such as gaming, especially gaming with high settings
- Of course these are known factors and managing them should be your first step for a longer lasting battery. Now let's get into more detailed parts.
## Major Suggestion - Install A Custom ROM (Optional)
- First of all, I definitely suggest you to install a **custom ROM** because stock ROMs are full of **bloatware (unwanted apps)** and custom ROMs are more **lightweight**. The ROMs I can suggest are **LineageOS** and **CrDroid**.
- If you want to keep using your current ROM, you can skip to [the next step](https://github.com/cutiepenguins/Android-Longer-Battery-Life-Guide/blob/main/README.md#reduce-the-screen-resolution).
- Assuming you installed one of these ROMs or any other **Vanilla ROM**, I am continuing with my next suggestion after installing a Vanilla ROM: **MicroG**
### MicroG
- MicroG is an **open source re-implementation of Google services and libraries** that respects your privacy and consumes **way less CPU and other resources** compared to **Google services and libraries** which granted almost twice better battery life on my Xiaomi Redmi Note 8. All you have to do is **installing .apk files from the** [website](https://microg.org/download.html). It is so easy! Also, **Huawei** devices can use MicroG! For further information, you can follow my [MicroG Guide](https://github.com/cutiepenguins/MicroG-Guide).
## Reduce The Screen Resolution
- Reducing screen resolution **doesn't** help with battery life **drastically** but it surely helps. However, it **drastically improves performance** since your CPU and GPU work under fewer loads. So, it's good both ways. 
  - If your manufacturer lets you reduce **screen resolution**, choose the reduced screen resolution. If not, you can still do it using **ADB** but you need **a computer** for it.
### ADB Method - Non-Rooted
- You can install, set up and connect your phone to ADB [following this guide](https://www.xda-developers.com/install-adb-windows-macos-linux/)
  -  After connecting, google your phone model and check its native resolution. For my case, my phone **Xiaomi Redmi Note 8's** native resolution is `1080x2340` which makes it **1080p**, so I'll reduce to **720p** to balance quality and battery life.
  - After making the decision about what pixel to reduce the resolution to, execute the command below to change the screen resolution:
      - `adb shell wm size [resolution]` - for **Xiaomi Redmi Note 8**, `720x1565` is an ideal value for resolution. You can experiment the values to make it fit your screen.
    - After reducing resolution, you can notice that the items on your screen now look way bigger. So, we should change **DPI (dots per inch)** to balance it executing the command below:
      - `adb shell wm density [DPI value]` - for **Xiaomi Redmi Note 8**, `270` is an ideal value for DPI. You can experiment the values for your screen.
### Terminal Method - Rooted
- If ADB method didn't work for your phone, **root your phone** first and install [Termux](https://f-droid.org/tr/packages/com.termux/). After launching Termux, execute the commands below one by one.
  - `su` - during this command, you will be asked to grant **Shell** root permissions in your phone. You should grant the permission.
  - `wm size [resolution]`
  - `wm density [DPI value]`
## Other Suggestions
- **Using battery saver mode** is a cliche but it helps. Battery saver modes of **Samsung** phones can restrict CPU and background processes while battery saver modes of **other manufacturers** generally only restrict background processes and not CPU. If you'd like to manually restrict your CPU, you can do it using a **kernel manager** but it requires a **rooted phone**. To restrict your CPU (and GPU as well if you'd like to maximize battery life), follow the steps below:
  - First, install a kernel manager. My suggestion is [SmartPack Kernel Manager](https://f-droid.org/tr/packages/com.smartpack.kernelmanager/). Simply open the app, grant **root/superuser permissions** and choose the lowest values for your CPU and GPU (you don't have to choose the lowest values if you don't want to maximize battery life since you might also need smooth performance). Make sure to enable `Apply on boot` options for both sections.
- **The last** important suggestion is checking your **battery health** and if it's lower than 80%, **replacing the battery**. You can see your battery health installing `AccuBattery` and charging your phone from **14% (or lower)** to **100%**.
- Other suggestions I can make are basic things like **using wallpapers with darker colors, limiting battery usage for apps (app battery optimizations), using web versions of some apps you use by adding the websites to home screen as a shortcut and avoiding [factors that cause your battery to drain faster](https://github.com/cutiepenguins/Android-Longer-Battery-Life-Guide/blob/main/README.md#factors-that-cause-your-battery-to-drain-faster) etc.**
- Also, keeping your battery level between **20% and 80%** is very important since it is scientifically proved that Li-Ion batteries work the most efficient when battery levels are kept between 20% and 80%. It also helps your battery health to not reduce.
## Conclusion
This guide was about how to get a longer battery life on your Android device. I hope it has been useful for you. Have a nice day! 🐧
