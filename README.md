# Hand Gesture Recognition for Robot Control

This project recognizes hand gestures from a webcam and uses them as simple
robot commands. It uses Google's MediaPipe library to get the 21 hand landmark
points, and then trains a classical machine learning model (Random Forest or
SVM) on those points to classify the gesture.

The gestures are: open_palm, fist, thumbs_up, point and peace.

`collect_data()` lets you record your own gestures from the
webcam into gestures.csv.

## Files

- gesture_recognition.ipynb - the code so far (landmarks + dataset)
- gestures.csv - the data (21 landmark coordinates + gesture label)

## How to run

Install the libraries:

    pip install mediapipe opencv-python pandas matplotlib

Open the notebook and run the cells. Run `collect_data()` to record your own data.
