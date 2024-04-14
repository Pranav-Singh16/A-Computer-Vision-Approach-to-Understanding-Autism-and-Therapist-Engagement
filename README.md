# A-Computer-Vision-Approach-to-Understanding-Autism-and-Therapist-Engagement
This project utilizes computer vision to analyze video data of children interacting with therapists during playtime. By tracking gaze patterns.
Child-Therapist Interaction Analysis - Video Prediction
This Python script performs video frame prediction using a pre-trained convolutional neural network (CNN) model. It analyzes video content by:

Extracting Frames: It reads a video and extracts frames at specified intervals.
Edge Detection: It converts frames to grayscale, applies Gaussian blurring for noise reduction, and then employs Canny edge detection to identify prominent edges.
Prediction: It converts the edge images into PyTorch tensors and feeds them into the trained CNN model for multi-class classification.
Advantages of Separate Prediction Script:

Modular Design: This script separates prediction logic from the potentially complex training process. This improves maintainability and reusability.
Efficiency: It allows you to leverage a pre-trained model without re-running the entire training pipeline for each prediction.
Scalability: This approach is scalable if you plan to deploy the model for real-time analysis or integrate it into a larger application.
Overall Workflow:

Load Video: Provide the path to the video you want to analyze.
Extract Frames: The script automatically extracts frames based on the specified interval.
Preprocess Frames: Frames are converted to grayscale, blurred, and edge detection is applied.
Prediction: The processed frames are fed into the loaded model for prediction.
Interpretation: Based on the predicted class probabilities, the script interprets various aspects of the interaction, such as:
Child's gaze direction (towards therapist or elsewhere)
Therapist's gaze direction (towards child or elsewhere)
Object interaction (ball, puzzle, or something else)
Engagement level between child and therapist
Requirements:

Python 3.x
pandas
NumPy
OpenCV (cv2)
Pillow (PIL)
PyTorch
torchvision
Instructions:

Ensure you have the required libraries installed.
Replace the placeholder paths in the script:
video_path: Path to the video you want to analyse.
/content/drive/MyDrive/Colab Notebooks/contweights.pth: Path to the weights file for the pre-trained model.
Run the script: python prediction.py

Note:

This script assumes the trained model is a CustomModel class with specific architecture and output branches. Make sure the model definition and weights file are compatible.
This README provides a clear overview of the script's functionality, advantages of using a separate prediction script, and essential instructions for running it.
