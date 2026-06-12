# Hand Gesture Recognition for Robot Control

This project recognizes hand gestures from a webcam and uses them as simple
robot commands. It uses Google's MediaPipe library to get the 21 hand landmark
points, and the plan is to train a classical machine learning model (Random
Forest or SVM) on those points to classify the gesture.

Week 1 just sets up MediaPipe and shows the detected hand landmarks. The next
weeks add the dataset and the machine learning.

## How to run

Install the libraries:

    pip install mediapipe opencv-python matplotlib

Open `gesture_recognition.ipynb` and run the cells. Run `run_hand_tracking()` to
try it with your own webcam (press q to quit).
