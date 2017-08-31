# se108
se108 datalogger support information page. This page includes In addition to technical information, device configuration utility script, support files and instructions that are necessary to run the se108 device configuration utility.

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-bh.jpg" width="400" height="400">


# Notes

- Logger must be running OS>28
- Logger should have a CF card
- This code supports EXO DCP-SOA v1

# Electrical Components

- Campbell Scientific CR1000 datalogger
- SDM-CD8S solid state relay driver
- SC105 I/O Serial adapter (x2)
- 7x Crydom Solid State Relays capabile of driving 3A sensors

# Directions

- If you edit any files in the se108.zip (e.g. se108main.cr1, se108settings.cr1 or control.xml) to change the programs behavior, you must zip into se108.zip prior to launching the device configuration utility (DCU)

- Prior to launching the DCU for the first time, you must edit the target of the shortcut .lnk file to reflect the correct path to devconfig.exe and the zip file that contains the crbasic scripts for the dev config utility to launch correctly. 

Here is an example of the target field:

DevConfig\devconfig.exe" --customise="se108.zip

# Supported sensors

- SeaBird (Satlantic) SUNA V1 & V2, polled and continuous operating modes
- Seabird (WetLabs) HydroCycle PO4
- XYLEM (YSI) EXO operated in SDI12 or Serial (if a SDM-SI01 is present in the can and attaced to the DCP SOA on SDM channel 1) 
- CSI OBS500/501
- Any generic SDI12 v1.3+ Sensor
- Any generic RS-232 sensor that outputs a datastream continuously 


# DCU Screenshots
## Splash screen

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-splash.jpg" width="900" height="600">

## Configuration
### System Tab

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config.png" width="800" height="600">

### Port 2 Tab (EXO)

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-port2-exo2.jpg" width="800" height="400">

### Port 7 Tab (OBS501)

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-port7.png" width="800" height="400">
