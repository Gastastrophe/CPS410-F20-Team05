GTA V Self Driving Car w/ Motion
======================
Welcome to our GTA V self driving car experiment. This code trains a model to drive a car in GTA V by itself. The training set is a loop focusing on the inner-city southeast of the golf course. Note: the built-in GTA V driving AI *is not used* here. This model is trained based on the first person view from the driver's perspective, keyboard keypresses, and object avoidance from the YOLO model. For more information, check out http://www.waynenterprises.com/ai-ml

**Please do not attempt to run the self-driving car in GTA V online. It is a violation of Rockstar's EULA and your account may be banned!**

:star: Star us on GitHub — it helps increase this project's visibility!

## Developers
Name | Username | Contributions
---: | :---
Evan Miller | gastastrophe | Machine Learning Model & Most Development
Michael Dahl | dahle1mr | GTA V Scripting & UDP API
Josh Gutowski | josh-gutowski | Team Member
Allen Bourk | bourk1af | Team Member
Ian Kraft | ianfraft | Team Member
Dr. Alexander Redei | asmalex | Motion Simulation

Credit to __ for providing the intial source code. A lot of the pre-processing comes from their code.

## Installation Instructions

1. Make sure you have the following installed:
	### Requirements
	------------ | -------------
	 - [Grand Theft Auto] (https://store.steampowered.com/agecheck/app/271590/)
	 - [Anaconda] (http://www.anaconda.com/)
	 - [OpenIV] (http://openiv.com/)
	 - (Optional)[SimTools] (https://simtools.us/)

Note: simtools licenses cost money!

1. Navigate to your GTA V installation directory
1. Create a *mods* and *scripts* folder in the root GTA V installation directory
1. Copy the *update* folder to *mods* folder (so now it's in /mods/update)
1. Move all **.rpf** files from root folder to *mods* folder (Note: they are alphabetical. Be sure to copy *common.rpf* too)
1. Copy the following files from /_installME/GTA_Binaries_And_Scripts/binaries/ to root folder in GTA V
 - *dinput8.dll* (yes, overwrite)
 - *ScriptHookV.dll*
 - *ScriptHookVDotNet.asi*
 - *ScriptHookVDotNet2.dll*
 - *ScriptHookVDotNet3.dll*
1. Copy the *GTAScriptHookPlugin.dll* file from /_installME/GTA_Binaries_And_Scripts/scripts to the /scripts folder in GTA V
1. Open OpenIV
1. Open the ASI Manager window (under Tools -> ASI Manager)
1. Install ASI loader and OpenIV.asi (they sould turn green. Leave openCamera off, it will appear blue)
1. (Optional) install *GrandTheftAutoV_GamePlugin.zip* from /_installME/GTA_Binaries_And_Scripts/Simtools  by opening the simtools plugin manager and dragging the file into the installer.
1. Open Anaconda Navigator
1. Open the /Car/GTAV-Self-driving-car.ipynb
1. Run the first three lines (this may take a while as new packages are installed
1. Run the rest of the notebook
1. Enjoy!

	### Version Table
	If you still encounter issues, here are the verion table tested with this build:

	------------ | -------------
	Anaconda Navigator |  v1.10.0
	Jupyter Notebook | v6.1.4
	Python | v3.8.5 (Note: I created a seperate environment in Anaconda for this code)
	keras | v2.4.3
	Grand Theft Auto V | Steam Edition (Build ID 6337558)
	OpenIV | v4.0.1
	ScriptHook | v1.0.2245.0
	ScriptHookDotNet | v3.1.0
	SimTools | v2.4
	Windows 10  | v2004, Build 19041.867

	NOTE: additional libraries are installed in the iPython script itself Make sure your imports work before proceeding to execute further parts of the code (warnings are OK, but errors are not)


## Developer Task List
- [x] Collect at least 2 hours of driving data around the training area
- [x] Get GTA V telemetry data forwarded to UDP using openIV scripting
- [ ] Train a "good" model
- [ ] Test model on city driving
- [ ] Test model on country driving
- [ ] Test self-driving car with person in it