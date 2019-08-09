## PCB notes

You can use the provided DXF files for making a SMD stencil if you have access to a laser cutter. Grab it from the `hardware` folder. It is adjusted for laser cutting, no extra pad swell required.

### v1.0 Control board render for assembly
![Control Board](img/pcb_control.jpg?raw=true "Control Board")

### v1.1 Power board render for assembly
![Power Board](img/pcb_power.jpg?raw=true "Power Board")

Actual hardware uses green PCBs.

### PCB Errata

Please read if you purchased bare PCBs. Assembled unit owners don't affected - required action already taken by us while assembling.

 - v1.1 Power PCB's has three silkscreen errors:
	- AC input terminals swapped L with N. **This is amended by applying a sticker covering over the top silkscreen. No boards shipped without a sticker. Every order that includes a bare board ships with a reminder about that. Every assembled unit is wired correctly.** Sorry about that. Board renders above has the corrected silkscreen.
    - OK1's orientation marker **dot** is wrong but the **line** is correct. Align the dot on the component itself with the line on the board. 
	![Dot](img/ok1_dot.jpg?raw=true "Dot.")
    - D2 is a bidirectional TVS. Ignore the cathode marking on the board silkscreen, it can be mounted either direction. 
	
	
	
## Assembly notes

### Control board:

 - IC1/IC2 (opamp) and IC3/IC4 (voltage regulator) are alternative footprints on PCB. Only one of them meant to be populated in each pair. BOM components uses IC1 and IC3 (leaves IC2 and IC4 empty). If you prefer to use a different voltage regulator or opamp, you have two different footprint options.
 - For crystal Y1, 3 different footprints provided in the same package. HC-49, HC-49S (crystal) and ceramic resonator. Most ceramic resonators include built-in load capacitors, in that case do not mount C4 and C5. 
 - Solder a 30-60μF 35V capacitor to connector pins 5 (negative) and 6 (positive). In the next hardware version this is moved to the PCB.
 - Control board is isolated from AC mains. Only connector pins 7 and 8 itself wired to AC.

### Power board:
 - OK1 and OK2 should be mounted on the bottom side of the board. SMD and through-hole footprints are provided.
 - Trim all the through hole legs after soldering.
 - Power board AC mains connection also can be used with 3 male blade terminals. I use blade terminals on assembled controllers, BOM includes a screw terminal. 
 - Mount the SMPS to the Power board with 4 self retaining nylon spacers. Position SMPS AC input towards inside of the Power board.
 - This board carries AC mains. **Never** touch it when powered on.

### Cabling:
 - On the Power board, X2 (3 pin, middle pin unused) is the AC supply **to** the SMPS board. X1 (2 pin) is the DC output **from** SMPS board. Both SMPS and the Power board connections uses JST-XH connectors. These are keyed connectors so you can't easily in plug it wrong way. If you are assembling a blank board, take care of the polarity!
 - **Power to Control board - Heater power connection:**
	 - Thanks to the design choice made by hot air gun designers, it is **impossible** to route 700W carrying AC heater lines on the PCB without posing a fire hazard. 
	 - For this reason, GX16-8 connector has 3 pins that needs to be connected to the power board separately. These connections marked clearly as L, N and PE on the Control PCB. Solder 3 wires to these pins with heatshrink and terminate with a female VH connector. Then connect it to X5 on Power board, marked Heater. 
	 - X5 pinout: Pin 1 is PE, pin 2 is N, pin 3 is L. Looking at the bottom side, square pad is pin 1.
 - **Power to Control board - Control connection:**
	 - This connector marked X4 on Power board, X2 on Control board and uses 5 pin JST-XH connectors. 
	 - Connections on both boards uses same pin numbers. For example Pin 1 on Power board should connect to Pin 1 on the Control board. 
	 - If you are going to use premade JST-XH cables, just be sure that you're using the OPPOSITE connector direction variant. Same direction cables will REVERSE the pin order on the other end. 
		 - Making this mistake will damage the Control board quite spectacularly. Be careful.
 - **Power board to mains:**
	 - Since Power board itself is not fused, It is **mandatory** to use a fused socket. Fused and switched IEC 60320 C14 sockets are recommended. For 220V use 4A, for 110V use 8A fuse. 

### Notes
 - Correct PE connection and GFCI in your outlet/fuse box is only thing that will protect you from an electrocution risk on mains powered circuits. PE is your life insurance and it is important. If you use a metal enclosure/front panel etc., connect it to PE. If, for some reason you blow a fuse or trigger a GFCI **do not EVER try to power it again without finding and fixing the root cause.**