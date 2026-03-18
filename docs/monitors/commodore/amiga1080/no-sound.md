# How to Repair the Commodore Amiga 1080 Monitor: No Sound

**Editor's Note:** The Amiga 1080 includes a built-in speaker. If the picture is flawless but the audio is dead, the audio amplification circuit is the target.

## 1. Technical Overview: Audio Amplification

The sound signal is processed through an output circuit containing transistors Q604 and Q605, and transformer T601, before reaching the speaker.

## 2. Symptoms: What does this look like?

* Normal picture.
* Complete silence from the speaker, even with the volume knob turned up.

## 3. ⚠️ Critical Safety Warning

Always unplug the monitor before checking physical connections like W661 or the speaker terminals.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 1: AIN Board (PW5253) - Audio input and preamplification circuitry*

## 4. Required Tools for the Bench

* DMM
* 0.047 µF test capacitor

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| Check W661. Is it OK? NO | Wire W661 | Defective W661. |
| Connect 0.047 µF cap between pin 30 of Q501 and base of Q605. Sound OK? NO | Sound Output Circuit | Faulty sound output circuit. Defective Q604, Q605, T601, R619. |
| Connect 0.047 µF cap between pin 30 of Q501 and base of Q602. Sound OK? NO | Preamplifier stage | Defective Q602, Q603. |
| Cap test at Q602 yields Sound OK (YES) | Volume Pot / Connector | Defective Sound VR (R651), Connector P602, M111, Q601. |

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 2: Amiga 1080 Main Board (PW5252-3) - Audio amplification transistors and transformer*

## 6. Repair Conclusion & "Recap" Advice

Dead audio is frequently traced back to the sound output transistors (Q604, Q605), the audio transformer (T601), or simply a dirty volume potentiometer (R651).

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 3: CRT Drive Board (PW5252-2) - Audio signal routing and connections*

## 7. FAQ: Pro-Level Calibration

**Q: Can I use headphones with this monitor?**

A: Yes, there is a dedicated HEADPHONE JACK BOARD (PW5252-4) connected via P661. Ensure this jack isn't physically stuck, as it mutes the main speaker.

![Amiga 1080 Video Terminal Board](images/1080A_Video Terminal Board.png)
*Figure 4: Video Terminal Board - Audio input connectors and signal routing*

## More in:

For related issues, check out: [No Raster (Screen Completely Dark)](no-raster-dark.md) - Troubleshooting complete display failure with no raster.