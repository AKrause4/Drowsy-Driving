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
* cd /lib/systemd/system/
* sudo nano detect_sleep.service
* [Unit]
Description=Drowsy Driving Detection
After=multi-user.target

[Service]
Type=simple
ExecStart=/usr/bin/python3 /home/pi/detect_sleep.py
Restart=on-abort

[Install]
WantedBy=multi-user.target

* Activate service: 
sudo chmod 644 /lib/systemd/system/detect_sleep.service
chmod +x /home/pi/detect_sleep.py
sudo systemctl daemon-reload
sudo systemctl enable detect_sleep.service
sudo systemctl start detect_sleep.service
 
