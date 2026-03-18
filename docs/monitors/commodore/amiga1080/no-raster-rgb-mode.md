# How to Repair the Commodore Amiga 1080 Monitor: No Raster in RGB Mode

**Editor's Note:** If you lack a raster entirely only when switched to RGB mode, the issue lies in the sub-brightness circuitry or the IC controlling the CRT drive exclusively for RGB.

## 1. Technical Overview: RGB Brightness Control

RGB mode utilizes a separate sub-brightness control (R256) and relies on a 12V line feeding IC Q121 to drive the guns.

## 2. Symptoms: What does this look like?

* Composite works.
* RGB mode has a completely black screen (no raster).

## 3. ⚠️ Critical Safety Warning

High voltage is still active even if the screen is black in RGB mode.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Amiga 1080 Main Board (PW5252-3) - RGB sub-brightness control circuitry*

## 4. Required Tools for the Bench

* DMM

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Turning RGB Sub-Brightness (R256) fixes the issue | Miscalibration | Adjust RGB Sub-Brightness (R256). |
| DC voltages at 12V line are NG | Power routing diodes | Check/Replace Q118, D112, D124, D125, D126, D127. |
| Voltages at #14, #17, #20 of Q121 are NOT 6~7V | Drive IC | Check/Replace Q121, Q119, Q120. |

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 2: CRT Drive Board (PW5252-2) - RGB drive IC and brightness controls*

## 6. Repair Conclusion & "Recap" Advice

A missing RGB raster is usually a simple misadjustment of R256 or a failure of the 12V routing components (Q118, D112).

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 3: AIN Board (PW5253) - Power routing and voltage regulation*

## 7. FAQ: Pro-Level Calibration

**Q: How do I correctly set RGB Sub-Brightness?**

A: Feed a black pattern signal. Set contrast and brightness to the click position. Adjust RGB SUB-BRIGHTNESS (R256) until the raster is slightly visible.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 4: Video Terminal Board - Mode switching and signal routing*

## More in:

For related issues, check out: [No Color (Monochrome)](no-color-monochrome.md) - Troubleshooting color decoding and sync issues.