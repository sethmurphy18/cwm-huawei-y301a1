# cwm-huawei-y301a1
This is the release of Clockworkmod for the Huawei Valiant. While you are more
than welcome to flash this to your device, there are a few things to note:

1. First and foremost, this WILL void your warranty, so if you have any issues
    with your device after this, they are longer covered by Huawei or MetroPCS.
2. Secondly, rooting your device and/or flashing a custom recovery is directly
    against MetroPCS's (and most carriers') Terms of Use. If Metro catches you
    with either of these, they will suspend your account.
3. Thirdly, I am in no way, share or form responsible for what you do to your
    device. If you are not okay with this, then do NOT flash this recovery.
4. Fourth and finally, this process requires that your device's bootloader is
    unlocked. If you do not know how to do this, then refer to the thread I will
    be creating later.

**Proceed if and only if you agree to ALL of those terms**


## Credits
* Totempoke for starting the project, I would have never decided to start it if
    I hadn't seen that he was stalled
* jonhaney from UnleashedPrepaids for analyzing the partitions and giving
    partition map for this phone
* KainXS for giving me the solution to the "dancing" screen issue

## Downloads
The files for this device are hosted on my Github. The more recent download can
be retrieved from the link below. If you want an older release, then you need to
go to the
[Releases Page](https://github.com/Eagerestwolf/cwm-huawei-y301a1/releases).

Download Link:


## Installation Instructions
1. Download the file listed above
2. Install the Android SDK on your PC. For more information on doing so, Google
    it.
3. On your phone, open the settings app, swipe to the left so you are on the all
    tab, and scroll to the bottom. You should see an option that says Fast Boot.
    Make sure that option is turned off.
4. Turn off the device.
5. Pull the battery for 10 seconds (annoying, but necessary)
6. Place the battery back in your phone, and press and hold POWER + VOLDOWN for
    10 seconds, when you release the buttons, your phone should stay at the
    Huawei Logo if you did everything correctly

    **If your phone booted normally, just repeat steps 4 - 6**

7. Open a terminal (Linux and Mac) or Command Prompt and change to the
    directory you downloaded the file to.
8. Next type
    ```bash
      fastboot devices
    ```

    You should see a line that says something like
      ```bash
        34230cc2        fastboot
      ```

    **If you don't, check your drivers.**

9. Now type the following command and MAKE SURE YOU TYPE IT CORRECTLY, if you
    don't, this process can brick your device
    ```bash
      fastboot flash recovery {filename}
    ```

10. Once that completes, type the following command
    ```bash
      fastboot reboot
    ```

    As soon as your phone's screen goes blank press and hold the VOLUP button
    until your device boots into recovery.


**If your device opens Clockworkmod, good you are done. If it pulls up Huawei
recovery, then you have an issue, double check your commands and try again.**