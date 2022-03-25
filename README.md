# HyperDrive-Mk1-Public


## Bootup Sequence:

1. Plug in battery and wait for beep
2. Hold down trigger until beep ends
3. To enter normal mode, release trigger
4. To enter WiFi mode, continue holding down trigger until you hear 3 short beeps
5. Turn the selector to 'Safe' position
6. Pull and release the trigger to calibrate 'Safe'
7. Turn the selector to 'Semi' position
8. Pull and release the trigger to calibrate 'Semi'
9. Turn the selector to 'Auto' position
10. Pull and release the trigger to calibrate 'Auto'
11. You will hear a short tone indicating the bootup sequence is complete, the gun is ready for operation





## Notes About User Interface:

- Settings are updated and saved to memory after entering a number and pressing 'Enter', or by tapping/clicking on another area of the screen
- Diagnostic data is updated after trigger release
- There is a known bug that affects the displayed battery voltage in WiFi mode (reporting slightly lower than actual).
- By default, hyperdrive will enter sleep mode after 24 hours of inactivity. To exit sleep, hold down the trigger until you hear a tone. If wifi was previously enabled, it will be turned off until the next reboot. 
- When the LiPo cell voltage drops below 3.15V, Hyperdrive will enter shutdown mode. To take it out of shutdown, unplug the dead battery and connect a fresh one. Even in shutdown, it will consume a small amount of current, which WILL CAUSE DAMAGE TO YOUR LIPO if left plugged in for extended periods of time.
- With a 4S LiPo and Wifi turned on, Hyperdrive will get very warm which could cause thermal shutdown during a game. In normal mode this won't be an issue.





## Notes about Firmware Update:

### I have made significant progress with the stability of FW updates, but occasionally there will be issues. I'm still in the process of figuring out the root cause, but here are a few things to try if you run into problems:
- Verify that your device is still connected to the Hyperdrive network
- Make sure the hyperdrive is physically close to the device you're updating from. If you have a metal receiver, the wifi signal will be weaker, and updates may only work within a few feet. 
- If you're updating from a phone or laptop, taking it out of battery saver mode can help
- Try updating from a different device

If the update is successful, you will get a blank white screen with "OK" in the upper left corner






### FW Version 0.1.1 Power Consumption

| Current Consumption  | 2S    | 3S    | 4S    |
|----------------------|-------|-------|-------|
| normal               | 35mA  | 32mA  | 30mA  |
| wifi (not connected) | 130mA | 130mA | 130mA |
| wifi (connected)     | 125mA | 125mA | 125mA |
| wifi (during update) | ~180mA| ~180mA| ~180mA|
| sleep                | 2.5mA | 2mA   | 1.7mA |
| shutdown             | 600uA | 900uA | 90uA  |


