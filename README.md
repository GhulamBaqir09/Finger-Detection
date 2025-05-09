# Finger-Detection
# Smart Proctor - Finger Movement Detection System

This project is a real-time hand tracking and gesture monitoring tool built using Python, OpenCV, and MediaPipe. It is designed for smart proctoring scenarios such as online tests or exams, where hand and finger movement monitoring is crucial to maintain integrity.

## Features

### 1. Real-Time Hand Tracking
- Utilizes MediaPipe Hands to detect and track up to two hands simultaneously via the webcam.
- Draws hand landmarks and connections for visual feedback.

### 2. Finger Tip Detection
- Highlights fingertips using circles for better visibility.
- Detects fingers based on specific landmark indices (4, 8, 12, 16, 20).

### 3. Finger Counting
- Determines how many fingers are raised.
- Increments a count of fingers that are up, including special logic for the thumb.

### 4. Hand Movement Monitoring
- Tracks the movement of finger tips across frames.
- Calculates total movement of the hand based on Euclidean distance.
- Displays movement as a percentage (0% to 100%) on screen.

### 5. Suspicious Activity Detection
- Flags suspicious behavior if movement exceeds a defined threshold (e.g., 60%).
- Also flags if 4 or more fingers are detected as raised.
- If suspicious behavior persists for more than 2 seconds, it triggers warnings.

### 6. Warning System
- First, second, and third warnings are shown based on repeated suspicious behavior.
- Displays warnings as text overlays on the video feed.

### 7. Automatic Paper Cancellation
- After 4 warnings, the system declares the paper as canceled.
- Shows a message: "Paper Canceled! Suspicious Activity Detected" and "Recording Stopped".
- **Automatically stops the webcam recording and exits the program.**

## Requirements

- Python 3.7+
- OpenCV
- MediaPipe
- NumPy

You can install dependencies using:

```bash
pip install opencv-python mediapipe numpy
Usage
Run the script with:

python fingermovement.py
The webcam will open and start tracking hand gestures. The program will provide real-time feedback and flag suspicious activity based on finger positions and movement.

File Description
fingermovement.py — Main Python script implementing the full functionality of hand tracking, finger monitoring, and proctoring logic.

License
This project is for educational and academic use only. All rights reserved.

Let me know if you’d like a version with setup instructions or contribution guidelines as well.
