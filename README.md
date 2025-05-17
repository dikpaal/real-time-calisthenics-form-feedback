# 🏋🏻‍♀️ Real-Time Squat Form Feedback System

This project provides real-time feedback on squat form using a pre-trained pose estimation model (`.tflite`), OpenCV for video capture and rendering, and TensorFlow for inference. The model evaluates key joint angles and provides feedback to help users correct their squat technique.

## 🚀 Features

- Detects key body points from video using TensorFlow Lite pose estimation
- Calculates angles at hips and knees
- Provides real-time feedback on squat depth and symmetry
- Highlights common form issues like:
  - Not squatting low enough
  - Knees caving in
  - Asymmetrical posture

## 🧠 Key Concepts

- **Pose Estimation**: TensorFlow Lite model outputs 17 key body points with confidence scores.
- **Joint Angle Calculation**: Angles at the knee and hip joints are computed using vector math and cosine rule.
- **Form Feedback Logic**:
  - Good form is identified by correct hip and knee angles and symmetry.
  - Multiple repetitions of the same error trigger displayed feedback.

## 🛠️ Dependencies

Install via `pip`:
```bash
pip install tensorflow numpy opencv-python matplotlib
▶️ Usage

- Replace squat_11.mp4 with your own video or use cv2.VideoCapture(0) for webcam.

Run the main script:

python squat_form.py
Press q to quit the video window.

📈 Example Feedback
"Squat lower"

"Keep your knees out."

"Ensure both sides move symmetrically"

"Good form!"

🧑‍💻 Author
Dikpaal Patel

