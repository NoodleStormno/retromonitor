# How to Repair the Commodore Amiga 1080 Monitor: No Color (Monochrome)

**Editor's Note:** An Amiga monitor stuck in black and white strips away the machine's greatest asset. This points to a failure in the chroma decoding stage.

## 1. Technical Overview: Color Synchronization

The color sync circuit decodes the NTSC color burst. This requires Q501 to function correctly and receive proper horizontal pulses.

## 2. Symptoms: What does this look like?

* Composite video displays a sharp, stable picture, but entirely in black and white.

## 3. ⚠️ Critical Safety Warning

Use isolated test probes. You will be shorting live pins on Q501 during this diagnostic.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Amiga 1080 Main Board (PW5252-3) - Color sync and Q501 IC location*

## 4. Required Tools for the Bench

* DMM
* 0.047 µF test capacitor

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Short Pin 13 of Q501 to +12V. Result is Abnormal | Q501 or Control Circuit | Check voltage at each Pin of Q501. Replace Q501 if abnormal, or check Color Control Circuit if normal. |
| Short Pin 13 to +12V. Result is Normal Color | Horizontal Pulse | Check/Replace Horizontal Pulse Circuit. |
| Connect 0.047 µF cap between TP41 & TP42. No signal | Color Sync Circuit | Check Color Sync Circuit. |

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 2: CRT Drive Board (PW5252-2) - Color demodulation and sync circuits*

## 6. Repair Conclusion & "Recap" Advice

Loss of color is almost always tied to IC Q501, the horizontal pulse circuit, or out-of-spec components in the color sync loop (R239, C204, L204).

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 3: AIN Board (PW5253) - Signal processing and color decoding*

## 7. FAQ: Pro-Level Calibration

**Q: How do I align the color sync?**

A: Connect a 0.47 mfd capacitor between TP-42 and the junction of C204/C205. Connect a 1k ohm resistor between pin 13 of IC501 and +11V. Adjust variable capacitor C551 until the color bar pattern stands still.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 4: Video Terminal Board - Color signal input and processing*

## More in:

For related issues, check out: [Specific Tinted Color](specific-tinted-color.md) - Troubleshooting single-color dominance issues.