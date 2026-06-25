# Hand Gesture Recognition for Robot Control

This project recognizes hand gestures from a webcam and uses them as simple
robot commands. It uses Google's MediaPipe library to get the 21 hand landmark
points, and then trains a classical machine learning model (Random Forest or
SVM) on those points to classify the gesture.

The gestures are: open_palm, fist, thumbs_up, point and peace.

Week 3 adds the machine learning. The notebook normalizes the landmarks, trains
a Random Forest, and checks it with a confusion matrix and cross-validation.

## Files

- gesture_recognition.ipynb - all the code (landmarks, dataset, training)
- gestures.csv - the dataset you record with collect_data()

## How to run

Install the libraries:

    pip install mediapipe opencv-python pandas scikit-learn matplotlib seaborn joblib

First record some gestures with `collect_data()` (it saves them to gestures.csv),
then run the cells from top to bottom.

## Results

The Random Forest gets about 97% accuracy (5-fold cross-validation). Most of the
mistakes are between fist and thumbs_up, which only differ by the thumb.
