# DrumBrute Impact — Drum Map Editor

A faster, scale-aware replacement for the Drum Map page in Arturia MIDI Control Center. It runs entirely in the browser: it reads your DrumBrute Impact over Web MIDI (SysEx), lets you edit all pad notes, and writes them back to the device.

## Usage

1. Close MIDI Control Center, your DAW, and anything else using the Impact's MIDI port.
2. Open https://teakmakai.github.io/drumbrute-impact-drum-map-editor/ in Chrome or Edge (or open `index.html` directly).
3. Allow "MIDI devices with SysEx" when the browser asks.
4. Pick the Impact as MIDI input and output, then press **Read from Impact**. A backup of the device values is saved automatically.
5. Edit notes with the scale tools, table, or keyboard, then press **Send changes**.

## Features

- Root/scale selection with lock-to-scale and 18 scales
- Automatic scale layout: choosing a root or scale puts the root on the Kick, the other pads on the next notes of the scale, and the color variants on the notes after that, so no two sounds share a note
- Warning when two sounds share a note
- Spread, randomize, reverse, transpose by scale step or octave
- Color-variant notes, optionally following the main note
- Mute button for each send (moves it to a spare note you choose, since the Impact can't switch a pad's MIDI output off)
- Live mode that only sends the notes that changed, optionally landing key changes on the next beat or bar using the Impact's MIDI clock
- Verify-after-send
- Automatic device backups, plus presets saved locally or exported as JSON

Only the 19 drum-map note values are ever written. The SysEx control IDs come from the open-source sysex-controls project.
