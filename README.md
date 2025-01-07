
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

## Contributing

Contributions are welcome! If you have suggestions for improvements or encounter issues, feel free to open an issue or submit a pull request.

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
