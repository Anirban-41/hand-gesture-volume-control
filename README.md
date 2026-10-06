# project

# Hand Gesture Volume Control

A real-time **hand gesture-based volume control system** built using Python, OpenCV, MediaPipe, NumPy, and Pycaw.

The project uses a webcam to detect the user's hand and tracks the **thumb and index finger**. The distance between these two fingertips is used to control the computer's system volume.

---

## Project Overview

This project provides a touch-free way to control the Windows system volume using hand gestures.

Instead of using a keyboard or mouse, the user can:

* Move the thumb and index finger closer to decrease the volume.
* Move the thumb and index finger farther apart to increase the volume.

The webcam captures the hand movement, MediaPipe detects the hand landmarks, and Pycaw controls the Windows master volume.

---

## Features

* Real-time hand tracking
* Thumb and index finger detection
* Gesture-based volume control
* Live volume percentage display
* Visual distance indicator between fingertips
* Real-time webcam processing
* Windows system volume control

---

## Technologies Used

* **Python** – Core programming language
* **OpenCV** – Webcam capture and image processing
* **MediaPipe** – Hand landmark detection
* **NumPy** – Distance calculation and normalization
* **Pycaw** – Windows system volume control
* **Comtypes** – Windows COM interface
* **ctypes** – Interface with Windows system components

---

## How It Works

The project follows this workflow:

```text
Webcam
   ↓
Capture Video Frame
   ↓
OpenCV Processing
   ↓
MediaPipe Hand Detection
   ↓
Detect Thumb & Index Finger
   ↓
Calculate Distance
   ↓
Normalize Distance
   ↓
Map Distance to Volume
   ↓
Control Windows System Volume
```

### Hand Gesture Detection

The project uses MediaPipe to identify hand landmarks.

The coordinates of:

* **Thumb Tip**
* **Index Finger Tip**

are extracted from the detected hand.

The distance between them is calculated using the Euclidean distance formula:

```text
Distance = √((x₂ - x₁)² + (y₂ - y₁)²)
```

The distance is then normalized between a minimum and maximum range and mapped to the Windows system volume.

---

## Project Structure

```text
hand-gesture-volume-control/
│
├── hand_gesture_volume_control.py
├── requirements.txt
├── README.md
└── .gitattributes
```

---

## Requirements

* Windows OS
* Python 3.x
* Working webcam
* Speakers or headphones
* Required Python libraries

> **Note:** Pycaw uses the Windows audio system, so this project is intended for Windows.

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/hand-gesture-volume-control.git
```

### 2. Open the Project Folder

```bash
cd hand-gesture-volume-control
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Program

```bash
python hand_gesture_volume_control.py
```

---

## How to Use

1. Run the Python program.
2. Allow access to your webcam if Windows asks for permission.
3. Position your hand in front of the camera.
4. The program will detect your hand landmarks.
5. Move your thumb and index finger closer together to decrease the volume.
6. Move them farther apart to increase the volume.
7. Press **Q** to stop the program.

---

## Customization

The volume control sensitivity can be adjusted using:

```python
min_dist = 30
max_dist = 200
```

These values determine the distance range used for mapping the hand gesture to the volume level.

The MediaPipe detection and tracking confidence can also be adjusted:

```python
min_detection_confidence=0.7
min_tracking_confidence=0.7
```

---

## Future Improvements

Some possible improvements for future versions:

* Add hand gesture-based mute/unmute
* Add play/pause media controls
* Add brightness control
* Add multiple gesture commands
* Improve volume smoothing
* Add configurable gesture sensitivity
* Develop a graphical user interface
* Add support for additional operating systems

---

## Learning Outcomes

Through this project, I gained practical experience with:

* Python programming
* Computer Vision
* OpenCV
* MediaPipe hand tracking
* Real-time webcam processing
* NumPy mathematical operations
* Windows audio control using Pycaw
* Integrating multiple Python libraries into a practical application

---

## Author

**Anirban Banerjee**

B.Tech – Electronics & Communication Engineering

Interested in **Python, Data Analytics, Data Science, and AI/ML**.

---

If you found this project useful, consider giving the repository a star.

 
