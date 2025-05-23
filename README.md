# AI_Identity_Verification_system
This project is an AI-based identity verification system that uses face recognition to identify individuals from images. It combines OpenCV, deep learning, and a simple GUI to perform real-time face detection and identification, ideal for security and access control applications.

🚀 Features
🔍 Face Detection using OpenCV and Haar cascades

🧑‍💼 Identity Recognition using a trained deep learning model

🧹 Preprocessing Pipeline for training image datasets

🖼️ Live Camera Feed or image-based verification

🖥️ Simple GUI Interface for real-time usage

📦 Organized structure for easy model retraining and updates

📁 Project Structure
bash
Copy
Edit
AI_Identity_Verification_System/
│
├── dataset/              # Training images (organized by person)
├── trained_model/        # Saved face recognition model
├── face_recognition.py   # Core recognition logic
├── dataset_creator.py    # Captures and saves images for training
├── train_model.py        # Trains the face recognition model
├── gui_app.py            # GUI application for live verification
├── utils/                # Helper functions and configurations
└── README.md             # Project documentation
🔧 Requirements
Python 3.7+

OpenCV

NumPy

scikit-learn

Pillow

tkinter

Install dependencies with:

bash
Copy
Edit
pip install -r requirements.txt
🛠️ How to Use
Create Dataset:

Run dataset_creator.py to collect images for each identity.

Train Model:

Execute train_model.py to train and save the recognition model.

Run Verification:

Launch gui_app.py to use the live identity verification system.

🎯 Use Cases
Smart attendance systems

Secure door access control

ID verification at check-in counters

Classroom face recognition projects

📌 Future Improvements
Add mask detection or emotion recognition

Improve accuracy using CNNs or transfer learning (e.g., FaceNet)

Deploy using Flask/Streamlit for web interface
