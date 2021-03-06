---
layout: device
title:  "Huawei P8 Lite 2017"
codename: prague
downloadfolder: prague
supportstatus: Current
maintainer: DarkJoker360
oem: Huawei
devicetree: https://github.com/TeamWin/android_device_huawei_prague
xdathread: "https://forum.xda-developers.com/p8lite/p8-lite-2017-development/recovery-twrp-huawei-p8-lite-2017-t4113153"
---

{% include disclaimer.html %}

{% include supportstatus.html %}
Note: Data cannot be decrypted in TWRP.

{% include appinstall.html %}

{% include download.html %}

{% include twrpinstall.html %}

<div class='page-heading' id='fastboot-install'>Fastboot Install Method (No Root Required):</div>
<a id='fastboot'></a>
<hr />
<p class="text"><a href="http://developer.android.com/sdk/index.html#linux-bundle-size">You will need the platform-tools from the Android SDK on your computer.</a> Find the Android command line tools section on the page linked and install the SDK tools package. From the SDK Manager, download only the platform-tools to get adb and fastboot binaries.</p>
<p class="text">Windows users will need proper drivers installed on their computer. You can try the <a href="https://forum.xda-developers.com/android/software-hacking/live-iso-adb-fastboot-driver-issues-t3526755" target=_blank>simple FWUL adb/fastboot ISO</a> or the <a href="http://www.xda-developers.com/universal-naked-driver-solves-your-adb-driver-problems-on-windows/">Naked ADB drivers</a> or the <a href="https://adb.clockworkmod.com/">Universal ADB drivers</a> if you don't already have a working driver installed</p>
<p class="text">On your device, go into Settings -> About and find the Build Number and tap on it 7 times to enable developer settings. Press back and go into Developer Options and enable USB debugging. From your computer, open a command prompt and type:</p>
<p class="code">adb reboot bootloader</p>
<p class="text">You should now be in fastboot mode.</p>
{% if page.fastbootunlock %}
<p class="text">Your device needs to be unlocked before it can flash custom images. To unlock your device type:</p>
<p class="code">{{ fastboot }} oem unlock</p>
{% endif %}
<p class="text">Download the correct image file and copy the file into the same folder as your adb and fastboot binaries. Rename the image to twrp.img and type:</p>
<p class="code">{{ fastboot }} flash recovery_ramdisk twrp.img</p>
<p class="code">{{ fastboot }} reboot</p>
<p class="text">Note many devices will replace your custom recovery automatically during first boot. To prevent this, use <a href="http://www.google.com">Google</a> to find the proper key combo to enter recovery. After typing <span class="code">{{ fastboot }} reboot</span>, hold the key combo and boot to TWRP. Once TWRP is booted, TWRP will patch the stock ROM to prevent the stock ROM from replacing TWRP. If you don't follow this step, you will have to repeat the install.</p>
