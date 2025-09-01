# AirPiano 🎹

**AirPiano** lets you control MIDI piano chords in real time using hand gestures captured from your webcam.  
Each finger is mapped to a chord in the **D major scale**, enabling natural, gesture-based music performance without touching a keyboard.

---

## ✨ Features
- 🖐️ Real-time hand tracking with **cvzone**
- 🎼 Finger-to-chord mapping (D major scale)
- 🎹 MIDI output with sustain effect via **pygame.midi**
- 👏 Works with both left and right hands
- 🎶 Dynamic gesture-based music interaction

---

## 🎵 Chord Mapping (D Major Scale)

| Finger | Chord (Notes)      | Description |
|--------|--------------------|-------------|
| Thumb  | D Major (62,66,69) | D – F# – A  |
| Index  | E Minor (64,67,71) | E – G – B   |
| Middle | F# Minor (66,69,73)| F# – A – C# |
| Ring   | G Major (67,71,74) | G – B – D   |
| Pinky  | A Major (69,73,76) | A – C# – E  |

Both hands share the same mapping.

---

## ⚙️ Customization
- 🎹 **Change instrument** → update `player.set_instrument(<instrument_number>)`  
- 🎼 **Change scale/chords** → edit the `chords` dictionary  
- ⏱️ **Adjust sustain** → modify `SUSTAIN_TIME` (in seconds)  

---

## 🧠 How It Works
- **cvzone** detects hands and fingers with `HandDetector`  
- **fingersUp()** identifies raised fingers  
- **pygame.midi** triggers `note_on` / `note_off` events  
- Chords sustain briefly after release for a natural sound  

---

## 🤝 Credits
- [cvzone](https://github.com/cvzone/cvzone) – Hand detection  
- [pygame.midi](https://www.pygame.org/docs/ref/midi.html) – MIDI interface  
- [OpenCV](https://opencv.org/) – Real-time camera input  

---

## 📄 License
Licensed under the MIT License.  
