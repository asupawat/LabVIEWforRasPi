# LabVIEWforRasPi

**IMPORTANTE NOTICE**
The Raspberri Pi Compatible Compiler for LabVIEW by TSXperts has been made a free product as of 01/01/2020. Full LabVIEW source code is available in this repository. To launch the main compiler application, open the RasPi Source.lvproj LabVIEW project, then launch the Raspberry Pi Compatible Compiler for LabVIEW.vi located inside RasPi Compiler/Compile and Download App virtual directory in the LabVIEW project. Make sure to follow the instructions below to setup your environment. This product is not supported and you should use it at your own risk. You are free to make any changes you see fit in the source code. You can use the source code commercially, provided you cite the source code was made by TSXperts LLC and that TSXPerts LLC shall be idenmified of any potential liabilities according to the License Agreement file included in this repository.

This repo includes some important documents with instructions on how to setup your environment to use the Raspberry Pi Compatible Compiler for LabVIEW to program your Raspberry Pis in LabVIEW. It also contains the two VIPM installer packages, one for the Home edition and the other for the Standard edition. The Home edition is applicable for Home not-for-profit projects and Academic use, while the Standard edition is suited for commercial applications. Make sure to read through the License Agreement document for all licensind details. The VIP file that is most applicable to you is to be downloaded and installed on the development machine in order to compile and download LabVIEW code to your Raspberry Pi. Dowload the Raspberry Pi image from this [Google Drive link](https://drive.google.com/drive/folders/0B7DdMz7ZefcwMjlzVlM3OGxJVWs?usp=sharing). 

Make sure to burn a SD Card with the image dowloaded from the link above, even though the official Raspberry Pi PIXEL Operating System is maintained untouched in that image, all the necessary support packages have been installed and properly configured so your Raspberry Pi is ready to receive compiled LabVIEW code. We will not provide support if you decide to update your Pi's operating system via sudo update. We will do our best to release updated images as the Raspberry Pi organization updates the released OS.

**A NOTE TO LABVIEW USERS: 
IF RUNNING LV 2016, MAKE SURE YOU ARE USING THE LATEST VERSION OF VI PACKAGE MANAGER (2016 SP1), OTHERWISE THE COMPILER WILL NOT PROPERLY INSTALL ON YOUR LABVIEW 2016**

**LV 2017 64-BIT NOT SUPPORTED. THE 32-BIT VERSION OF LV 2017 IS SUPPORTED**

**Raspberry Pi 3B+ and 4B not supported.**

Make sure you go through the full Product User Manual made available on this repository's Wiki page, PRIOR TO START DOWNLOADING AND INSTALLING FILES.

Support inquiries can be made at our support forum below (recommended) or through the following e-mail address: lvforpisupport@tsxperts.com.
https://www.tsxperts.com/forums/forum/raspberrypiforlabviewforum/raspberry-pi-compatible-compiler-for-labview-support-forum/

The complete product user manual can be found at this repository's Wiki page: https://github.com/labviewforRaspi/LabVIEWforRasPi/wiki

Make sure you start from the Wiki page and follow ALL of its instructions on how to setup your environment as well as places to get more information.

**ACTIVATION PROCEDURE**

Once you have purchase a license, the activation of the Compiler needs to happen from within LabVIEW. **Do not attempt to activate the compiler from the webpage you used to purchase the license.** From within LabVIEW, go to the Help Menu and select Activate Addon. Then enter your credentials (License ID and Activation Password) on the popup screen.
 
Make sure you have downloaded and installed the VIP package file that matches your purchased license type (there are two different VIP files, one for the Home edition and one for the Standard edition). **The Standaed VIP file won't activate with a Home license and vice versa.**

Some common mistakes during activation to double check:

1) Activation needs to happen from within LabVIEW. Open LabVIEW in Administration mode (right click the LabVIEW icon and select Run as Administrator), got to Help->Activate Add On... option. Select the compiler and click activate. Enter your license ID and password

2) The compiler has two vip VI Package Manager files available for download. Make sure you download and install the one matching the purchased license edition. If you purchased the Home license, make sure to download the vip file that has a Home in the name. If you purchased the Standard license, make sure to download and install the vip file that DOES NOT have Home in the name. If you inadvertently installed the wrong vip file, uninstall it from VI Package Manager, download the correct vip file and attempt the installation again

3) When downloading the vip file from the github repo, DO NOT right click at the file and select Save As. This will corrupt the download and the compiler will not install properly. Make sure to click at the Download button on github to download the file


##Release Notes for VIP Packages##

**Version 1.0.0.13

Fixed bug with Check for Updates functionality if activated from Compiler Menu

**Version 1.0.0.12

General improvements on error handling

**Version 1.0.0.11

Runtime [V1.0.0.827]

Fixed bug with hidden toolbars

Fixed bug when re-running an aborted Vi

Fixes:

- Issue with shift register not properly functioning when branched in the block diagram


**Version 1.0.0.10**

Runtime [V1.0.0.822]

Add support for Scale By Power Of 2

Fix bug with disabled inputs on Index Array for ND arrays

Fix bug with default values on Array Subset

Fix bug with abort handling inside of nested SubVIs

Addition:

- Data manipulation subpalette


**Version 1.0.0.9**

Runtime [V1.0.0.805]

- Add local configuration file (vi_name.cfg) to control window size and position.  Select 'Save' from the File menu to save the current window size and position to this file.

- Improve responsiveness to aborts.  File > Quit will abort running VIs

- Fixed bug with swapped inputs on Replace Array Subset

- Add numeric conversion functions to the palettes.

- Add additional Date/Time functions.  Format Strings follow the Python convention described in the documentation for the datetime module.  This is similar to the LabVIEW format but there are a few differences.

- Cosmetic changes to increase the font size in Spinboxes and Numeric entry controls

**Version 1.0.0.8**

- Added Compound Arithmetic

- Added support for non-english versions of LabVIEW

**Version 1.0.0.7**

Runtime[V1.0.0.773]

- Fixed bug with GPIO Event Detection

Runtime [V1.0.0.768]

- Fixed bug in VISA error handling

- Fixed bug when wires connected to a loop termination terminal are branched

Runtime [V1.0.0.764]

- Fixed bug with carriage returns in Control Labels (i.e. Enable Termination Char in Configure Serial Port)

- Add support for Compound Arithmetic

- Fixed bug with single element Build Array and Bundle nodes

- Added Support for Compound Arithmetic

- Removed need for development machine to be connected to Internet for automated version check

- Added automated version update checking as part of the GUI

**Version 1.0.0.6**

Fixes: 

[Runtime V1.0.0.749]

Fixed bug to allow Waveform Graph to accept a 1D array

Cosmetic fixes for Graphs and Charts

[Runtime V1.0.0.751]

Fixed bug with Progress Bar values

Fixed bug with Match Pattern requiring offset to be wired

[Runtime V1.0.0.755]

Fixed bug with SubVI input/output ordering with terminals not connected to ConPane

Fixed bug with return value of Console Print function

**Version 1.0.0.5**

Fixes: 

- Not allowing compilation if Runtime revision deployed to the Pi matches released Runtime version

**Version  1.0.0.4**

Updates: 

- Auto detection and notification of the user if newer versions of Runtime and/or Library files are available for upgrade

**Version 1.0.0.3**

Internal Build

**Version  1.0.0.2**

Bug Fixes: 

- Serial Config holding compilation

- Waveform Graphs generating runtime error on the Pi. For this fix to take effect, please Update the Runtime on the Compiler->Update runtime menu item in the Raspberry Pi Compatible Compiler for LabVIEW GUI. Follow the instructions on how to do that as described by [this document](https://github.com/labviewforRaspi/LabVIEWforRasPi/blob/master/Raspberry%20Pi%20Compatible%20Compiler%20for%20LabVIEW%20GUI%20-%20Operating%20Manual.pdf)








