# PS3 and RPCS3 System Errors - Explained

This document contains a detailed description of various system errors related to the PlayStation 3 and RPCS3 emulator.

---

## BSOD (Blue Screen of Death)
- **What it does:** Corrupts (deletes lines of text from) the backup file `Xregistry.sys` (`dev_flash2/etc/backup/`) and deletes the main `Xregistry.sys` (`dev_flash2/etc/`).

---

## Severe BSOD
- **What it does:** Deletes only `libuserdata.sprx` (or similar) from `dev_flash/sys/external/`.

---

## RSOD (Red Screen of Death)
- **What it does:** 
  - On RPCS3: impossible to trigger.
  - On real PS3: deletes `vsh.self` located in `dev_flash/vsh/module/`.

---

## "A serious error has occurred"
- **What it does:** Similar to RSOD. 
  - On RPCS3: can be triggered.
  - Corrupts the `sys_init_osd.self` file in `dev_flash/vsh/module/`.

---

## "Cannot start. The appropriate hard disk was not found."
- **What it does:** Remove the SSD or HDD physically.
  - On RPCS3: try corrupting files inside `dev_hdd0`, but it's not 100% reliable.

---

## Severe RSOD
- **What it does:** Extremely rare. It is believed that almost all essential system files are corrupted except XMB.

---

## "The hard disk's file system is corrupted and will be restored."
- **What it does:** 
  - On RPCS3: delete `dev_hdd0`.
  - On real PS3: corrupt files inside `dev_hdd0` or poorly format the HDD/SSD.

---

## "Corrupted Data"
- **What it does:** Corrupt the `EBOOT.BIN` file of any app to cause this.

---

## YLOD (Yellow Light of Death)
- **What it does:** Cannot be simulated. Occurs when CPU or GPU solder points physically disconnect due to heat or age.

---

## GLOD (Green Light of Death)
- **What it does:** Similar to YLOD, but slightly less severe.

---

## GARLOD (Green and Red Light of Death)
- **What it does:** Can occur due to system overheating. May share causes with YLOD if more severe.

---

## Semi-brick
- **What it does:** Occurs when a system update fails or non-critical files get corrupted.
  - Doesn't show "A serious error has occurred".

---

## Full Brick
- **What it does:** Critical. Occurs with YLOD/GLOD/GARLOD. The PS3 becomes completely unusable (no video, no response).
  - Only solution: reflash the NOR/NAND chip.
  - Can be accompanied by BSOD.

---

## Visual Glitches
- **What it does:** Caused by corruption or deletion of visual assets (XMB, WAVE, PS3 boot icons).
  - If severe, it means essential visual system files are missing.

---

## Audio Glitches
- **What it does:** XMB or system sounds are corrupted or missing.
  - On RPCS3: install firmware 2.80 or below.
  - On real PS3: delete audio `.arc` or XMB sound files.

---

## "The disk must be formatted"
- **What it does:** Appears after an interrupted or failed format.
  - Can be triggered by intentionally corrupting the disk format.

---

## Error Codes (e.g., 800017, 8007E21G)
- **What it means:** Usually due to missing RAP licenses, broken HEN activation, or corrupted CFW.
  - Severity depends on the specific code.

---

## Boot Loop
- **What it does:** The system cannot fully boot and keeps restarting.
  - On RPCS3: delete all files except `vsh.self`.
  - On real PS3: corrupt `dev_flash` files that load early system modules.

---

## System Freezing
- **What it does:** Caused by RAM or CPU overload.
  - Can also be triggered by buggy plugins like `PS3xPAD` on modded systems.

---

## Incompatible Data
- **What it does:** Happens when inserting a PS2 disc into a non-backward-compatible model (CECH(D–K)).

---

## Disc Read Error
- **What it does:** Caused by unreadable, unknown, or damaged discs, or a failing disc reader.
  - The disc icon may not appear at all.

---

## Signed Out
- **What it does:** Happens when signing out manually or launching HEN for the first time.
  - Harmless, just an alert.

---

*Feel free to contribute or improve this list with more error cases!*
