# Introduction

Welcome to the se108 datalogger software repository. This repository maintains technical information, device configuration utility (DCU) support files, datalogger scripts, and setup instructions that are necessary to operate the Campbell Scientific SE108. 

# What is the SE108 and how do I use it?
The SE108 is essenstially a submersible CR1000 datalogger equipped with power switching and communication peripherals. The se108 has a power input port, a telemetry port (Port 1) and seven sensor ports (Ports 2-8).
The DCU is a GUI that makes it easy to setup the se108's input ports, change its sampling schedule and operate the se108 on site.

## SE108 port information

<img src="https://github.com/OneGneissGuy/CSI-se108/blob/master/images/se108-bh.jpg" width="445" height="440">

### Bulkhead types by port 

Port | Port function and sensor support
------------ | -------------
Port 1 | MCBH-8-MP
Port 2 | MCBH-6-FS 
Port 3 | MCBH-8-FS
Port 4 | MCBH-5-FS
Port 5 | MCBH-4-FS
Port 6 | MCBH-6-FS
Port 7 | MCBH-3-FS
Port 8 | MCBH-8-FS

### Port function

Port | Port function and sensor support
------------ | -------------
Power In | 12 volt, 3 amp power input (fused at 10 amp)
Port 1 | RS-232 datalogger communications / SW12 output
Port 2 | Xylem EXO water quality sonde 
Port 3 | Generic RS-232 or SDI-12 serial sensor (Satlantic SUNA pin compatible)
Port 4 | Zebra-tech wiper
Port 5 | Generic RS-232 serial (WETLabs digital sensor pin compatible)
Port 6 | Generic analog input (Turner Designs C7 snesor pin compatible)
Port 7 | Generic SDI-12 sensor
Port 8 | Generic RS-232 or SDI-12 serial sensor (Satlantic SUNA pin compatible)

### Port pin mapping 

#### Port 1

Pin Number | Datalogger Pin | Pin Function
------------ | ------------- | -------------
1 | CR1000 G | Power Ground
2 | CR1000 RS232 Pin 2 | RS-232 RXD 
3 | CR1000 RS232 Pin 3 | RS-232 TXD 
4 | CR1000 RS232 Pin 4 | RS-232 DTR
5 | CR1000 RS232 Pin 5 | RS-232 Ground
6 | CR1000 RS232 Pin 6 | RS-232 DSR
7 | CR1000 RS232 Pin 7 | RS-232 RTS 
8 | CR1000 SW12 | Switched 12 Volts

#### Port 2
Pin Number| EXO DCP-SOA Pin
------------ | ------------- 
1 | N/C
2 | Red
3 | Black
4 | N/C
5 | Yellow
6 | White

#### Port 3
Pin Number | Pin | Pin Function
------------ | ------------- | -------------
1 | Relay 2 Pin 2 | Sensor Power In
2 | Power Ground | Sensor Power Ground
3 | Power Ground | Sensor Communication Ground
4 | CR1000 Port C7 | SDI-12
5 | CR1000 Com3-RX/Port C6 | RS232 TX
6 | CR1000 Com3-TX/Port C5 | RS232 RX
7 | CR1000 SE3 | Sensor analog signal +
8 | N/C | N/A

#### Port 4
Pin Number | Wiper Board Pin
------------ | -------------
1 | 1
2 | 2
3 | 3
4 | 4
5 | 5

#### Port 5
Pin Number | Sensor Pin | Pin Function
------------ | ------------- | -------------
1 | Power Ground | Sensor Power Ground
2 | Relay 4 Pin 2 | Sensor Power +
3 | SC105 (SDC7) TX | Sensor RS232 RX
4 | SC105 (SDC7) RX | Sensor RS232 TX

#### Port 6
Pin Number | Sensor Pin | Pin Function
------------ | ------------- | -------------
1 | Relay 5 Pin 2 | Sensor Power +
2 | Power Ground | Sensor Power Ground
3 | CR1000 SE1 | Sensor Signal +
4 | CR1000 Analog Ground | Sensor Signal - 
5 | CR1000 G | 10X gain
6 | N/C | 100X gain 


#### Port 7
Pin Number | Sensor Pin | Pin Function
------------ | ------------- | -------------
1 | CR1000 C7 | SDI-12
2 | Power Ground | Sensor Power Ground
3 | Relay 6 Pin 2 | Sensor Power +

#### Port 8
Pin Number | Sensor Pin | Pin Function
------------ | ------------- | -------------
1 | Relay 6 Pin 7 | Sensor Power +
2 | Power Ground | Sensor Power Ground
3 | Power Ground | Sensor Communication Ground
4 | N/C | N/A
5 | SC105 (SDC8) RX | Sensor RS232 TX
6 | SC105 (SDC8) TX | Sensor RS232 RX
7 | N/C | N/A
8 | N/C | N/A

# Notes

- Logger must be running OS>28
- Logger should have a 2GB CF card
- This code supports EXO DCP-SOA v1. It can support v2, but code (se108main.cr1) will need to be updated to handle increased wake up delay time.

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
