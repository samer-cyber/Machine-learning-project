# Hand Gesture Recognition for Robot Control

The objective is to build a classification model that identifies real-time human hand gestures (e.g., stop, point, thumbs up) to act as simulated command inputs.

To keep the scope realistic and appropriate, I plan to handle the computer vision step by using a pre-trained library (like Google's MediaPipe) strictly to extract 3D spatial hand landmarks. The core machine learning component of the project will focus entirely on taking those extracted coordinate datasets and training a classical algorithm—such as a Random Forest or Support Vector Machine (SVM)—to classify the gesture states.