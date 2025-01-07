
# Facial Emotion Recognition using OpenCV and DeepFace

This project uses **OpenCV** for face detection and **DeepFace** for emotion classification based on facial expressions. The system is capable of detecting and classifying emotions such as happiness, sadness, anger, surprise, fear, and disgust.

## Features
- Real-time emotion detection using the webcam.
- Classification of emotions into multiple categories.
- Use of **OpenCV** for face detection and **DeepFace** for emotion analysis.
- Supports static images and real-time video streaming.

## Requirements

To run this project, you need the following libraries:

- Python 3.6+
- OpenCV
- DeepFace
- numpy
- matplotlib

### Installing Dependencies

You can install the necessary dependencies by running:

```bash
pip install opencv-python deepface numpy matplotlib
```

## Setup and Usage

### Step 1: Clone the Repository

Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/your-username/Facial-Emotion-Recognition-using-OpenCV-and-DeepFace.git
cd Facial-Emotion-Recognition-using-OpenCV-and-DeepFace
```

### Step 2: Run the Emotion Recognition Script

To run the emotion recognition system using your webcam, execute the following Python script:

```bash
python emotion_recognition.py
```

This will start capturing the webcam feed and detect emotions in real-time.

### Step 3: Test with Static Images

You can also test emotion recognition with static images. To classify emotions from an image, run:

```bash
python predict_image.py --image path_to_image.jpg
```

Replace `path_to_image.jpg` with the path to the image you want to test.

## Code Overview

### 1. **Face Detection:**

OpenCV is used to detect faces in the input image or video frame.

### 2. **Emotion Classification:**

DeepFace is used to analyze the face and classify the dominant emotion based on facial expressions.

### 3. **Real-Time Webcam Feed:**

The webcam feed is captured using OpenCV, and DeepFace processes each frame to detect emotions.

### Example Code:

```python
import cv2
from deepface import DeepFace

# Start video capture
cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()
    if not ret:
        break
    
    # Analyze the frame for emotion
    result = DeepFace.analyze(frame, actions=['emotion'])
    
    # Get the dominant emotion
    dominant_emotion = result[0]['dominant_emotion']
    
    # Display the emotion on the frame
    cv2.putText(frame, dominant_emotion, (50, 50), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 255, 0), 2, cv2.LINE_AA)
    
    # Show the frame with emotion displayed
    cv2.imshow('Emotion Recognition', frame)
    
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

## Contributing

Contributions are welcome! If you have suggestions for improvements or encounter issues, feel free to open an issue or submit a pull request.

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
