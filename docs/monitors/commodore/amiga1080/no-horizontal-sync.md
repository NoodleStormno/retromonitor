# How to Repair the Commodore Amiga 1080 Monitor: No Horizontal Sync

**Editor's Note:** The horizontal sync circuit is the heartbeat of the display. If this fails, the image becomes an unrecognizable mess of diagonal lines.

## 1. Technical Overview: The Sync Heartbeat

The horizontal synchronization circuit utilizes Automatic Frequency Control (AFC) to lock the electron beam to the frequency of the video output. The core component is IC Q501.

## 2. Symptoms: What does "No Horizontal Sync" look like?

* The image is visible but sliced into diagonal shreds.
* The image is a chaotic mess of lines tearing horizontally.

## 3. ⚠️ Critical Safety Warning

Do not touch the heat sinks near the flyback transformer while the unit is powered. Components in this area can carry high voltage and extreme heat.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Main Board showing horizontal sync circuit and flyback transformer*

## 4. Required Tools for the Bench

* Oscilloscope
* DMM
* Non-metallic alignment tool

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Picture stabilizes by rotating R451? NO | Hold Circuit | Check Hold circuit and Q501. |
| Picture stabilizes by rotating R451? YES | Move to next test | Check for 10Vp-p sync pulse at #37 of Q501. |
| Sync pulse (10Vp-p) is absent | Sync Circuit | Check Sync Circuit and Q501. |
| Sync pulse (10Vp-p) is present | AFC Circuit | Check AFC circuit and Q501. |

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 2: CRT Drive Board - Horizontal deflection components*

## 6. Repair Conclusion & "Recap" Advice

Most horizontal sync issues are resolved by checking the AFC circuit or reflowing solder joints around Q501 and the H. HOLD control (R451).

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 3: Video Terminal Board - Horizontal sync signal input*

## 7. FAQ: Pro-Level Calibration

**Q: How do I properly adjust horizontal hold?**

A: Connect a white pattern signal, set brightness to maximum, connect terminal N of the main board to +12V with a jumper, adjust H. HOLD (R451) until the picture stops moving, and then remove the jumper.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 4: AIN Board - Control signal routing*

## More in:

For related issues, check out: [No Vertical Sync](no-vertical-sync.md) - Rolling picture and vertical hold issues.