# How to Repair the Commodore Amiga 1080 Monitor: No Vertical Sync

**Editor's Note:** A rolling picture is a frustrating experience. The vertical sync circuit in the Amiga 1080 locks the vertical refresh rate to the incoming 60Hz signal.

## 1. Technical Overview: Vertical Lock

The vertical hold circuit aligns the monitor's internal vertical oscillator with the synchronization pulses from the Amiga. This is managed primarily by IC Q501.

## 2. Symptoms: What does "No Vertical Sync" look like?

* The picture rolls continuously up or down the screen.
* Adjusting the V. Hold knob changes the rolling speed but cannot stop it entirely.

## 3. ⚠️ Critical Safety Warning

Use non-metallic alignment tools when adjusting potentiometers on a live chassis to prevent accidental shorts to high-voltage lines.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Main Board showing vertical sync circuit around Q501*

## 4. Required Tools for the Bench

* Plastic adjustment wand
* Oscilloscope
* DMM

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Picture stabilizes by rotating R351? YES | Sync Circuit | Check sync circuit and Q501. |
| Picture stabilizes by rotating R351? NO | V. HOLD Circuit | Check V. HOLD circuit and Q501. |

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 2: Video Terminal Board - Sync signal input processing*

## 6. Repair Conclusion & "Recap" Advice

If the V. HOLD control (R351) has no effect or cannot center the lock, suspect degraded capacitors in the vertical hold circuit surrounding Q501.

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 3: CRT Drive Board - Vertical deflection components*

## 7. FAQ: Pro-Level Calibration

**Q: How do I calibrate the Vertical Hold?**

A: Feed a white pattern signal, set brightness to the click point, and turn the V. HOLD control (R351) to the center of the vertical hold range.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 4: AIN Board - Audio and control circuits*

## More in:

For related issues, check out: [No Horizontal Sync](no-horizontal-sync.md) - Diagonal tearing and horizontal sync problems.