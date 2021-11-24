# Drowsy-Driving

# Necessary libraries:
* imutils
* dlib
* opencv-python
* scipy
* espeak
# download dlib pretrained 68 point feature http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2
# if you run into 'libf77blas.so cannot be found' error: sudo apt-get install libatlas-base-dev
# if using ReSpeaker 2-mic Pi-HAT for speaker, follow directions here https://github.com/respeaker/seeed-voicecard and set Raspberry Pi speaker to seeed-2mic-voicecard
# To have the program run at startup:
* in a terminal: sudo nano /etc/profile
* add at the end: python3 /home/pi/detect_sleep.py &
* then save, close, and reboot 
 
