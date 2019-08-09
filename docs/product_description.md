Hot Air Rework Controller for generic 858D / 85x heat guns

A small, portable and robust hot air controller for generic Chinese 858D / 8586 / 8858 / 852 / 878 / 858 hot air guns.

## General Specifications and Features

-   Designed to use with Chinese 858D / 8586 / 8858 / 852 / 878 / 858 hot air guns.
-   Aims to be a safer alternative compared to existing controllers. For example:
    -   It will [not](https://www.youtube.com/watch?v=WPy9XYGDmWQ) [try](https://www.youtube.com/watch?v=WPy9XYGDmWQ) [to](https://www.youtube.com/watch?v=A319o8Ji4oI) [kill](https://www.youtube.com/watch?v=pgR7YbXUivs) [you](https://www.eevblog.com/forum/chat/deadly-wiring-fault-atten-858d-hot-air-rework-station/) (if you have a GFCI): Mains and earth connection are correctly wired.
    -   It will not [spontaneously combust](https://www.youtube.com/watch?v=tUFW5teeRBM) when left alone: Cuts off the hot air gun heater completely from mains after an idle timeout. Protects even if the unlikely event of TRIAC failure thanks to an internal relay.
    -   Safe to remove/change hot air gun while powered on: Both mains hot and neutral is disconnected from the front connector when the tool is removed so it is always safe to touch. 
-   Celsius or Fahrenheit display modes.
-   Works with the stand/holder: You can use the original holder or make your own with magnets.
-   Cools the tool down when in stand, with set thresholds.
-   Goes to sleep if left on stand. Selectable intervals or can be disabled. Wakes up automatically when needed.
-   Selectable power-on temperature and air: It can remember the last used settings as well (default).
-   Power limit: You can limit the maximum heating power on demand. Useful with under-powered UPSes or generators.
-   Selectable AC power regulation strategy: Phase angle (more precise) or pulse skip (less noisy).\* 
-   Internal temperature sensor used for compensating ambient temperature.
-   Manual calibration for ambient and tool set temperature.
-   Controller itself will work with 100-250V AC, 30-80Hz. (but you MUST use a hot air gun that rated for your mains voltage)



## Important!

This product is only a controller for specified hot air guns. **You must also have the hot air gun itself and its stand for a working system. These are not included.** These hot air guns are cheap and may arrive defective from manufacturing or shipping. Defective/incompatible hot air guns may damage the controller and/or trip your GFCI or worse. **It is entirely your responsibility to check if the hot air gun is compatible and not defective (use my guide for this). I cannot be held responsible if anything bad happens to controller or you. This is a DIY product. It does not have any certifications. I hope you have been sufficiently warned.**

[Click here for the hot air gun guide](https://github.com/soguklehim/hot-air-controller/blob/master/docs/hotairgun_guide.md)



## Options

You have three options that you can choose based on how adventurous are you.

1.  **Fully assembled controller**
    
    -   Includes one Hot Air Controller, tested and ready to work.
	
2.  **Assembled boards**
    
    -   Includes one front panel assembly (Control board + front panel) and one Power board, with all components mounted and tested.
    -   This is equals to Option 1 minus the case, back panel and AC socket. Mount it to a case of your liking, wire Power board to AC mains connection and it is ready to work.
	
3.  **Empty boards**
    
    -   Includes one blank Control board and one blank Power board. Without components, **but an unsoldered, preprogrammed ATMEGA328P-AU will be included** for the controller board. Use the provided BOM and your DIY skills for a working controller.
    
    

## You'll also need (not included)

-   AC power cable 
-   Hot air gun
-   Hot air gun stand



## Open(-ish) source

**Following elements of this product are available free of charge:**

-   Control and power board schematics
-   Control and power board BOM and assembly guide
-   Open source version of source code (coming soon)
    -   If you purchase an option that includes an assembled control board, it'll sent preprogrammed with the "closed" version of the code. Open source version has different fonts and temperature control algorithm (because I can't redistribute the sources of these). Otherwise, functionality is the same. 

> Originally this is going to be closed source (like all of my hardware products) but I decided to release an open version of the work due to popular demand. Porting things to Arduino ecosystem and replacing/rewriting/converting closed source to open takes time. It is still ongoing and I'm currently investing my time on that but it is not my first priority. Thank you for your understanding.

All assembled control boards ships with unlocked Optiboot bootloader. ICSP pins are also broken out if you really need that 0.5K. Happy hacking!

[Link to the repo](https://github.com/soguklehim/hot-air-controller/)



## Physical:

-  Dimensions: 110x105x50mm
-  Weight: 400gr



## Notes:

-   Currently shipping:
	-   Firmware: v1.0.24
    -   Control board: v1.0
    -   Power board: v1.1
-   AC input socket: IEC 60320 C14: Also known as "computer cable". (for assembled option)
-   Please read the "Shipping Policies" section at the store page ("View Store" button) before ordering.