# Virtualmouse
📌 Overview
This Virtual Mouse project uses your webcam and hand gesture recognition to control the mouse pointer in real time. With Python and computer vision, it detects the movement of your index finger to move the cursor and recognizes a "click" gesture when the index finger and thumb come close together.

🧠 Features
Real-time cursor movement using your index finger

Left click detection when index finger and thumb come close

Visual feedback with on-screen tracking

Works with any standard webcam

🛠️ Technologies Used
Python 3.x

OpenCV – for capturing and processing video frames

MediaPipe – for detecting and tracking hand landmarks

PyAutoGUI – for performing mouse operations like move and click

▶️ How It Works
Accesses your webcam feed.

Detects hand landmarks using MediaPipe’s Hands module.

Moves the mouse cursor to match the position of your index finger tip (Landmark ID 8).

When the index finger tip (ID 8) and thumb tip (ID 4) come close (within 50 pixels), a left click is performed.

🎯 Gesture Mapping
Gesture	Action
Index finger up	Move cursor
Index finger & thumb close	Left click

🧪 Installation
Clone the repository

git clone https://github.com/Sonu-2843/virtualmouse.git
cd virtualmouse
Install dependencies

pip install opencv-python mediapipe pyautogui
Run the script

python virtual mouse.py

📸 Sample Output
Add an image or short screen recording of the cursor being controlled with hand gestures here.

📌 Code Snippet (Key Logic)

if id == 8:
    pyautogui.moveTo(index_x, index_y)

if id == 4 and abs(index_y - thumb_y) < 50:
    pyautogui.click()
    
🚀 Future Improvements
Add right-click and scroll gestures

Improve click stability using gesture smoothing or confirmation time

Implement multi-hand support
