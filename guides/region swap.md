# How to do a region swap
## __WARNING : This is for swiching OOS regions, not going from ColorOS to OxygenOS, if you want to switch from COS to OOS, please read the [COS2OOS.md](./COS2OOS.md) guide__
## __WARNING 2 : I am not responsible if something goes wrong__


## Requirements
- An OxygenOS OnePlus
- An internet connection on your phone
- Latest version of your actual region needs to be the same as the latest version of the region you want to switch
- OxygenUpdater installed on your phone (the app is now called OS updater)


## The actual guide
### 0. Preparing
Your device needs to have the local install option under software update, it should look like this

![](../assets/screenshots/local_install.jpg)

To enable Local installation, you need to enable developper options. Here are the steps to enable developpper options :
- Go to settings -> About device -> Version
- Click 7 times on "version number"
- Enter your pin
- You should now be a developper

Now that local installation is enabled, we can start downloading

### 1. Downloading the ROM
- Open OS Updater
- Go to settings -> update method
- Select stable(full) ![](../assets/screenshots/downloading.jpg)
- Go back to the main tab (the update tab) and click "Download update"
- (_reccomended_) Rename the update file to something like "old.zip"
- Go back to OS Updater's settings tab -> Device and pick the region you want to switch to
- "Update method" might switch to incremental again, so switch it back to "stable(full)"
- (_reccomended_) Rename the update file to something like "new.zip"

## 2. Swapping regions
- Go to system settings -> System & update -> software update -> click on 3 dots -> local install -> select old.zip __AND DON'T CLICK INSTALL__
- While not closing this app, go remove old.zip and rename new.zip to old.zip
- Go back to the update page and click install
- Wait for the phone to install the update, when finished, you should have swapped the update with other regions, this will also swap OTAs

## 3. Checking if it worked
- Go to Settings -> About device -> version

The first characters of the version number and the hardware version should have changed, it's the device model, here are the names for each region

|Region|Hardware name       |
|------|--------------------|
|US    |CPH2749             |
|EU    |CPH2747EEU / CPH2747|
|GLO   |CPH2747             |
|IN    |CPH2745             |