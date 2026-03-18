# How to Repair the Commodore Amiga 1080 Monitor: No Raster (Screen Completely Dark)

**Editor's Note:** A completely dark screen with no raster is a classic CRT symptom. The Amiga 1080 relies on specific voltages at the CRT grids and a functioning heater to draw the electron beam.

## 1. Technical Overview: The Electron Beam Path

The CRT requires a heated cathode to emit electrons and high voltages on the grids (G2 and G3) to accelerate them to the screen. Without these, the screen remains black.

## 2. Symptoms: What does "No Raster" look like?

* The screen is pitch black when powered on.
* No static sound when touching the glass.
* The neck of the CRT does not glow (heater off).

## 3. ⚠️ Critical Safety Warning

READ THIS BEFORE OPENING: High voltage up to 27.5kV may be present at the second anode. Always discharge the picture tube anode to the CRT conductive coating before handling.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Amiga 1080 Main Board (PW5252-3) - Location of critical components*

## 4. Required Tools for the Bench

* High Voltage Probe (accurate and reliable)
* Digital Multimeter (DMM)
* Oscilloscope

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Heater is not lighting | Missing Flyback Pulse or bad FBT | Check for 25Vp-p pulse at #9 of FBT. |
| 115V missing at #2 of FBT | Power Supply or R427 | Check power circuit or check if R427 is open. |
| G2 voltage is not approx 600V | CRT or R920 | Check R920 and CRT. |
| G3 voltage is not approx 7kV | Focus Pack | Check focus pack and CRT. |

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 2: CRT Drive Board (PW5252-2) - Contains focus and G2/G3 voltage circuits*

## 6. Repair Conclusion & "Recap" Advice

A missing raster often traces back to a lack of high voltage generation. If the horizontal oscillator and drive are normal but the 115V at the FBT is missing, investigate the horizontal output transistor and the FBT itself.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 3: AIN Board (PW5253) - Audio and input circuitry*

## 7. FAQ: Pro-Level Calibration

**Q: How do I measure the high voltage safely?**

A: Connect an accurate high voltage meter to the second anode of the picture tube with brightness and contrast at minimum. It must not exceed 27.5kV.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 4: Video Terminal Board - Input signal processing*

## More in:

For related issues, check out: [Power Supply Failure](power-supply-failure.md) - Troubleshooting +115V rail and power circuit problems.