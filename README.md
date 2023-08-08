# Real-Time Face Tracking and Filters

This repository contains a face tracking and filtering application using TensorFlow.js and the Face Landmarks Detection model. The application captures webcam video, detects facial landmarks, and applies filters to the face in real time. It also allows users to take and view captured photos with filters.

## Files

1. *index.html*: The main page that provides an interface to open the face tracking and filtering application.

2. *1-facetracking.html*: The face tracking and filtering application page. It uses TensorFlow.js to perform real-time face tracking and display filters.

3. *third_page.html*: The captured photo display page. It shows the photo taken using the application along with applied filters.

4. *triangle.js*: A JavaScript file containing an array representing triangles for facial landmarks.

## Usage

1. Open `index.html` to access the application.

2. Click the "open camera" button to access the face tracking and filtering application.

3. In the face tracking and filtering application:
   - The webcam stream is used to detect facial landmarks.
   - Filters are applied to the detected facial features in real time.
   - Click the "Take a Photo" button to capture a photo with applied filters.

4. The captured photo can be viewed in the `third_page.html` page.
   - The photo is displayed along with the applied filters.

## How It Works

1. *index.html*: Provides an entry point to the application. Clicking the "open camera" button redirects to the face tracking and filtering application.

2. *1-facetracking.html*: The main application page where face tracking and filtering occur.
   - The webcam stream is accessed using `navigator.mediaDevices.getUserMedia`.
   - The Face Landmarks Detection model from TensorFlow.js is loaded and used to estimate facial landmarks.
   - Facial landmarks are used to draw bounding boxes and apply filters to the detected face.
   - Clicking the "Take a Photo" button captures the photo data and redirects to the `third_page.html` page.

3. *third_page.html*: Displays the captured photo with applied filters.
   - The photo data is retrieved from localStorage.
   - The photo is displayed using an `<img>` element.

## Dependencies

- [TensorFlow.js](https://www.tensorflow.org/js): A JavaScript library for running machine learning models in the browser.
- [face-landmarks-detection](https://github.com/tensorflow/tfjs-models/tree/master/face-landmarks-detection): A TensorFlow.js package for detecting facial landmarks.
