# THE BEAT COP

![](https://i.imgur.com/d0R6KNK.gif)

*THE BEAT COP* (TBC) is a free drum machine made in Pure Data Vanilla 0.48 and released under the GNU GPLv3 license.                                            

_________

# Install instructions for THE BEAT COP, March 24, 2018

Pure Data Vanilla version 0.48 (or higher) and the flatGUI extension are required for THE BEAT COP.

Platform specific instructions below.

_________

## Windows / Mac OS
**Step 1: Install PD Vanilla version 0.48 or higher**

Please install the 32bit version, since FlatGUI is only available as a 32bit extension.

http://puredata.info/downloads/pure-data 



**Step 2: Install the flatGUI external**

Once pd is installed, launch pd.exe, the console window should appear.

On the menubar select "Help" --> "Find externals"

In the window that opens, search for "flatgui"

Three or more items should appear in the list below the search bar. Select the one that isn't greyed out. When you click on the filename it should begin to download then extract the external.

When it has finished extracting, it will show 100% and say that it was successful. You might have to scroll down the text box.



**Step 3: Open THE BEAT COP in pd**

Open the file "basic-patch.pd" in Pure Data by selecting "File" --> "Open" from the pd menu bar, or by double clicking on it in file explorer.

If you want to use THE BEAT COP in other pd patches aside from the test patches I've included, you can create a new patch in THE BEAT COP release folder, or declare the path to the "tbc" folder in your patch.

To declare the path to the tbc folder in your pd patch, simply create a new object [declare -path C:/full/path/to/tbc] and then create a new object [THE_BEAT_COP] and THE BEAT COP should appear.

_________

## Linux

**Step 1: Download lastest source code for PD Vanilla**

http://puredata.info/downloads/pure-data 



**Step 2: Install PD Vanilla**

Use the following commands

tar -xvzf pd-filename.tar.gz

cd pd-filepath-on-your-system



There are instructions in the pd folder on how to compile it, but here are the commands you'll need



./autogen.sh

./configure

make

sudo make install



**Step 3: Install the flatGUI external**

Once pd is installed, launch pd by typing "pd" in a terminal. The console window should appear.

On the menubar select "Help" --> "Find externals"

In the window that opens, search for "flatgui"

Three or more items should appear in the list below the search bar. Select the tar file (it's the one that isn't greyed out). When you click on the filename it should begin to download then extract the external.

When it has finished extracting, it will show 100% and say that it was successful. (You might have to scroll down the text box to see this.)



**Step 4: Open THE BEAT COP in pd**

Open the file "basic-test.pd" in Pure Data by double clicking on it in file explorer, or by selecting "File" --> "Open" from the pd menu bar.



If you want to use THE BEAT COP in other pd patches aside from the test patches I've included, you can create a new patch in THE BEAT COP release folder, or declare the path to the "tbc" folder.

To declare the path to the tbc folder in your new pd patch, simply create a new object [declare -path ~/full/path/to/tbc] then you can simply create a new object [THE_BEAT_COP] and THE BEAT COP should appear.

**WARNINGS:**

Raspberry Pi 3 can run THE BEAT COP, but currently THE BEAT COP reads / writes to disk frequently to save patterns, samples, and settings.

  * You may quickly wear down the SD card on your pi! USE AT YOUR OWN RISK!

  * To see TBC reading / writing to disk, you can enable debug logs within the file "/tbc/tbc-state-saves/tbc-#/settings.txt". Close and re-open THE BEAT COP for this to take effect.    



There is (at the time of this writing) no build for the flatgui extension on ARM devices.

  * THE BEAT COP only uses the "knob" object from this library, but thankfully the "knob" object is interchangable with the "vslider" and "hslider" object.

  * To open THE BEAT COP on Raspberry Pi, you must open the "THE_BEAT_COP.pd" file in a text editor, find and replace all the word "knob" with "vslider", then save the file and exit.

  * If you open up THE BEAT COP and there are no knobs, double check this!



In my experience "apt-get install puredata" downloads vanilla version 0.46.7-3, which is outdated and will not work for THE BEAT COP. (Version 0.48 has some list processing functions that I use.)

________

# That's cool, but how do I use it?

THE BEAT COP includes a comprehensive, interactive help file THE_BEAT_COP-help.pd

You can also check out the demo videos that I've made on my youtube channel, [MegalonPureData](https://www.youtube.com/channel/UCRTrsMZ6f6HXOpgBpMisBiQ/videos)

I hope to make a tutorial series soon.
