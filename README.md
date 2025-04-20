# Pose-Estimator
Pose Estimation with OpenCV & MediaPipe

I just wrapped up the initial version of a Basic Pose Estimation System using Python, OpenCV, and MediaPipe. This project captures human body landmarks in real-time through a webcam and calculates joint angles — a fundamental step toward building more advanced applications like fitness trackers, gesture-controlled interfaces, or rehab monitoring tools.

🔍 What it does:

Detects and draws key body landmarks in real time

Tracks joint positions and visualizes them

Calculates angles between joints using vector math

Displays real-time FPS for performance monitoring

🛠 Tech Stack / Libraries Used:

Python

OpenCV – for video capture and drawing

MediaPipe – for human pose estimation

Math & Time – for angle calculations and performance tracking

🔧 How It Works (Short Summary)
Video Capture:

The webcam is accessed using cv2.VideoCapture(0) to get live video feed.

Pose Detection:

MediaPipe's Pose model processes each frame to detect body landmarks (like shoulders, elbows, knees, etc.).

Landmark Drawing:

Detected body landmarks and connections are drawn using mpDraw.draw_landmarks() for visualization.

Position Extraction:

The (x, y) pixel positions of each landmark are calculated relative to the video frame dimensions.

Angle Calculation:

findAngle() takes three landmark points and computes the angle between them using trigonometry, useful for detecting joint positions or movement.

FPS Display:

Frames per second are calculated and displayed on screen to monitor performance.

Live Visualization:

The output is displayed in a real-time OpenCV window showing the person with pose landmarks, angles, and FPS overlay.







