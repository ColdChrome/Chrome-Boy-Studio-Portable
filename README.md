<img width="512" height="512" alt="card" src="https://github.com/user-attachments/assets/174b4bfd-678b-46ee-ac38-12a2a003e6c8" />
# Chrome Boy Studio Portable v0.9

**Custom firmware for the M-VAVE FM1** 

Chrome Boy turns the FM1 into a pocket groovebox that is playful, a little chaotic and still experimental. It boots straight into a pattern. Turn one knob to get new grooves, or pull random chord progressions until something sticks.

> ⚠️ **Experimental firmware.** Expect rough edges, and back up your FM1 before installing. We're still working on bug fixes, quality-of-life features, better export and more MIDI options.



---

## Contents

1. [Try it in your browser](#1-try-it-in-your-browser)
2. [Install it on your FM1](#2-install-it-on-your-fm1)
3. [Quick start](#3-quick-start)
4. [Pages and controls](#4-pages-and-controls)
5. [Exporting stems to your DAW](#5-exporting-stems-to-your-daw)
6. [Known bugs and limitations](#6-known-bugs-and-limitations)
7. [Going back to an older version](#7-going-back-to-an-older-version)
8. [Credits](#8-credits)
9. [Building from source](#9-building-from-source)
10. [Licence](#10-licence)

---

## 1. Try it in your browser

You can play Chrome Boy in a browser before installing it on hardware, using the FM-1 emulator.

www.coldchrome.la/pages/chrome-boy-studio-portable-emulator

- Open the Chrome Boy emulator page and click **Start**.
- Or open the [FM-1 Emulator](https://github.com/joakimeriksson/fm1-emu) and drop the `.fwsc` from the [Releases](../../releases) page onto it.

**Emulator keys**

| Key | Does |
|---|---|
| `A` … `'` | Play notes from C4 |
| `Z` / `X` | OCT− / OCT+ |
| `Space` | PLAY |
| `←` `→` | SELECT knob (change track) |
| `,` `.` | ALGORITHM knob (new generated pattern) |
| `1` – `0` | FX, SCL, ENV, LFO, EDIT, GLO, HOME, SAVE, ARP, SEQ |
| `R` | REC |
| Mouse | Drag or scroll any knob on the picture; click keys and buttons |

**Emulator tips**
- If a quick key press is missed, hold the key for a moment.
- Computer keys start at C4, so the three lowest drum keys (kick, closed hat, open hat) need the mouse. On a real FM1, all keys work.
- The emulator starts with a fresh project, not your FM1's saved state.
- MIDI input works in Chrome and Edge only.

---

## 2. Install it on your FM1

**You need:**
- An M-VAVE FM1 and a USB cable.
- **Chrome or Edge on a computer.** Installing uses Web MIDI, which Safari, Firefox and phones don't support.
- One of the following on your FM1:
  - M-VAVE's open firmware.
  - An earlier Chrome Boy build.
  - M-VAVE stock firmware **V15**. If you have an older stock version, update it to V15 with M-VAVE's own updater first.

**Before you start: back up your FM1.** Save or export anything you want to keep, because installing can replace your patches and projects.

**Steps**
1. Plug in the FM1 and close any other app that uses it, such as a DAW or M-VAVE's editor.
2. Open Chrome Boy's card on [thefirmwarehub.com](https://thefirmwarehub.com) and use its install button, or open the **Install Chrome Boy** page.
3. Click **1 · Connect** and allow MIDI access when Chrome asks.
4. **If you're on stock V15:**
   1. Read the note.
   2. Tick **"I've backed up"**.
   3. Click **Reconnect for the stock install**.
5. Click **2 · Install** and wait for **DONE**. Don't unplug the FM1 or close the tab while it installs.
6. The FM1 restarts into Chrome Boy and shows **CHROME BOY STUDIO PORTABLE V0.9**.

If the page says **STOP … Not flashing**, it didn't recognise the firmware on your FM1, so it left the FM1 untouched.

> The install over stock V15 uses M-VAVE's own update route, but it is the newest and least-tested path. If something goes wrong, M-VAVE's updater can put stock firmware back.

---

## 3. Quick start

1. Power on. Chrome Boy boots to the **HOME** screen with a pattern ready.
2. Press **PLAY**.
3. Use the **SELECT** knob (← →) to choose a track: drums, bass, lead, E.PNO, bell, pad, organ and more.
4. Turn **ALGORITHM** to generate a new pattern for that track. The 128 positions are split into 4 tiers of complexity:
   - **1** foundational: triads, diatonic notes, plain rhythms.
   - **2** colour: sus chords, 7ths, gentle syncopation.
   - **3** complex: 9ths, borrowed chords, more hits and accents.
   - **4** experimental: tritone substitutions, chromatic approach notes, wide dynamics.
5. Open **SEQ** and press any white key for a **lottery pull**: a new chord progression and a new pattern from the same tier. Keep pulling until something lands.
6. Press **SAVE**, name the project (K1 picks the character, K2 moves the cursor), then press **SAVE** again to write it. **PLAY** cancels.

---

## 4. Pages and controls

| Button | Page |
|---|---|
| HOME | Overview of the tracks and the pattern |
| FX | Master FX rack (time-based, modulation, drive and filter effects) |
| SCL | Scale and key |
| ENV | Envelope |
| LFO | LFO routing |
| EDIT | Piano roll and step edit |
| GLO | Global settings |
| SAVE | Save and load projects, and **Export to DAW** |
| ARP | Arpeggiator |
| SEQ | Sequencer and lottery pulls |
| PRESETS | Voices for the current track |

**Hold HOME** to open **SYSTEM NAV**, which has the Step Matrix, Mixer, Piano Roll, Step Edit, Global, SEQ, FX Rack, Save and Clear project.

**Drums:** the drum track has 808 and 909 modes and genre grooves (HOUSE, 4/4 SYNC, MIAMI, ELECTRO, DETROIT, BREAKS, TRAP, DNB, HALF). Each pull shifts the hats and toms against the groove, so the same groove gets a new feel.

---

## 5. Exporting stems to your DAW

Chrome Boy plays each track one at a time so you can record them as separate stems.

1. Connect the FM1 to your computer over USB. It shows up as a stereo audio input ("USB-Audio" on a Mac).
2. In your DAW, arm a track that records from the FM1 and start recording.
3. On the FM1, open **SAVE** and choose **EXPORT TO DAW**.
4. Press **3** to switch the tail mode:
   - **TAIL RING** (default): notes ring out into the silent gap between stems.
   - **TAIL CUT**: notes stop at the barline, so each stem is exactly your loop length.
5. Press **1** to start, or **2** to cancel.

Each stem starts after a 4-second lead-in, plays one loop, and stops on the barline. The count-in is switched off during export and turned back on afterwards. The FM1 can't trim the audio in your DAW, so line the stems up from the first hit.

---

## 6. Known bugs and limitations

Chrome Boy is still in development. These issues are known and being worked on:

**Bugs**
Applying a new variation on one track will change other tracks too. Planning to make this a toggle in final release.
- **The export (save stems) screen stays on after the export finishes.** The stems are recorded correctly, but the screen doesn't close by itself. Try pressing **HOME** or another page button to leave it. If it won't clear, save first if you can, then power-cycle the FM1. Your saved projects aren't affected.
- **The mixer has visual glitches.** Meters, labels or values on the MIXER page can draw incorrectly or overlap. The levels themselves still work. The fix is in progress.
- **Quick button presses are sometimes missed in the emulator.** Hold the button for a moment. This happens in the emulator only.
- **The ALGORITHM knob on drums froze the emulator in 3.10.0 – 3.10.2.** This is fixed in 3.10.3. If you're on an older build, update.

**Limitations**
- The screen font only has capital letters, so voice names show in caps (e.g. "ORGAN 2").
- Choosing a preset on a PSG chip track, like the default E.PNO, switches it to an FM voice, which replaces the chip sound on that track.
- The 303 and pluck tracks have only 3 presets each, and PSG tracks have none. Flash space is very tight (453,896 of 453,921 bytes used).
- The 909 mode is as deep as M-VAVE's closed 808 drum engine allows.
- Export is one stereo stem at a time. Multichannel USB audio would need changes in M-VAVE's closed SDK.
- Cue lines only appear on the export prompt and the save naming screen.

**Coming next**
- Bug fixes and stability (the export screen, the mixer visuals).
- Quality-of-life improvements across the menus and controls.
- Better export options.
- More MIDI options.

**Found something?** Send a note with your Chrome Boy version (shown at boot), what you pressed, and what happened. That helps a lot.

---

## 7. Going back to an older version

Every version is kept on the [Releases](../../releases) page. Install an older `.fwsc` the same way as a new one.

To go back to M-VAVE firmware, use M-VAVE's own updater.

---

## 8. Credits

- **Chrome Boy Studio Portable** is an independent project built on M-VAVE's open FM1 SDK. It is **not made by or affiliated with M-VAVE**.
- **FM-1 Emulator** by Joakim Eriksson, MIT licence: github.com/joakimeriksson/fm1-emu
- **WebUpdate.js** (the installer library) by M-VAVE, GPL-3.0 with linking exception.

Use at your own risk. Back up first, and have fun breaking things (musically).

---

## 9. Building from source

This repository is M-VAVE's [FM1 Open](https://github.com/m-vave/fm1_open) kit with Chrome Boy's changes on top. M-VAVE's original README, with its build steps, is in [`README.FM1_OPEN.md`](README.FM1_OPEN.md).

**Chrome Boy's own code:**
- `app/cb/`: the groovebox (sequencer, pattern generator, screens, FX rack).
- `app/audio_output.c`, `app/presets.c`, `app/project.c`: changed from M-VAVE's versions.
- `app/version.h`: Chrome Boy's device ID, `FM-1_8230090`.
- `tools/Build-Mac.ps1`: a macOS build that runs JieLi's Windows toolchain through Wine.

**Building:**
- **Windows:** follow [`README.FM1_OPEN.md`](README.FM1_OPEN.md) (`build.bat`).
- **macOS:** run `tools/Build-Mac.ps1 -FirmwareOnly` with PowerShell, with `FM1_WINE` set to your Wine binary and `-Toolchain` pointing at the JieLi `pi32` toolchain.

The firmware is written to `build/dx7/generated/FM1_OFFICIAL_OPEN.fwsc`. The FM1 has room for 453,921 bytes, and Chrome Boy uses nearly all of it.

## 10. Licence

Chrome Boy's code is GPL-3.0 with M-VAVE's FM1 SDK linking exception, the same as FM1 Open. See [`LICENSE.md`](LICENSE.md). The FM1 sound engine is M-VAVE's closed binary SDK under its own terms, in [`THIRD_PARTY.md`](THIRD_PARTY.md). Keep both files with any build you share.

