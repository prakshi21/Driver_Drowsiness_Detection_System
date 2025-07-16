
# Driver Drowsiness Detection System

A real-time system that detects driver drowsiness using facial landmark tracking and Eye Aspect Ratio (EAR) calculations. It alerts the driver with a loud alarm sound when signs of fatigue are detected, aiming to reduce accidents due to sleepiness at the wheel.

---

##  Overview

This project implements a lightweight, non-intrusive Driver Drowsiness Detection System using a standard smartphone camera and a laptop. It leverages facial landmark detection to monitor the driver's eye behavior and triggers an alert if prolonged eye closure is detected. The system is built using Python and open-source libraries like OpenCV, dlib, and simpleaudio.

---

##  Key Features

- Real-time video processing for driver eye activity monitoring
- Calculates Eye Aspect Ratio (EAR) to detect eye closure duration
- Alerts driver with a loud alarm when drowsiness is detected
- Visual feedback on screen with bounding contours and warning messages
- Works with standard laptops and mobile phone cameras
- Minimal hardware requirements and highly portable

---

##  Installation

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/driver-drowsiness-detection.git
   cd driver-drowsiness-detection
   ```

2. **Create and activate a virtual environment (optional but recommended)**  
   ```bash
   python -m venv venv
   source venv/bin/activate    # Linux/macOS
   venv\Scripts\activate       # Windows
   ```

3. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the facial landmark predictor file**  
   Download `shape_predictor_68_face_landmarks.dat` from [Dlib's model download page](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)  
   Extract and place it in the project directory.

---

##  Dependencies

- Python 3.x
- OpenCV
- Dlib
- Imutils
- SimpleAudio
- NumPy

You can install all dependencies using:
```bash
pip install opencv-python dlib imutils simpleaudio numpy
```

---

##  System Flow

1. Capture video stream from iPhone camera.
2. Detect face using Dlib's frontal face detector.
3. Extract eye landmarks using 68-point facial landmark model.
4. Calculate EAR (Eye Aspect Ratio).
5. If EAR < 0.25 for 10 consecutive frames:
   - Trigger audio alert via `simpleaudio`
   - Display “DROWSINESS ALERT!” on screen

---

##  Sample Output

- Eye contours drawn in real-time on the live video feed.
- Red text warning when drowsiness is detected.
- Loud alarm sound to alert the driver.

---

##  Testing

- Simulated various eye states: open, blinking, prolonged closure.
- Tested under different lighting conditions.
- Achieved ~15–20 FPS on standard laptop hardware.

---

##  References

- [Dlib Library](http://dlib.net/)
- [OpenCV Documentation](https://docs.opencv.org/)
- [SimpleAudio](https://simpleaudio.readthedocs.io/)
- [Imutils](https://imutils.readthedocs.io/en/latest/)
- [Python Docs](https://docs.python.org/3/)

---

## 📌 License

This project is for academic and educational purposes.
