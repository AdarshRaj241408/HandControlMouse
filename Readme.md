# Hand Control Mouse

This project allows you to control your computer's mouse using hand gestures detected through a webcam. It uses OpenCV for image processing, MediaPipe for hand tracking, and PyAutoGUI for controlling the mouse.

## Features
- Tracks your hand using a webcam.
- Moves the cursor when one index finger is up.
- Performs a left-click when both index and middle fingers are up, and the distance between them is small.
- Easily extendable to include additional mouse actions using PyAutoGUI.

## Installation

### 1. Create a Virtual Environment
It is recommended to run this project inside a virtual environment.

```bash
python3 -m venv venv
source venv/bin/activate   # For Linux/macOS
venv\Scripts\activate     # For Windows
```

### 2. Install Dependencies

```bash
pip install opencv-python numpy mediapipe pyautogui
```

## Running the Project

### Linux Users
**Ensure you are using Xorg, as Wayland may cause issues.** To switch to Xorg, log out and choose **Xorg** from the login screen options.

Start the project with:
```bash
python AiVirtualMouse.py
```

### Windows Users
For Windows, additional configuration may be needed to ensure compatibility with PyAutoGUI.

## How It Works
- The webcam detects your hand and tracks key points using **MediaPipe**.
- If **only the index finger is up**, the cursor moves accordingly.
- If **both the index and middle fingers are up**, the script calculates the distance between them:
  - If the distance is small, a **left click** is performed.
- Users can modify and add more gesture-based controls using PyAutoGUI commands.

## Future Improvements
- Adding Windows compatibility.
- More hand gesture-based controls (right-click, scroll, drag, etc.).

Enjoy experimenting with gesture-based control! 🚀