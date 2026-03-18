# How to Repair the Commodore Amiga 1080 Monitor: No Raster (Sound OK)

**Editor's Note:** If you can hear the Amiga's audio but the screen is dead, the composite video processing or horizontal drive stage has failed, while the power supply remains active.

## 1. Technical Overview: Raster Generation

Raster generation requires the horizontal output transformer (T461) to create the high voltage and heater pulses necessary for the CRT.

## 2. Symptoms: What does this look like?

* Audio plays normally.
* The screen is entirely black.

## 3. ⚠️ Critical Safety Warning

Even if the screen is black, high voltage may still be present at the anode. Discharge before touching the flyback transformer (T461).

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Main Board showing flyback transformer (T461) location*

## 4. Required Tools for the Bench

* DMM
* Oscilloscope

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| CRT Heaters are lit, but no HV at 2nd Anode | Horizontal Output | Check/Replace Horiz. Output Trans. T461. |
| Heaters lit, HV OK, DC +16.5V is missing | Supply Line Components | Check/Replace D403, D409, R428, R438. |
| CRT Heaters are not lit | Heater Pulse | Check Heater pulse at #9 of T461. |
| Heater pulse OK but heaters off | Wiring / Fusible Resistor | Check/Replace Wiring and Fusible Resistor R920. If still no raster, replace CRT (heater open). |

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 2: CRT Drive Board - Heater circuit and fusible resistor R920*

## 6. Repair Conclusion & "Recap" Advice

A missing raster with good sound usually points to a break in the horizontal deflection path (T461) or an open CRT heater filament. Always check R920 if the heater pulse is present but the tube won't glow.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 3: Video Terminal Board - Video signal input*

## 7. FAQ: Pro-Level Calibration

**Q: What is the typical voltage for Q501 pins 19, 20, 21?**

A: You should expect a typical DC voltage of 7V on these pins.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 4: AIN Board - Audio circuitry (working in this scenario)*

## More in:

For related issues, check out: [No Picture, Normal Sound](no-picture-normal-sound.md) - Raster present but no video signal.