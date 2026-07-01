# Hand Gesture Recognition for Robot Control

This project recognizes hand gestures from a webcam and uses them as simple
robot commands. It uses Google's MediaPipe library to get the 21 hand landmark
points, and then trains a classical machine learning model (Random Forest and
SVM) on those points to classify the gesture.

The gestures are open_palm, fist, thumbs_up, point and peace. Each one maps to a
command: STOP, GRAB, MOVE FORWARD, TURN and SPEED UP.

The notebook does everything: gets the hand landmarks with MediaPipe, builds the
dataset, trains and compares a Random Forest and an SVM, and runs a live demo
that turns each gesture into a robot command.

## Files

- gesture_recognition.ipynb - all the code
- gestures.csv - the dataset you record with collect_data()

## How to run

Install the libraries:

    pip install mediapipe opencv-python pandas scikit-learn matplotlib seaborn joblib

First record your gestures with `collect_data()` (it saves them to gestures.csv),
then run the cells from top to bottom. At the end, run
`run_live_control()` to start the webcam demo (press q to quit).

## Results

Both models reach about 94% accuracy (5-fold cross-validation). They make the
same mistakes (fist vs thumbs_up, which differ only by the thumb), and the most
useful features are the fingertip positions.
