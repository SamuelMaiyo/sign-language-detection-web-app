# sign-language-detection-web-app
This is simple web app that allows sign detection and translation to text and to speech at the click of a button.

# Hand Detection and Tracking
Mediapipe is used to track the key points on the human hand. This model precisely localizes 21 3D hand-knuckle coordinates i.e., x, y, z-axis, inside the detected hand regions.

![Sign Language extraction](https://github.com/SamuelMaiyo/sign-language-detection-web-app/blob/8f4d4ccebda39e10160840d3d58501b3713b02c5/Screenshots/OpenCV%20sign%20detection.PNG)


# Sign Extraction
After hand detection and tracking, this model is passed over the dataset. Considering the American Sign Language dataset, we have a to z alphabets. The detection model is passed over every alphabet directory containing images. The model compares the obtained landmark points with all the letters of the alphabet and determines the one with the highest probability. Once the model extracts the feature and determines the alphabet with the highest probability, the landmarks turn green

# Conversion to Text and Speech
The label with the highest probability is recognized to be the predicted label and is displayed as text in the OpenCV feed. The recognized letters and words are converted into the corresponding speech using the pyttsx3 library.

# Web application Integration
A web application is created using flask. This creates a user-friendly interface where users can be able to access the sign language translation system easily. The web application is linked with system in the back-end and with a click of a button, the system will start running and display an OpenCV window.

![Web Application](https://github.com/SamuelMaiyo/sign-language-detection-web-app/blob/3daa66dd2b6cb0d5346385194baec99f3b8a8076/Screenshots/web%20app.PNG)
