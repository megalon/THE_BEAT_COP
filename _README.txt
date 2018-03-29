
.=================================================================.
|                                                                 |
|    What is The Beat Cop?                                        |
|        The Beat Cop (TBC) is a free drum machine made in        |
|            Pure Data Vanilla 0.48                               |
|        The Beat Cop is released under the GNU GPLv3 license.    |
|        THIS SOFTWARE IS PROVIDED WITHOUT WARRANTY!              |
|                                                                 |
|    For more information visit:                                  |
|        http://www.thebeatcop.club                               |
|        https://github.com/megalon                               |
|                                                                 |
|    Author:                                                      |
|        Claude Barker (aka megalon)                              |
|        tbc.claude@gmail.com                                     |
|                                                                 |
'================================================================='




Install instructions for The Beat Cop, March 24, 2018
-------------------------------------------------------------------

Pure Data Vanilla version 0.48 (or higher) and the flatGUI extension are required for The Beat Cop.

Platform specific instructions below.


Windows:    
    Step 1: Install PD Vanilla version 0.48 or higher
        http://puredata.info/downloads/pure-data 

    Step 2: Install the flatGUI external
        Once pd is installed, launch pd.exe, the console window should appear.
        On the menubar select "Help" --> "Find externals"
        In the window that opens, search for "flatgui"
        Three or more items should appear in the list below the search bar. Select the Windows zip file (it's the one that isn't greyed out). When you click on the filename it should begin to download then extract the external.
        When it has finished extracting, it will show 100% and say that it was successful. You might have to scroll down the text box.

    Step 3: Open The Beat Cop in pd
        Open the file "basic-patch.pd" in Pure Data by selecting "File" --> "Open" from the pd menu bar, or by double clicking on it in file explorer.

    If you want to use The Beat Cop in other pd patches aside from the test patches I've included, you can create a new patch in The Beat Cop release folder, or declare the path to the "tbc" folder in your patch.
    To declare the path to the tbc folder in your pd patch, simply create a new object [declare -path C:/full/path/to/tbc] and then create a new object [THE_BEAT_COP] and The Beat Cop should appear.


Linux:
    WARNINGS: 
        1. Raspberry Pi 3 can run The Beat Cop, but currently The Beat Cop reads / writes to disk frequently to save patterns, samples, and settings.
		You may quickly wear down the SD card on your pi! USE AT YOUR OWN RISK!
		To see TBC reading / writing to disk, you can enable debug logs within the file "/tbc/tbc-state-saves/tbc-#/settings.txt". Close and re-open The Beat Cop for this to take effect.    
        
        2. There is (at the time of this writing) no build for the flatgui extension on ARM devices.
		The Beat Cop only uses the "knob" object from this library, but thankfully the "knob" object is interchangable with the "vslider" and "hslider" object.
		To open The Beat Cop on Raspberry Pi, you must open the "THE_BEAT_COP.pd" file in a text editor, find and replace all the word "knob" with "vslider", then save the file and exit.
		If you open up The Beat Cop and there are no knobs, double check this!
        
        3. In my experience "apt-get install puredata" downloads vanilla version 0.46.7-3, which is outdated and will not work for The Beat Cop. (Version 0.48 has some list processing functions that I use.)
    
    Step 1: Download lastest source code for PD Vanilla
        http://puredata.info/downloads/pure-data 

    Step 2: Install PD Vanilla
        Use the following commands
        tar -xvzf pd-filename.tar.gz
        cd pd-filepath-on-your-system

    There are instructions in the pd folder on how to compile it, but here are the commands you'll need

        ./autogen.sh
        ./configure
        make
        sudo make install

    Step 3: Install the flatGUI external
        Once pd is installed, launch pd by typing "pd" in a terminal. The console window should appear.
        On the menubar select "Help" --> "Find externals"
        In the window that opens, search for "flatgui"
        Three or more items should appear in the list below the search bar. Select the tar file (it's the one that isn't greyed out). When you click on the filename it should begin to download then extract the external.
        When it has finished extracting, it will show 100% and say that it was successful. (You might have to scroll down the text box to see this.)

    Step 4: Open The Beat Cop in pd
        Open the file "basic-test.pd" in Pure Data by double clicking on it in file explorer, or by selecting "File" --> "Open" from the pd menu bar.

    If you want to use The Beat Cop in other pd patches aside from the test patches I've included, you can create a new patch in The Beat Cop release folder, or declare the path to the "tbc" folder.
    To declare the path to the tbc folder in your new pd patch, simply create a new object [declare -path ~/full/path/to/tbc] then you can simply create a new object [THE_BEAT_COP] and The Beat Cop should appear.


Mac OS:
    I don't have access to a Mac in order to test The Beat Cop, but these instructions should work out. I will update this readme if changes need to be made.

    Step 1: Install PD Vanilla version 0.48 or higher
        http://puredata.info/downloads/pure-data 

    Step 3: Install the flatGUI external
        Once pd is installed, launch the pd application. The console window should appear.
        On the menubar select "Help" --> "Find externals"
        In the window that opens, search for "flatgui"
        Three or more items should appear in the list below the search bar. Select the option that isn't greyed out. When you click on the filename it should begin to download then extract the external.
        When it has finished extracting, it will show 100% and say that it was successful. (You might have to scroll down the text box to see this.)

    Step 3: Open The Beat Cop in pd
        Open the file "basic-test.pd" in Pure Data by double clicking on it in file explorer, or by selecting "File" --> "Open" from the pd menu bar.

    If you want to use The Beat Cop in other pd patches aside from the test patches I've included, you can create a new patch in The Beat Cop release folder, or declare the path to the "tbc" folder.
    To declare the path to the tbc folder in your new pd patch, simply create a new object [declare -path ~/full/path/to/tbc] then you can simply create a new object [THE_BEAT_COP] and The Beat Cop should appear.


