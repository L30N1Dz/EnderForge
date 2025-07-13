## ✨ Overview

**EnderForge** is custom-tuned firmware built upon the powerful [Marlin](https://marlinfw.org/) platform, specifically tailored for the Ender 5 printer. It incorporates several community-driven upgrades to enhance your printing experience, providing superior performance, reliability, and customization.

---

## 🔧 Features

* ✅ Optimized for custom Ender 5 builds
* ✅ Integrated community-driven enhancements
* ✅ Frequently updated for improved features and stability

Specific Firmware Changes from Stock Ender 5:

* Base Firmware Package - Vanilla Marlin (latest Beta) Using Creality Silent 4.2.7 mainboard W/ BL Touch.
* defined CUSTOM_MACHINE_NAME "EnderForge ;)"
* defined AUTO_BED_LEVELING_BILINEAR (better leveling vs default linear)
* defined PREHEAT_BEFORE_LEVELING (I only preheat the bed, nozzle=19 bed=60)
* defined TEMP_SENSOR_0 = 5 (This is for the 104t-4 100K thermister on my hot-end, non-stock)
* defined Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN (I use an older two connector BL-touch)
* defined INVERT_E0_DIR = true (My extruder was running backwards, possibly due to the non-stock extruder)
* Custom Boot Screen.
  
Upgrades:
* Creality 4.2.7 Silent Mainboard
* BLtouch bed leveling
* All Metal Extruder
* New Bed Springs
* Capricorn Tubing
* A pair of Y-axis Belt tensioners.
* Cantaliever Bed Support Arms (Printed)
* Official Creality Printer Enclosure (I do NOT reccomend, works fine but there are better and cheaper options... Why does my printer have to sit sideways in it?)
* Heatsinks and 12v Fans on both the Extruder and Y axis Nema Motors (Buck Converter was added to power the fans off the 24V PSU)
* Top Mounted Extruder (Printed the mount)
* Non standard placement of screen and filiment feed.
* 115W Ceramic Heater, 104T-4 Thermister, New heatsink w/ BiMetal heatbreak (copper and titanium) (VS stock 40W PTFE fed heatbreak)
* Direct Drive using stock extruder motor
* Hydra Toolchanger Toolhead and dual 5051 Blower fans with heat threaded brass inserts for the fan
* Front BL touch adapter for Hydra Toolchanger

Other:
  
* Custom USB connection (I blew up the UART -> Serial USB chip while O-scope probing for a pin to use to run a 90W diode laser, DO NOT TEST WITH EARTH GROUND! (forgot printer was USB to PC IE grounded through PC, woops...)
( I Had a couple spare Uart to Serail converters for other projects, not the same chip but they work the same way. I have had Zero issues with it, all i did was soughter to the TX and RX (and a common ground, didn't even remove the blown chip, hooked up to my adapter board and issue resolved.)
* Installed Bootloader with Arduino UNO (simplest method) Installing Firmware from an SD is 1000% easier and if you didn't own a printer when the Ender 5 came out you probably have no idea what I'm talking about lol.
* Not a physical upgrade but good to *NOTE* : The Original Ender 5 (maybe you found one secondhand) still had old enough Firmware to not include Thermal Runaway Protection, that was the very first upgrade i did (A firmware upgrade to the latest Marlin at the time as Creality had not implemented the feature yet in their modified Marlin Firmware. No longer an issue afaik, but keep it in mind.

Upcoming:
* Klipper Firmware
* Z-rod stabalizer (found an amazing product for the zero-G printers that will work on the Ender 5 10-20$ on AliExpress, It removes the ringing and wobble caused by moving Z-rod.)
* Linear Railes, YES, NO? (Not much benifit but I don't like the current setup)
* Eventually a self leveling Bed (3 adjustable axis/leveling points)
  
---

## ⚡ Getting Started

Simply clone this repository, configure it as needed for your Ender 5 setup, and flash your printer with the provided firmware build.

```bash
git clone https://github.com/YourUsername/EnderForge.git
```

---

## 📌 Updates & Contributions

Updates occur as frequently as possible. If you notice a feature in a newer Marlin release you'd like included, please [submit an issue](https://github.com/YourUsername/EnderForge/issues). To request an update featuring your own custom design or enhancement, please open a new [feature request issue](https://github.com/YourUsername/EnderForge/issues/new?template=feature_request.md).

---

## 🌟 Future Plans

Stay tuned! Future firmware builds may include:

* 🔹 Klipper firmware variant
* 🔹 Additional community upgrades

---

## 🛠️ Maintained by AstroCat

Firmware managed by AstroCat, the legendary space-faring feline engineer at **IGBOTO Lab's**. [AstroCat@IGBOTO.com](mailto:AstroCat@IGBOTO.com)

---

