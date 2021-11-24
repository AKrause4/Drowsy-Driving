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
* In a terminal, open rc.local to modify: sudo nano /etc/rc.local
* Add before exit 0: python3 /home/pi/YOUR_LOCATION/detect_sleep.py &
* Save and reboot
