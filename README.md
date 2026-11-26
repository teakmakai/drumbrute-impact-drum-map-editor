# DrumBrute Impact — Drum Map Editor

A faster, scale-aware replacement for the Drum Map page in Arturia MIDI Control Center. It runs entirely in the browser: it reads your DrumBrute Impact over Web MIDI (SysEx), lets you edit all pad notes, and writes them back to the device.

## Usage

1. Close MIDI Control Center, your DAW, and anything else using the Impact's MIDI port.
2. Open `index.html` in Chrome or Edge. Opening the file directly works; so does a GitHub Pages link.
3. Allow "MIDI devices with SysEx" when the browser asks.
4. Pick the Impact as MIDI input and output, then press **Read from Impact**. A backup of the device values is saved automatically.
5. Edit notes with the scale tools, table, or keyboard, then press **Send changes**.

## Features

- Root/scale selection with lock-to-scale and 18 scales
- Spread, randomize, reverse, transpose by scale step or octave
- Color-variant notes, optionally following the main note
- Live mode (sends each edit instantly) and verify-after-send
- Automatic device backups, plus presets saved locally or exported as JSON

Only the 19 drum-map note values are ever written. The SysEx control IDs come from the open-source sysex-controls project.
