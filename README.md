# 🚗 Driver Monitoring System (ADAS-Like)

A real-time Driver Monitoring System built using Python, OpenCV, and MediaPipe that detects driver drowsiness, microsleep, yawning, gaze direction, head-down posture, and possible phone distraction.

## 📌 Features

- 👁️ Eye Aspect Ratio (EAR) based eye closure detection
- 😴 Drowsiness detection
- 🚨 Microsleep detection with alarm
- 😮 Yawning detection using Mouth Aspect Ratio (MAR)
- 👀 Gaze tracking (Left / Right / Forward)
- 📱 Phone distraction detection
- 🙇 Head-down posture detection
- 📊 PERCLOS (Percentage of Eye Closure) calculation
- 🔔 Real-time audio alert system

## 🛠️ Technologies Used

- Python
- OpenCV
- MediaPipe Face Landmarker
- NumPy
- Winsound

## 📂 Project Structure

```text
Driver-Monitoring-System/
│
├── models/
│   └── face_landmarker.task
│
├── driver_monitoring.py
├── requirements.txt
└── README.md
```

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/driver-monitoring-system.git
cd driver-monitoring-system
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download MediaPipe Model

Download the Face Landmarker model and place it inside the `models` folder:

```
models/face_landmarker.task
```

### 4. Run the Project

```bash
python driver_monitoring.py
```

## 🎯 Detection Modules

### Drowsiness Detection
Uses Eye Aspect Ratio (EAR) and MediaPipe eye blink scores to identify prolonged eye closure.

### Microsleep Detection
Triggers when eyes remain closed beyond the defined threshold.

### Yawning Detection
Uses Mouth Aspect Ratio (MAR) to detect yawning behavior.

### Gaze Tracking
Tracks iris position to determine:
- Looking Left
- Looking Right
- Looking Forward

### Head Pose Monitoring
Detects head-down posture, which may indicate distraction.

### Phone Distraction Detection
Combines head-down posture and gaze direction to estimate phone usage while driving.

### PERCLOS Monitoring
Calculates the percentage of time the driver's eyes remain closed.

## 📸 Output

The system displays:

- EAR Score
- MAR Score
- PERCLOS %
- Eye Closed Duration
- Gaze Direction
- Driver State (Normal / Drowsy / Microsleep)
- Warning Messages

## 🚨 Alert System

An audible alarm is triggered when:
- Driver becomes drowsy
- Microsleep is detected

## 🔮 Future Improvements

- Head pose estimation using 3D facial landmarks
- Mobile phone object detection using YOLO
- Driver identity verification
- Dashboard for analytics and reports
- Cloud-based monitoring

## 👨‍💻 Author

Tejaswi Kolluri

## 📄 License

This project is developed for educational and research purposes.
