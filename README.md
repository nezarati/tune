# Tune

**🌐 Live demo: <https://nezarati.github.io/tune/>**  ·  **⭐ Source: <https://github.com/nezarati/tune>**

[![Live demo](https://img.shields.io/badge/live%20demo-nezarati.github.io%2Ftune-38bdf8?style=for-the-badge)](https://nezarati.github.io/tune/)
[![GitHub repo](https://img.shields.io/badge/github-nezarati%2Ftune-181717?style=for-the-badge&logo=github)](https://github.com/nezarati/tune)
[![License: MIT](https://img.shields.io/badge/license-MIT-2ea44f?style=for-the-badge)](LICENSE)
[![Single file](https://img.shields.io/badge/one%20HTML%20file-99%20KB-6f42c1?style=for-the-badge)](index.html)

**One file. Every tool a musician needs to stay in time and in tune.**

`Chromatic Tuner · Vocal Pitch Monitor · Metronome · Tone Generator — 100% offline, zero dependencies`



---

## Description

Tune is a professional-grade music toolkit that packs a precision chromatic tuner, a vocal pitch monitor, a full-featured metronome, and a reference tone generator into a single self-contained HTML file. Inspired by studio staples like APTuner, GuitarTuna, Pro Metronome, and Soundbrenner, it needs no install, no account, and no internet: open it in any modern browser and allow microphone access. All processing runs locally through the Web Audio API, and your audio never leaves the device. It is published free on GitHub Pages and works on desktop and mobile alike. Touch-friendly throughout, with pinch zoom and haptics.

The tuner uses the McLeod Pitch Method to lock onto fundamentals from 27.5 Hz up past 4 kHz with sub-cent accuracy, rejecting the octave errors that plague naive detectors. Results appear on a clock-style needle dial or a five-harmonic strobe, alongside an adjustable A4 (380-480 Hz), six temperaments, transposing-instrument support, and string-snapping instrument modes.

The pitch monitor draws a continuous, zoomable pitch contour with a lockable window, alpha-graded cent gridlines, and user guide lines: pin a pitch you sing, add microtonal notes, or load folk scales and maqams such as Hijaz, Bayati, and Rast - then export or import the whole setup as JSON. A sing-along coach plays a reference tone that follows your voice, holds a fixed note, or loops scale runs, with its own volume, waveform, and octave shift, scoring every take with a hold timer and accuracy percentage, while a vibrato meter reports rate and depth live.

The metronome delivers sample-accurate timing across eleven time signatures, subdivisions, tap tempo, haptics, and a speed trainer, and the tone generator covers reference pitches for every common instrument. Settings persist locally, and the entire suite ships in one ~100 KB file - ready to host, share, or carry on a USB stick.

---

## Feature Overview

### 🎛 Chromatic Tuner (APTuner-style)
- Clock-style needle gauge with LED arc, spring-damped needle, in-tune glow
- 5-harmonic **strobe display** mode (bars drift left = flat, right = sharp, still = perfect)
- Live readouts: detected Hz, target Hz, cents offset, sharp/flat verdict
- Input **level** and **clarity** meters
- **Hardware-style calibration profiles**, like real clip-on/pedal tuners: **Snark SN-1/SN-2/SN1X (415–466 Hz, 1 Hz steps — yes, exactly 416 works)**, **D'Addario NS Micro (410–480)**, **Korg CA-2/pitchblack (410–480)**, **Boss TU-3 (436–445)**, **Peterson-style strobe (400–480, 0.1 Hz)**, or full **Custom 380–480 @ 0.1 Hz** — with −/+ step buttons and out-of-range presets auto-disabled
- **A4 reference**: profile-aware slider + quick presets (415, 432, 440, 442, 466)
- **Flat & capo modes** (up to 4 flats / capo 7) shift displayed note names like hardware Guitar/Bass modes, and **needle response** is selectable (slow / medium / fast)
- **Temperaments**: Equal (12-TET), Just Intonation, Pythagorean, ¼-comma Meantone, Werckmeister III, Vallotti
- **Transposition**: Concert, B♭, E♭, F, A, D, G instruments (shows written pitch)
- Note naming: sharps, flats, or both · needle sensitivity ±20 / ±35 / ±50 cents
- Instrument modes: Chromatic, Guitar, Bass, Ukulele, Violin — with string snap & in-tune highlighting
- Input device selector for multi-mic setups

### 📈 Pitch Monitor (vocal-pitch-monitor style)
- **Continuous, smooth** pitch contour (60 Hz trail, curve-interpolated, short drop-outs auto-bridged — no steps between notes)
- **Lockable window**: pin the view to exact notes (Vocal C3–C5, Wide, Bass, Full presets — or hit **🔒 Lock** to freeze any window) so it never drifts while you sing
- **Zoom & pan, both axes**: vertical scroll / vertical pinch / −+ zoom the pitch axis (2–84 semitones); horizontal scroll, shift+scroll, the bottom time strip, horizontal pinch, or the seconds −+ buttons compress/expand the time axis (1.5–30 s of history). Drag to pan, **⌖ Re-center** snaps onto your voice; a badge warns when the pitch leaves the window
- **Cent gridlines** (10/25/50 ¢) appear automatically as you zoom in, drawn with graded transparency (no number clutter) — toggle them any time with the **Cent lines** checkbox
- **Guide lines**: switch on **✚ Add line** (toolbar) or the **“Click graph to add lines”** box in the panel below, then tap the graph to drop a line exactly where you touch; pin the pitch you're singing; add microtonal notes (note+cents or Hz); load whole folk scales & maqams (Hijaz, Bayati, Rast, Kurd, Saba, Dorian…)
- **Editable guides**: tap any guide chip to load it back into the form and save changes (note, cents, Hz, scale, label, colour); the chip's ✕ deletes one line, **🗑 Clear all** removes everything; **⬇/⬆ Export/Import config** shares the whole setup as JSON
- **Fast FFT**: 4096-point analyser with low smoothing for an instantly-reacting spectrum, plus a ~25 ms pitch-analysis cadence
- **Guide lines**: pin any pitch you sing, add exact Hz or note+cent microtone lines, or load whole **folk scales & maqams** (Hijaz, Bayati, Rast, Kurd, Saba, Dorian, pentatonics...) as labeled dashed guides in your color
- **Export / import config**: one JSON file carries guides, monitor window & zoom, A4, temperament, transposition, instrument mode, metronome and tone-gen settings - share it with your ensemble
- **Calm grid**: background note/cent/time lines are deliberately dim so your pitch trail and guides stand out
- **Auto-zoom** mode still available: glides with your voice in an adjustable window
- **Vibrato view**: ±100-cent deviation display where vibrato waveforms and ~1 Hz wobbles are directly visible
- Live **vibrato meter**: measures rate (Hz) and depth (±cents) from the last 2.5 s
- **🔊 Sing-along coach** — a full vocal trainer:
  - **Follow my voice**: reference tone glides under your pitch so you always hear the true note
  - **Fixed target note**: sing against one steady pitch (any note + octave)
  - **Scale run**: loops any scale/maqam degree-by-degree at your chosen seconds-per-note
  - Own **volume**, **waveform** (sine/triangle/square/saw) and **±1 octave shift**
  - **Hold timer** (current/best time inside the target window) and session **Accuracy %** score
  - Adjustable target window: **±10 / ±25 / ±50 ¢**, plus ↺ reset stats
- Big live readouts: frequency (Hz), note, cents · live **oscilloscope** and **spectrum analyzer**

### ⏱ Metronome (Pro Metronome / Soundbrenner style)
- Sample-accurate Web Audio scheduling (look-ahead scheduler, background-tab safe)
- Clock-style dial: beat dots, sweeping hand, beat flash (fully repainted every frame; hand parks at beat 1 when stopped, dial state resets on time-signature change)
- 20–300 BPM with ±1/±10 steppers, slider, and presets
- **Tap tempo** (auto-folds into a usable range)
- 11 time signatures: 2/4, 3/4, 4/4, 5/4, 6/4, 7/4, 3/8, 7/8, 6/8, 9/8, 12/8 (compound meters count dotted-quarter beats)
- Subdivisions: beat, 8th, triplet, 16th
- 3 synthesized sounds: Click, Wood, Beep · accent beat 1 · count-in · volume
- **Speed trainer**: auto tempo change every N bars toward a target BPM
- Tempo markings (Largo → Prestissimo)
- **Vibrate on beat** (Android haptics) and automatic **screen wake-lock** while playing

### 🎹 Tone Generator
- Playable one-octave keyboard + octave stepper, 4 waveforms, volume
- Reference presets: Guitar (Standard / Drop D / Open G), Bass, Ukulele, Violin, Cello, A4
- Follows your A4, temperament & transposition settings — tune by ear

---

## 🚀 Publishing to GitHub Pages (~2 minutes)

**Option A — no git needed (web upload):**
1. On github.com click **+ → New repository**, name it `tune`, make it **Public**, click *Create repository*.
2. On the empty repo page click **uploading an existing file** and drag in the files from this folder: `index.html`, `preview.png`, `README.md`, `LICENSE`.
3. Commit to the `main` branch.
4. Go to **Settings → Pages**, set *Source* to **Deploy from a branch**, *Branch* to **main** and folder to **/ (root)**, then **Save**.
5. After ~30 seconds your site is live at `https://nezarati.github.io/tune/` 🎉
   (Optionally replace `nezarati` in this README and add an absolute `og:url` in `index.html` for perfect link previews.)

**Option B — git command line:**
```bash
cd tune
git init -b main && git add -A
git commit -m "Tune: tuner + pitch monitor + metronome in one HTML file"
git remote add origin https://github.com/nezarati/tune.git
git push -u origin main
```
Then finish with steps 4–5 above.

> Note: `index.html` is the app itself (identical to `tune.html` plus SEO/social-preview meta tags). GitHub Pages serves it directly — no build step, no dependencies.

---

## Mobile Ready 📱

Fully responsive down to ~320 px: compact sticky tab bar, thumb-sized controls, fluid piano keyboard that fits any screen, safe-area padding for notched phones, pinch/scroll zoom on the monitor, haptic metronome beats, and a wake-lock that keeps the screen on while practicing. On iPhone/iPad, host the file over HTTPS (e.g. GitHub Pages) for microphone access; Android Chrome can open it directly.

## How to Use

1. Open `tune.html` in Chrome, Firefox, Edge, or Safari (desktop: double-click works; mobile/iOS: host over HTTPS, e.g. GitHub Pages).
2. Click **🎙 Start Mic** and grant microphone permission.
3. Play or sing — the needle, strobe, and monitor respond instantly.
4. Switch tabs for the metronome or tone generator (they work without the mic).
5. All settings are saved automatically in your browser (localStorage).

### Keyboard Shortcuts
| Key | Action |
|---|---|
| `Space` | Start/stop metronome (Metronome tab) |
| `T` | Tap tempo |
| `↑ / ↓` | ±1 BPM (`Shift` = ±10) |
| `1 – 4` | Switch tabs |

---

## Technical Notes

- **Pitch engine**: McLeod Pitch Method (NSDF) on audio decimated to 24 kHz, 4096-sample window (~170 ms), parabolic peak interpolation, median-of-3 smoothing, octave-error suppression via first-key-peak selection.
- **Verified accuracy**: 45-case automated test suite — sub-cent error on synthesized tones from 27.5 Hz (A0) to 2093 Hz (C7), correct noise/silence rejection, vibrato tolerance, temperament tables cross-checked against published cent deviations.
- **Metronome**: look-ahead scheduler (25 ms tick, 120 ms audio horizon; extended when the tab is hidden) — timing is drift-free.
- **Privacy**: microphone audio is analyzed in-memory and routed to a zero-gain sink; nothing is recorded, uploaded, or stored.
- **Size**: ~85 KB single HTML file, no external requests, works offline.

---

*Tune — inspired by APTuner (bromsaudio.com) and the best of modern tuner/metronome apps.*
