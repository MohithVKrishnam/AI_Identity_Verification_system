# AI Identity Verification System

## Overview

The **AI Identity Verification System** is a facial recognition-based security system designed to verify the identity of users in a workspace. It captures and stores face images, then compares real-time captured faces with the stored database for identity verification.

This system uses **YOLOv8** for face detection and **Face Recognition** library to compare the detected faces with known faces in the database. It provides features such as:

- **User Registration**: Capture and store user details along with their face images.
- **Real-Time Detection**: Detect and verify faces in real-time.
- **Identity Verification**: Compare detected faces with stored faces to verify identity.
- **Secure Logging**: The system logs the first and last detected time of each user.

## Features

- **User Registration**: Capture face images and store them with the user's details (name, age, branch).
- **Live Face Detection**: Detect faces using YOLOv8 and verify them using facial recognition.
- **Display User Details**: Show the name, first detected time, last detected time, and confidence score when a match is found.
- **Exit Button**: An exit button to close the application gracefully.
- **Full-Screen Interface**: The GUI provides a clean and modern full-screen interface with easy-to-use buttons.

## Installation

### Prerequisites

Before running the project, make sure you have the following installed:

- Python 3.x
- Libraries:
  - `opencv-python`
  - `tkinter`
  - `Pillow`
  - `ultralytics`
  - `face_recognition`
  - `sqlite3`
  - `numpy`
  
You can install these dependencies using `pip`:

```bash
pip install opencv-python pillow ultralytics face_recognition numpy
```

### Database Setup

The application uses **SQLite** to store user details. The database and necessary tables will be created automatically when you run the program.

## Usage

### Step 1: Launch the Login Page

- When you first launch the program, you will see a **Login page**.
- Enter the **Username** and **Password** to proceed (default credentials: `admin` / `password`).
- You can also exit the application by clicking the **Exit** button.

### Step 2: Register Users

- After logging in, you will be taken to the **Main page**.
- Here, you can enter the **name**, **age**, and **branch** of the user and click **Capture Image** to register a new user.
- The system will capture the user's face using the webcam and store the image along with the user details in the **datasets** folder.

### Step 3: Start Real-Time Detection

- On the **Main page**, click **Start Live Detection** to begin real-time face recognition.
- The system will display detected faces with the user's name, first and last detected times, and the confidence score.
- If the system detects a previously registered face, it will update the **last detected time**.

### Step 4: Exit the Application

- You can exit the application anytime by clicking the **Exit** button in either the login or main window.

## Folder Structure

```
AI_Identity_Verification/
│
├── datasets/                # Folder where captured user images are stored
├── background-image.jpg     # Background image for GUI
├── metadata.json            # Stores metadata (name, age, branch) of registered users
└── main.py                  # Main Python file to run the application
```

## How it Works

1. **Face Detection**: YOLOv8 is used to detect faces in real-time. Once a face is detected, the system extracts the face encoding.
2. **Face Recognition**: The system compares the detected face encoding with stored face encodings using the **face_recognition** library.
3. **User Verification**: If a match is found, the system displays the user's name and the first/last detected times.
4. **Logging**: The first time a user is detected, the system logs the detection time. Every subsequent detection updates the **last detected time**.

## Contributing

If you would like to contribute to this project, feel free to fork the repository, make improvements, and create pull requests.

## License

This project is open-source and available under the MIT License.
Credits
**YOLOv8** (You Only Look Once) is a state-of-the-art, real-time object detection system. The model is utilized in this project for face detection.

Citation for YOLOv8:

YOLOv8 (Ultralytics): The YOLOv8 model is developed by Ultralytics. It is an improved version of the original YOLO architecture, providing faster and more accurate object detection.
For more details, check the official YOLOv8 repository.
Original YOLO Paper:

Redmon, J., Divvala, S., Girshick, R., & Farhadi, A. (2016). You Only Look Once: Unified, Real-Time Object Detection. Proceedings of the IEEE conference on computer vision and pattern recognition, 779-788.

Link to paper : https://arxiv.org/abs/1506.02640
