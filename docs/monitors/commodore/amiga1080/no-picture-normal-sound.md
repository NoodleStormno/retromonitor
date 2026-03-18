# How to Repair the Commodore Amiga 1080 Monitor: No Picture, Normal Sound

**Editor's Note:** This issue differs slightly from "No Raster." Here, the high voltage and raster are present, but the composite video signal is getting lost before it reaches the electron guns.

## 1. Technical Overview: Video Amplification

The composite video signal must be amplified and processed through the signal input board and the main video amp circuit before reaching the CRT.

## 2. Symptoms: What does this look like?

* The screen may show a blank raster (grey or white), but no image.
* Sound is perfectly clear.

## 3. ⚠️ Critical Safety Warning

You will be taking live voltage readings near Q501 and Q208. Keep your hands steady and ground your meter properly to the chassis.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Main Board showing video amplifier circuit (Q208) and Q501*

## 4. Required Tools for the Bench

* DMM
* 0.047 µF test capacitor

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Touch pin 6 of Q501 to ground quickly. No click noise? | Signal Input Board | Check/Replace Signal Input Board Circuit Q124, Q125, Q126. |
| Turn contrast control, screen brightness does NOT vary | Video Amp Circuit | Short emitter/base of Q208. If raster appears, Check/Replace Video amp circuit Q208. |
| Voltage at pin 6 of Q501 is NOT 2-3V | Diodes/Transistors | Check/Replace Q126, D122. |

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 2: Video Terminal Board - Signal input board with Q124, Q125, Q126*

## 6. Repair Conclusion & "Recap" Advice

Video signal loss is frequently caused by a failure in the signal input board transistors (Q124, Q125, Q126) or the main video amplifier Q208.

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 3: CRT Drive Board - Video signal path to CRT*

## 7. FAQ: Pro-Level Calibration

**Q: How do I test IC Q501 directly?**

A: Connect a 0.047 µF capacitor between pin 6 and pin 4 of Q501. If the picture appears, Q501 or X201 needs replacement.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 4: AIN Board - Audio circuitry (working normally)*

## More in:

For related issues, check out: [No Raster (Sound OK)](no-raster-sound-ok.md) - Audio works but screen is black.