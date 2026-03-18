# How to Repair the Commodore Amiga 1080 Monitor: Power Supply Failure

**Editor's Note:** A stable power supply is the foundation of the Amiga 1080. The critical voltage line is the +115V rail, which drives the high-voltage flyback circuit.

## 1. Technical Overview: The +115V Rail

The power board converts AC line voltage into a regulated +115V DC supply. If this voltage drops to zero or spikes, the monitor will fail to operate or trigger protection circuits.

## 2. Symptoms: What does "Power Failure" look like?

* Total loss of power (no LED, no sound).
* Clicking sounds from the chassis.
* The fail-safe (FS) circuit trips immediately upon power-up.

## 3. ⚠️ Critical Safety Warning

The power circuit handles direct AC mains voltage. Perform an AC leakage current check before returning the set to operation to ensure exposed metallic parts do not exceed 1.5 volts RMS.

![Amiga 1080 Main Board](images/1080A_MAIN BOARD PW5252-3.png)
*Figure 1: Main Board showing power supply section and +115V regulation*

## 4. Required Tools for the Bench

* DMM isolated from mains
* Soldering Iron
* Replacement Fuses (3A 125V and 1.2A 125V)

## 5. Step-by-Step Troubleshooting Flowchart

| Measurement Result | Likely Culprit | Action |
| :--- | :--- | :--- |
| 115V measures 0V | Blown Fuse | Check fuse F802. |
| F802 is OK, but still 0V | AC Fuse or Rectifier | Check AC fuse and R803. If OK, check voltage at C809 (approx 160V). |
| 115V is too low or too high | Error Amp | Check Error Amp circuit Q804, D814, etc. |
| Voltage at C809 is 0V | Rectifier Circuit | Check Rectifier circuit and wiring. |

![Amiga 1080 Mechanical Disassembly](images/1080A_Mechanical Disassembly.png)
*Figure 2: Mechanical disassembly showing power supply access points*

## 6. Repair Conclusion & "Recap" Advice

Power failures are frequently caused by shorted switching transistors (Q801, Q802) or blown fuses. Always check the over-voltage protector (D806, D813) if the rail shuts down under load.

![Amiga 1080 CRT Drive Board](images/1080A_CRT DRIVE BOARD PW5252-2.png)
*Figure 3: CRT Drive Board - Connected to main power supply*

## 7. FAQ: Pro-Level Calibration

**Q: Where is the +115V adjustment located?**

A: Use the R851 potentiometer (+115V ADJ) located on the main board.

![Amiga 1080 AIN Board](images/1080A_AIN BOARD PW5253.png)
*Figure 4: AIN Board - Secondary power distribution*

## More in:

For related issues, check out: [No Raster (Screen Completely Dark)](no-raster-dark.md) - Complete black screen troubleshooting.