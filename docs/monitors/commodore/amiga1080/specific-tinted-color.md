# How to Repair the Commodore Amiga 1080 Monitor: Specific Tinted Color

**Editor's Note:** If everything on the screen looks heavily tinted red, green, or blue, one of the color drive channels has likely failed.

## 1. Technical Overview: CRT Drive

The demodulated color signals leave Q501 and travel to the CRT Drive Board, where they are amplified to drive the specific Red, Green, and Blue cathodes.

## 2. Symptoms: What does this look like?

* The entire image is washed in a single strong tint.
* Certain colors are entirely missing from the spectrum.

## 3. ⚠️ Critical Safety Warning

The CRT Drive Board sits directly on the neck of the picture tube. Be extremely gentle to avoid snapping the fragile glass neck of the CRT.

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 1: CRT Drive Board (PW5252-2) - Color drive transistors and amplification stages*

## 4. Required Tools for the Bench

* DMM
* Non-metallic alignment tool

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Voltages at Pins 19, 20, 21 of Q501 are Normal | Sync Capacitor | Adjust C551. If it cannot be adjusted, Check/Replace X501, C551. |
| Voltages at Pins 19, 20, 21 of Q501 are Abnormal | CRT Drive Board / Q121 | Detach connection of Demod Output Leads. Check/Replace Q121 and parts in CRT DRIVE Circuit. |

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 2: Amiga 1080 Main Board (PW5252-3) - Q501 IC and color demodulation outputs*

## 6. Repair Conclusion & "Recap" Advice

A specific color tint usually indicates a blown transistor on the CRT Drive Board or a failure of the color demodulator outputs on Q501.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 3: AIN Board (PW5253) - Signal processing and color balance controls*

## 7. FAQ: Pro-Level Calibration

**Q: How do I adjust SUB-TINT and SUB-COLOR?**

A: Apply a rainbow color signal. Set CONTRAST, COLOR, and TINT to the click position. Adjust the SUB TINT (R553) and SUB COLOR (R554) controls to obtain a good tint and color.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 4: Video Terminal Board - Color signal input and processing*

## More in:

For related issues, check out: [No Sound](no-sound.md) - Troubleshooting audio amplification and speaker issues.