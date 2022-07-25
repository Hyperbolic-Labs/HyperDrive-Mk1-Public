

# HyperDrive Mk1 User Manual - FW 0.2.0

---





## Getting Started

> If your HyperDrive isn't installed in your gearbox yet, refer to the HyperDrive Installation Guide to get your build running as quickly as possible. After you've installed your HyperDrive in your gun and are ready to try it out, you will need to calibrate the sensors. Calibration automatically adjusts the sensitivity of the sensors to account for mechanical tolerances in the trigger and selector plate.
>
> 
>
> ### 1	|	Calibration
>
> 1. Plug in battery and immediately press & hold trigger.
> 2. Release the trigger as soon as you hear a beep.
> 3. Wait for 5 sequential beeps. This indicates trigger needs to be calibrated.
> 4. As soon as the beeps end, slowly press and release the trigger several times.
> 5. After 5 seconds, you will hear a success tone if the calibration was accepted.
> 6. You will then hear a series of continuous short beeps. This indicates the selector switch is ready to be calibrated.
> 7. Rotate the selector switch to the 'SAFE' position.
> 8. Press and release trigger. 
> 9. Rotate the selector switch to the 'SEMI' position.
> 10. Press and release trigger.
> 11. Rotate the selector switch to the 'AUTO' position.
> 12. Press and release trigger.
> 13. You will then hear a success tone indicating that the selector switch is calibrated.
> 14. Calibration is now complete!
>
> ![Sensor Calibration Diagram](C:\Users\15417\Dropbox\GitHub\HyperDrive-Mk1\src\assets\020-Recalibrate-Mode.svg)
>
> 
>
> 
>
> Once you've successfully calibrated the sensors, you will need to access the settings through the WiFi interface. Almost any device (phone, tablet, or PC) will work. You do not need an internet connection to access settings, so if needed you can tweak values in the field. Read the following steps to access the settings dashboard.
>
> 
>
> ### 2	|	Connecting to WiFi
>
> 1. Plug in battery and wait for 1.5sec tone.
> 2. Before the tone ends, press & hold trigger.
> 3. After the tone ends, you can release the trigger.
> 4. You should hear a success tone indicating unit is in WiFi Mode. If not, unplug battery and try again.
> 5. On your phone/PC, look for a WiFi access point called "HyperDrive".
> 6. Connect to the access point with the password "12345678".
> 7. Open your browser (Chrome, Safari, Edge, etc) and type "192.168.1.1" into the URL bar and press Enter.
> 8. After a few seconds, the settings dashboard will load.
> 9. Bookmark the page in your browser for easier access next time.
> 10. You can now customize your HyperDrive to suit your needs. Settings are updated in real time, and automatically saved to memory.
> 11. Refer to the [Settings Reference](## [Settings Reference) section for a more detailed description of settings.
>
> ![Entering WiFi Mode](C:\Users\15417\Dropbox\GitHub\HyperDrive-Mk1\src\assets\020-Enter-WiFi-Mode.svg)
>
> 
>
> 
>
> When you've adjusted the settings to your liking and you're ready to use it in a game, just plug in the battery and wait for the tone to complete. All the settings are loaded from memory and it's ready for action!
>
> 
>
> ### 3	|	Normal  Operation
>
> 1. For regular game use it is recommended to use normal mode, as standby power usage is less than in WiFi mode.
> 2. Plug in battery and wait for 1.5sec tone to end without touching trigger.
> 3. Stored calibration values are loaded from memory.
> 4. Your gun is now ready to use!
>
> ![Entering WiFi Mode](C:\Users\15417\Dropbox\GitHub\HyperDrive-Mk1\src\assets\020-Normal-Mode.svg)
>
> 
>
> 
>
> ### 4	|	Firmware Update
>
> 1. In the HyperDrive settings dashboard, click the 'Firmware Update' button
> 2. You will be redirected to a new page. Click the button called 'Choose File', and select the firmware file to apply.
> 3. Click the 'Update' button to the right.
> 4. The firmware update process will take ~1-2 minutes to complete. Make sure the device you're connected to is within 10ft to reduce the chance of a failed update. If it loses connection during the update process, you will need to disconnect the battery and start again.
> 5. If the update was successful, "OK" will be displayed on the screen. Disconnect the battery, and the new firmware has been installed successfully.
> 6. If unsuccessful, "FAIL" will be shown. Disconnect the battery from the Hyperdrive and start again, following the same steps above.
>









# Settings Reference

---



## Trigger

* Trip Point - Sensitivity of the trigger. Lower values mean higher sensitivity. Recommended range is 15-50, but values from 1-100 are accepted. Be aware that setting the sensitivity very high could cause trigger jams.
* Release Point - Trigger is disengaged when the released below this value, so pick a number equal or less than trip point.
* Input Buffer - This feature is not yet implemented.
* DMR Delay - Introduces configurable dead time after a shot (SEMI only). Any trigger pulls during this time period will be blocked. Valid entries range from 0 - 10,000 milliseconds.
* Jam Timeout - This feature is not implemented yet.



## Cycle Settings

* Cutoff Angle - This setting adjusts the angle when power is cut off to the motor. Try different values from 0-360 degrees to determine what works best for your gun. If you have issues with overspin or double shots, try reducing the cutoff angle.
* Active Braking - Sets the strength of the active brake in milliseconds. Higher values will make cycling more consistent, but will increase motor wear and cause additional heating. Typical values are 1-10 milliseconds.
* Burst Size - Configure the number of shots per burst. Valid inputs range from 3 - 50 shots per burst.



## RoF Limiting

* Motor Power - This feature is not implemented yet. 
* Cycle Delay - Adds an additional delay after each cycle. This delay is applied to all modes, including AUTO and BURST. Use this setting to reduce your RoF if needed.
* 1st Cycle Boost - This feature is not implemented yet.



## Battery

* E-Fuse Protection - Protects the motor and electronics from accidental shorts. If the current rises above this level, power to the motor is instantly cut off to prevent damage. Typically this will be set to somewhere in the 50-250 amp range.
* Low Level - This feature is not implemented yet. 
* Empty Level - When the cell voltage in your battery reaches this level, the HyperDrive will go into hibernation mode to prevent damage to the battery. Typical protection levels range from 3100mV-3400mV per cell for LiPo/LiIon. Note that HyperDrive still consumes a small amount of power in hibernation, so it is not recommended to leave the battery connected for long periods of time. 
* Sleep Timer - After this period of time without any trigger events, HyperDrive will enter sleep mode where standby power consumption is reduced to a minimum. To resume normal operation, press and hold trigger for up to 5 seconds until you hear a beep. After waking from sleep, it will enter normal mode. You will need to perform a power cycle to re-enter WiFi mode.



## Game

* Simulated Magazine - This feature is not yet implemented.
* Magazine Capacity - This feature is not yet implemented.
* Magazine Low Level - This feature is not yet implemented.
* Reload Lockout - This feature is not yet implemented.
* Enable Game Timer - This feature is not yet implemented.
* Timer Duration - This feature is not yet implemented.



## Counters

* Shots Since Powered On - Counts the number of rounds fired since power was applied.
* Total Shots - The lifetime total number of rounds. This number is never reset.
* User Shot Counter - This feature is not yet implemented. 
* Reboot Cycles - Number of times power has been applied to the unit.
* Up Time - Number of minutes unit has been powered on. 
* Total Up Time - Lifetime total number of minutes unit has been powered on. This number is never reset. 



## About

* Serial Number - 7 character code used to uniquely identify your device.
* Firmware Version - Check this number to make sure your firmware is up to date with the most recent version.
* Hardware Revision - Tracks which specific hardware version you have. Rev. G has a purple light, Rev. F does not. For all other practical purposes they are identical.
* Mfg Date - The date that the unit was assembled and tested. 
* MAC ID - Unique identification number for the HyperDrive WiFi access point.
* FW Update - Click this button to update the firmware your HyperDrive is running. 



## Modes

* Selector Type - This feature is not yet implemented.

* Position 1 - Change this value to set the mode when the selector is in the 'Safe' position.

* Position 2 - This feature is not yet implemented.

* Position 3 - Change this value to set the mode when the selector is in the 'SEMI' position.

* Position 4 - This feature is not yet implemented. 

* Position 5 - Change this value to set the mode when the selector is in the 'AUTO' position.

  

  ### Mode Options
  
  > - SAFE - Nothing happens when trigger is pulled.
  > - SEMI - 1 round is fired as soon as trigger is pulled. Unit then waits until trigger is released.
  > - BINARY - 1 round is fired as soon as trigger is pulled, then another once trigger is released. If the trigger is not released in 3 seconds, the second round will not be fired.
  > - BURST - Fires a predetermined number of rounds as soon as trigger is pulled. Unit then waits until trigger is released. 
  > - BURST (Interruptible) - Same as BURST, but firing will stop if trigger is released before all of the rounds have been fired.
  > - AUTO - Gun will continuously fire until trigger is released.



## Haptics

* Intensity - This feature is not yet implemented.
* Battery Low- This feature is not yet implemented.
* Battery Exhausted - This feature is not yet implemented.
* Trigger Release - This feature is not yet implemented.
* Mode Change - This feature is not yet implemented.
* Safety Alert - This feature is not yet implemented.
* Mag Low - This feature is not yet implemented.
* Mag Empty - This feature is not yet implemented.
* Game Timer - This feature is not yet implemented.



## Calibration

* Invert Magnet Polarity - If you installed the magnet on the sector gear backwards, the cycle detection algorithm won't work right. Checking this box will invert the polarity of the magnet in software so you don't have to disassemble the gearbox again. A reboot is required to apply this setting.
* Trigger - Click this button to initiate a new trigger calibration. Wait for the 5 consecutive beeps, then follow the same steps you would for a normal trigger calibration. When calibration is done, you will hear a short 'success' tone. 
* 3 Position Selector - Click this button to initiate a new selector calibration. Wait for the beep, then press/release the trigger in the Safe, SEMI, and AUTO positions respectively. When calibration is done, you will hear a short 'success' tone. 
* 5 Position Selector - This feature is not yet implemented. 
* Sector AoE & AoR - This feature is not yet implemented. 



## Diagnostic

* Refresh - Click this button to refresh the diagnostic data. Keep in mind, most fields are updated when the trigger is released.
* Error Code - If the HyperDrive detects any errors, the error code will be shown here. Refer to [Troubleshooting](## Troubleshooting) to look up any error codes. A zero in this field means there are no errors detected.
* Cell Voltage - Displays the volts per cell of the battery. Multiply this number by the number of series cells in your battery to determine the battery voltage. For example, 3.6V/cell * 3S battery = 10.8V.
* Series Cells - As soon the battery is plugged in, your HyperDrive will automatically detect the number of series cells in your battery and display that numbe here. 
* Battery Level - A rough estimation of the remaining charge left in your battery. 4.2V per cell is considered 100% charge, and 0% charge is set to the Empty Level field under 'Battery'.
* FET Temperature - Temperature in °C of the main MOSFET. If this temperature goes above 60°C, power to the motor will be shut off until the unit cools off. 
* Gearbox Temperature - This feature is not yet implemented. 
* Trigger Position - Displays the position of trigger. This number may fluctuate slightly due to imperfect mechanical tolerances of the trigger. 
* Selector Position - Displays the current selector position. 0 = 'Safe' position, 2 = 'SEMI' Position, and 4 = 'AUTO' position.
* Sector Angle - Angle of sector gear. Use this value for troubleshooting overspin issues or determining exact precocking level.
* Est. Battery Resistance - This feature is not yet implemented. 
* Trigger Latency - Duration of time (in microseconds) from trigger being pulled to power being applied to motor. 
* Peak Current - This value is the peak current draw of the motor. In the AUTO column, the peak value is taken from the last cycle. 
* Avg. Current - Average current draw of the motor for SEMI and AUTO. Use this number to gauge how efficient your gearbox is. Average SEMI current is only updated after an AUTO/BURST event.
* Cycle Duration - Number of milliseconds to complete a gearbox cycle. Semi cycle duration is only updated after an AUTO/BURST event. 
* Rate of Fire - Calculated rounds per second. This number is derived from the cycle duration. SEMI rate of fire is only updated after an AUTO/BURST event.
* Est. mAh per Cycle - This experimental figure is calculated from cycle duration and average current, and provides an estimate of the amount of battery capacity used per cycle.









# Troubleshooting

---





| Symptom                                  | Fixes                                                        |
| ---------------------------------------- | ------------------------------------------------------------ |
| No tone when battery plugged in          | Charge or replace battery<br>Check wires for damage<br>Damaged spade connectors to motor<br>Make sure circuit boards aren't damaged |
| Frequent trigger jams                    | Reduce trigger sensitivity & re-calibrate<br>Shim trigger to reduce axial slop<br>Upgrade trigger to CNC aluminum for better mechanical tolerance<br>Trigger has damaged circuit board traces<br>Make sure ETU is clean & dry |
| Incorrect mode selected                  | Re-calibrate selector sensor<br>Dirty or wet selector sensor<br>Replace selector plate<br>Replace selector switch cam for less mechanical slop<br>Damaged selector sensor |
| Frequent overheating                     | Verify ETU is mounted flush with gearbox with good thermal contact<br>Improve gearbox shimming/mechanical efficiency |
| Overspin/Double shot on SEMI             | Reduce cutoff angle<br>Increase active braking level<br>Reduce motor power<br>Reduce battery voltage<br>Change to stiffer spring |
| Overspin on BURST/AUTO                   | Reduce cutoff angle<br>Increase active braking level         |
| Disconnecting from WiFi                  | Move ETU closer to connected device<br>Disable AUTO-connecting to your home network |
| Randomly waking from sleep               | Re-calibrate trigger                                         |
| Not responsive after SEMI cycle          | Reduce DMR delay setting<br>Reduce cycle delay setting<br>Increase trigger release point<br>Increase trigger trip point |
| Gearbox unable to complete cycle         | Check shimming<br>Change or replace battery<br>Switch to high torque motor<br>Switch to battery with higher voltage or capacity<br>Check for damaged wiring |
| Motor only clicks when trigger pressed   | Check wiring for shorts or damaged insulation<br>Charge or replace battery<br>Replace motor<br>ETU has overheated |
| Multiple shots fired on SEMI             | Check for damaged or missing sector magnet<br>Check for damaged circuit board |
| Fires continuously when power is applied | Check wiring and motor for shorts                            |





| Error Code | Description          | Possible Causes                                           |
| ---------- | -------------------- | --------------------------------------------------------- |
| -1         | E-Fuse Tripped       | Shorted wiring or gearbox jam                             |
| -2         | Cycle Timeout        | Motor disconnected or gearbox jam                         |
| -3         | MOSFET Overheated    | Heavy use with high ambient temperature                   |
| -4         | Regulator Overheated | Inadequate heatsinking to gearbox shell with 4S battery   |
| -5         | Low Voltage          | Battery exhausted, damaged wiring, or failing motor       |
| -6         | Trigger Jam          | Trigger sensitivity too high                              |
| -7         | Decock Failed        | Battery level too low, motor disconnected, or gearbox jam |
| -8         | Sector Sensor Fail   | Damaged circuit Board, cracked or missing sector magnet   |
| -9         | Other                | N/A                                                       |







# Miscellaneous

---

- To decock the piston, press and hold the trigger for 5 seconds in SEMI, BINARY, or BURST mode. The piston will be towards the front of the gearbox with the spring stretched out. It is recommended to decock when storing the gun for long periods of time, as it puts the gearbox components under stress.
- When an error occurs during operation, the motor will beep the corresponding error code. For example, an over temperature error (-3) will register as 3 consecutive beeps.
- You may hear an extremely faint clicking sound coming from the ETU. This is a completely normal side effect from the way some of the components are manufactured.
- While in SAFE, HyperDrive will consume less standby power than in other modes.
- Keeping your HyperDrive in WiFi mode during a game may cause it to overheat, especially on a 3S or 4S battery pack.







# Technical Specifications

---

- Operating voltage range: 4.0V - 17.0V
- Current consumption: WiFi ON - 150mA, WiFi OFF - 50mA
- Operating temperature range: -20°C - 50°C
- Maximum current capability: 325A
- Dimensions: 46mm x 29mm x 10mm
- Weight: 25g / 0.88oz

