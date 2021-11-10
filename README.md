# KinectMaxWeki

In a predefined space, the user can activate 2 samples, each with a hand gesture, and control audio effects that are triggered when the user sits in 3 certain spots.

This program uses input from a Kinect CHOP and extracts 5 types of data from the skeleton - forearms X and Y pos of both hands of a user and the full body's position on the X axis. This info is remapped and sent via OSC (port 5000) to MaxMSP. 

Max sends the info further to Wekinator on 2 ports in order to create 2 models, one with classification, the other with DTW: 
- on 6448 - classification - define 3 classes using 1 input (body's posX) to determine 3 different positions on the X axis of this predefined space (left, middle, right)
- on 6449 - use DTW and send 4 inputs (forearms data) to create 2 similar hand gestures, one by moving the left arm up and down, the other using the right arm.

# Video demo
https://youtu.be/2owoZz5Ew4M
