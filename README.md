# Hand Gesture Puppet
This is an in progress Hand Gesture control project. It uses computer vision to detect hand gestures through the camera webcam. The detected gestures are sent to a microcontroller in which I am puppeteering a 3D printed hand that I am designing. This project can be implemented to puppeteer anything. I am using a GitHub repository originally from Kazuhito Takahashi, and translated by Nikita Kiselov which consists of the base code that maps and reads the hand gestures. The code altered is directly in the app.py file, commented depicting the arduino connection.

# How It Works
After downloading this repo and necessary libraries, upload the ardiuno code to the microcontroller and servos as desired. Then close the arduino IDE and open the app.py and run the code. Note that you need to have an available webcam on your laptop/computer. The camera runs normally around 30 FPS for me before a hand enters the view. Once a Hand enters the view, the FPS drops to around 1.5 as it constantly sends the arduino updated data (I plan on improving this). Then it detects whether your hand is open, closed or whatver gesture you want to train and move the arduino accordingly. Right now the Arduino code is hardcoded and only changes to specific positions coded in. I plan on improving this aspect as well.

# Troubleshoot
Download: Tensorflow, Mediapipe
Different port: Check what port your microcontroller is connected to
Module not found: Change the interpreter on your IDE
Port Busy: Close the arduino IDE while using the python script and vice versa

# Reference
* [MediaPipe](https://mediapipe.dev/)

# Original Repo Author
Kazuhito Takahashi(https://twitter.com/KzhtTkhs)

# Translation and other improvements
Nikita Kiselov(https://github.com/kinivi)
 
# License 
hand-gesture-recognition-using-mediapipe is under [Apache v2 license](LICENSE).
