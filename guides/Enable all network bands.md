# Enabling all LTE/5G Bands on OnePlus 15
## Things to know
- This has been tested to work on other OnePlus phones and even Realme, even though I'm not reccomending to do that without knowledge
- This could also let you unlock network bands from other regions for non-chineese devices
- This guide __DOES NOT REQUIRE YOU TO HAVE ROOT ACCESS__
- __Don't screw around with the EFS, it contains critical data like IMEI, battery health and other things you don't want to loose__

## The guide
### 0. Requirements
- Your OnePlus 15 with ADB enabled
- A Windows PC
    - Linux won't work, i'm not even sure it would work in a virtual machine
- Qualcomm QPST and ADB installed
- Qualcomm USB driver found [here](https://www.mediafire.com/file/c59zj43e7d3x1pl/Necessary+Files.zip/file)


### 1. Booting your device in the correct mode and installing the drivers
- On your PC, in your terminal, run `adb devices` to be sure that ADB is working on your PC and enabled on your phone
    - If you don't see any device, check that ADB is enabled and that you have authorized your computer on your phone. Also check if your cable is able to transmit data
    - If you see your device, you can continue
- On your PC, in your terminal, run `adb reboot ftm`, this is a special mode that isn't really accessible apart from this command
- Still in your terminal, run `adb shell` and once you've entered the android shell, run `setprop sys.usb.config diag,diag_mdm,qdss,qdss_mdm,serial_cdev,dpl,rmnet,adb`, you should hear a windows device plug-in sound
- Go to device manager -> unknown devices, you should see multiple unknown devices, all these devices are your phone
    - If you don't, check that your cable is working correctly
- Right-click on the one with a correct name (should be "Oneplus 15) -> Update driver -> Browse my computer for drivers -> Let me pick from a list of available drivers on my computer -> Next -> Have Disk... -> Browse... -> _Select qcmdm.inf file from the qualcomm driver you downloaded earlier_ -> Qualcomm Incorporated -> Qualcomm HS-USB Android DIAG 9018 (this exact one, not another one)
    - If you get an update warning, just say that you don't care and still want to install the driver
- Now do the same with all the unknown devices with the same name (Here, Oneplus 15)

Now that your drivers are set up, we can start editing all the EFS stuff

### 2. Editing the EFS
- Open QPST Config
- On the top bar, press "Start Clients" -> EFS explorer -> _Select any device until you find one where there isn't an error when launching the explorer_