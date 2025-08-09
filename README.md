# PyFingerLED

**PyFingerLED** is a Python-based hand gesture recognition system that controls an Arduino-powered LED array in real time.  
Using computer vision and a webcam, it detects the number of raised fingers and lights up corresponding LEDs — creating an interactive light display.

---

## ✨ Key Features
- **Real-Time Gesture Detection** – Uses OpenCV and MediaPipe (`cvzone.HandTrackingModule`) for precise hand tracking.
- **Arduino-Powered LEDs** – Controls up to 5 LEDs via Arduino and `pyFirmata`, matching finger positions.
- **Python + Arduino Synergy** – Combines computer vision with hardware control seamlessly.
- **On-Screen Feedback** – Displays finger count and LED status in a live OpenCV window.
- **Scalable Design** – Can be extended to motors, servos, or IoT devices.

---

## 🛠 How It Works
1. **Hand Detection** – Webcam feed is processed with a pre-trained ML model to detect hand landmarks.
2. **Finger Counting** – Identifies which fingers are raised (e.g., `[0,1,1,0,0]` = 2 fingers).
3. **LED Control** – Sends commands to Arduino via USB (COM3) to light up LEDs accordingly.
4. **Visual Feedback** – Shows finger count and LED states directly on the OpenCV output window.

---

## 📊 Demo Example

| Gesture      | LEDs Lit       | Python Output |
|--------------|---------------|--------------|
| ✊ (Fist)     | None          | `[0,0,0,0,0]` |
| ☝️ (Index)   | LED 1         | `[0,1,0,0,0]` |
| ✌️ (Two)     | LEDs 1 & 2    | `[0,1,1,0,0]` |
| 🤟 (Three)   | LEDs 1–3      | `[0,1,1,1,0]` |
| 🖐️ (Five)   | All LEDs      | `[1,1,1,1,1]` |

---

## 🚀 Potential Upgrades
- **Wireless Control** – Replace USB with Bluetooth or Wi-Fi (ESP32).
- **Brightness Control** – Use PWM to adjust LED brightness based on finger angle.
- **Robotics** – Control a robotic arm or drone with gestures.
- **Smart Home** – Trigger IoT devices like lights and fans via gestures.

---

## 🎯 Why It’s Cool
- **No extra hardware** – Just a webcam + Arduino.
- **Beginner-friendly** – Learn computer vision, Arduino, and Python in one project.
- **Fully customizable** – Add voice control, animations, or multi-hand support.

---

## 💡 Ideal For
- Makers & STEM educators
- Arduino/Python beginners
- Rapid prototyping of gesture-controlled systems
