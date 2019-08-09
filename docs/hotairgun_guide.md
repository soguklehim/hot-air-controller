## Hot air gun guide

**Keywords for finding a compatible hot air gun:** "858 hot air gun 8 holes"

**Keywords to avoid:** 898, Yihua 898BD (looks exactly the same but incompatible)

It should look like this: 
![Hot Air Gun](img/hotair.jpg?raw=true "Hot Air Gun")

**Connector:** GX16-8

**Pinout [Cable Color]:** 
1. TC + [Orange]
2. TC-, Reed [White]
3. Reed [Yellow]
4. PE [Green]
5. Fan - [Blue]
6. Fan + (24V) [Brown]
7. Heater (AC!) [Red]
8. Heater (AC!) [Black]

**Cable colors only for reference. There is no standards in China - always measure to be sure.**

### Checklist: 

 1. **Visual check:** Check for any anomalies, cracks, dents etc. Check the tip of the air gun, it should look protruded like in the photo. If it is looks like depressed in, it is damaged in shipping. This portion, when sunked in, may directly contact to the heater core itself and create a short. Get a refund, or only use it after a complete disassembly and extensive inspection.
 2. **Heater coil (pins 7-8):** Measure resistance pins between 7 and 8, it should be 60-80ohm for 220V guns and 15-30ohm for 110V guns.
	*  Do not proceed if your reading doesn't match the reference above.
	* Check for continuity 7 and 8 between all other pins. Do not proceed if you measure any resistance.
2. **PE (pin 4):** Verify continuity between this pin and the metal gun tip. 
	* Do not proceed if you measure a resistance higher than 1 ohms.
3. **Reed relay (pins 2-3):** Verify that you measure between pins 2-3 
	* Continuity (<1 ohms), when the air gun is in the stand
	* Open line (infinite ohms), when the air gun is not in the stand
4. **Fan test (optional):** Supply 12-24V DC to pins 5 (-) and 6 (+). You should hear and feel the fan is running.
5. **Thermocouple test (optional):** There is a K type thermocouple in the air gun that is connected to pins 1 and 2. If your multimeter has a range for temperature measurement use this. If not, use the DC millivolt range. With a lighter heat the metal section of the air gun for 10 seconds. You should read a temperature/voltage increase. If the measured temperature/voltage decreases check your connection, you may connected the TC lines reversed. If there is no change after 10 seconds of heating, do not proceed.

**Only connect the hot air gun to the controller after you run through the checklist. It is highly recommended that you inspect the internals of your air gun.**