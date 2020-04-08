# Getting Started with FRC Programming

[return to master guide](https://github.com/TASRobotics/master-guide/blob/master/README.md)

This is a quick guide to get setup to start programming. 

## Installing Programs

You need to install 3 different things in order. The first is FRC Game Tools. This program includes Driver Station, which allows you to control the robot. Next is CTRE Toolsuite, which is the library for the motor controllers we usually use (Talon SRX). Finally, VS Code is the program that is used to write the robot code.

## Note

If you don't have fast wifi, you can come to the sessions and ask for USBs preloaded with the installers.

### FRC Game Tools

1. Download FRC Game Tools from [here](https://www.ni.com/en-us/support/downloads/drivers/download.frc-game-tools.html)
    - Needs login with NI Account. Make one if you don’t have one 
2. Unzip the whole folder and run setup.exe
3. Click Next for everything. There is no need to fill in any information
4. You can just skip NI Licensing

### CTRE

1. Click [here](http://www.ctr-electronics.com/hro.html#product_tabs_technical_resources)
2. Download the newest version of “CTRE Phoenix Framework Installer” (zip file) 
3. Unzip and run the program

### WPILib Suite

1. Click [here](https://github.com/wpilibsuite/allwpilib/releases) and download the Windows 64 installer
2. Select all or current user, doesn’t matter
3. Make sure all checkboxes are checked. You probably have to select/download VS Code
4. Click “Execute Install” 

## Roborio

Roborio (the brain of the robot) needs to be configured correctly for it to work for this year. Here are the steps.

1. Updating the firmware and imaging the Roborio: https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/imaging-your-roborio.html
    - Note: If the shortcut is not on the desktop, it is located here: 
    C:\Program Files (x86)\National Instruments\LabVIEW 2019\project\roboRIO Tool
2. Run Phoenix Library/Diagnostic
    - Open Phoenix Tuner and connect to the robot
    - Click "Run Temporary Diagnostic Server"

## Configuring Radio

These are the steps for configuring the radio. Complete instructions [here](https://docs.wpilib.org/en/latest/docs/getting-started/getting-started-frc-control-system/radio-programming.html).

1. Install radio configuration utility from the instructions page
2. Choose radio type
3. Load firmware
4. Type in team number, then configure.

## Updating Firmwares

The PDP, PCM, Roborio, and TalonSRX may need firmware updates.

1. Connect to roborio and open up Phoenix Tuner
2. Navigate to CAN Devices tab.
3. Under Field-Upgrade Device Firmware, select the CRF and click Update Device

## Driver Station

The driver station is the program used to control the Robot. You can get familiar with the layout of the program [here](https://docs.wpilib.org/en/latest/docs/software/driverstation/driver-station.html). However, there are some settings that should be set to help you debug and connect to the robot.

1. Set the team number at the third tab (gear tab).
    - Change this whenever you work on a different robot.
    - If this is not set properly, you won't be able to connect to the robot!!!
2. At the same tab, change the dashboard type to Shuffleboard.

After finishing this guide, you should go on to the [First Program guide](First_Program.md).
