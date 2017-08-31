# se108
Welcome to the se108 datalogger software repository. This repo houses technical information, device configuration utility (DCU) scripts, support files and instructions that are necessary to program the se108 and operate the DCU. The se108 has a power input port, a telemetry port (Port 1) and 7 sensor ports (Ports 2-8). The Campbell Scientific SE108 is submerisble CR1000 datalogger equipped with power switching and communication peripherals.The se108 DCU is used to program the se108's input ports and sampling schedule.

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-bh.jpg" width="445" height="440">

# Notes

- Logger must be running OS>28
- Logger should have a CF card
- This code supports EXO DCP-SOA v1

# Electrical Components

- Campbell Scientific CR1000 datalogger
- SDM-CD8S solid state relay driver
- SC105 I/O Serial adapter (x2)
- 7x Crydom Solid State Relays capable of driving 3A sensors

# Directions

- If you edit any files in the se108.zip (e.g. se108main.cr1, se108settings.cr1 or control.xml) to change the programs behavior, you must zip into se108.zip prior to launching the device configuration utility (DCU)

- Prior to launching the DCU for the first time, you must edit the target of the shortcut .lnk file to reflect the correct path to devconfig.exe and the zip file that contains the crbasic scripts for the dev config utility to launch correctly. 

Here is an example of the target field:

DevConfig\devconfig.exe" --customise="se108.zip

# Supported sensors

- SeaBird (Satlantic) SUNA V1 & V2, polled and continuous operating modes
- Seabird (WetLabs) HydroCycle PO4
- XYLEM (YSI) EXO operated in SDI12 or Serial (if a SDM-SI01 is present, set to SDM channel 1 and wired to the  DCP SOA RS232 Tx&RX channels) 
- Any generic SDI12 v1.3+ Sensor (such as the CSI OBS500/501)
- Any generic RS-232 sensor that outputs a datastream continuously 

# DCU Screenshots

## Splash screen

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-splash.jpg" width="1024" height="576">

## Configuration

### System Tab

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config.png" width="575" height="515">

### Port 2 Tab (EXO)

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-port2-exo2.jpg" width="1024" height="576">

### Port 7 Tab (SDI-12)

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-config-port7.png" width="850" height="425">
