# se108
se108 datalogger device configuration utility scripts and support files
# Notes

- Logger must be running OS>28
- Logger should have a CF card
- This code supports EXO DCP-SOA v1


# Directions
-If you edit any files in the se108.zip (e.g. se108main.cr1, se108settings.cr1 or control.xml) to change the programs behavior, you must zip into se108.zip prior to launching the device configuration utility (DCU)

-Prior to launching the DCU for the first time, you must edit the target of the shortcut .lnk file to reflect the correct path to devconfig.exe and the zip file that contains the crbasic scripts for the dev config utility to launch correctly. 

Here is an example:

C:\Program Files (x86)\Campbellsci\DevConfig\devconfig.exe" --customise="c:\se108\se108.zip
