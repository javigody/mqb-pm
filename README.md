# MQB-stats

This is a performance monitor, based on Martoreto's aa-stats.
It's made specifically for use with the Volkswagen/Skoda/Seat/Audi MIB2 infotainment units, but it might also work on others, as long as they have Android Auto support.

# Screenshots:
Some screenshots of the app:

Golf GTI theme with high visibility-dials.
![VW theme](https://i.imgur.com/dTG3oBq.png)

Seat theme with high min/max turned on.
![Seat theme](https://i.imgur.com/g8J8whV.png)

Skoda ONEapp theme with high min/max turned on.
![Skoda ONE theme](https://i.imgur.com/OfO3jpb.png)

Stopwatch/laptimer mode in VW GTI theme:
![VW stopwatch](https://i.imgur.com/0jm310L.png)


# Installation instructions:

Download the latest release here: https://github.com/jilleb/mqb-pm/releases

- Make sure Android Auto is in developer mode: Open Android Auto (while not connected to the car), go to About. Tap the "About Android Auto" header 10 times untill you see a toast message saying you're a developer. From the right top corner select developer options, scroll down and make sure you check "Unknown sources". This will allow programs from non-Playstore apps to be run on Android Auto. See a picture guide how to enable Developer mode here: https://www.howtogeek.com/271132/how-to-enable-developer-settings-on-android-auto/
- Install aauto-vex-vag.apk (open source service by Martoreto: https://github.com/martoreto/aauto-vex-vag/) , the service that supplies exlap-communication between Android and the head-unit. Note: this app will not show up in your launcher.
- Install the Performance Monitor apk
- Open the Performance Monitor settings, grant all the rights it's requesting. If you don't do this, the app will NOT work.
- Hook your phone to your car's USB, start Android Auto on your unit.
- You can find the Performance Monitor in the menu on the lower right in Android Auto, the one with the dashboard clock on it.


# Known issues
- App slowing down over time, and restarting. I haven't pinned this down completely yet. 

- Black screen of death: On some cars it doesn't work for unknown reasons. This will not kill your car or headunit. Send me a logcat. 
On Huawei and Honor devices this is a common problem, caused by a bug in their ROMs. A workaround to get OEM apps working again is to clear the Android Auto apk cache when this happens. (thanks to nerone-github for the information.)

- No data
If you don't see any data in the app, it can have various reasons:
Some cars don't provide data to the headunit. 
Some MIB2 firmware versions don't provide data to the exlap channel.
Not all data elements are available on all cars. If one element doesn't provide data, try an other one.
Most cars do not report oil and coolant temperatures below 50.

- Android Auto crashing after some time
It looks like the app is crashing Android Auto when it's not getting any data. This doesn't happen on all cars.

- Appkillers/memory managers kill the service
Put the Vag extensions for Android Auto app in the whitelist of your memory manager.

- Phone locking causes data to stop
Some phones kill the datafeed as soon as the screen is locked. This doesn't happen with all phones.

# What to do when it's not working?
- Try choosing a different type of data in the settings app. Not all cars have all data available. Reconnect to the car after you've done this.
- Check if you have applied all rights. Did you open the settings app after installing? Did you install both APK's?
- Unplug/replug your phone and try again

# Currently not working firmware versions:
**MIB2:**
- VW 0245
- VW 0343
- VW 0613
- VW 0617
- VW 0755
- VW 1156

**MIB2Std**
- Seat 0351
- Seat 0359


**RCD330:**
- VW 5406

# Currently confirmed working firmware versions:
**MIB2Std**
- Seat 0462
- Skoda 0468

**MIB2:**
- VW 0814
- VW 1187
- Seat 1146
- Skoda 0468 

**MIB2.5**
- Seat 1162

# Mixed results:
**MIB2:**
The following firmwares are working, but for some users they don't.
- VW 0751
- VW 0753