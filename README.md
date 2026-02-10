# Diabetic Retinopathy Detection System

A full-stack web application for detecting diabetic retinopathy using deep learning (Xception CNN model).

## Features

- 🔐 **User Authentication**: Secure login and registration with SQLite database
- 🤖 **AI-Powered Detection**: Advanced Xception CNN model for retinopathy detection
- 📊 **Real-time Analysis**: Upload retinal images and get instant predictions
- 📈 **Prediction History**: Track all your previous diagnoses
- 🎨 **Modern UI**: Beautiful, responsive design with Tailwind CSS
- 🔒 **Secure**: Password hashing and session management

## Tech Stack

### Frontend
- HTML5
- Tailwind CSS
- Vanilla JavaScript

### Backend
- Flask (Python web framework)
- SQLite (Database)
- TensorFlow/Keras (Deep Learning)

## Installation

### Prerequisites
- Python 3.8 or higher
- pip

### Steps

1. **Install Dependencies**
```bash
pip install -r requirements.txt
```

2. **Ensure Model File Exists**
Make sure `final_xception_diabetic_retinopathy.h5` is in the project root directory.

3. **Run the Application**
```bash
python app.py
```

4. **Access the Application**
Open your browser and navigate to:
```
http://localhost:5000
```

## Project Structure

```
diabities_clg/
│
├── app.py                    # Flask backend
├── cnn.py                    # Model training script
├── requirements.txt          # Python dependencies
├── users.db                  # SQLite database (auto-created)
├── final_xception_diabetic_retinopathy.h5  # Trained model
│
├── templates/
│   └── index.html           # Main frontend page
│
└── static/
    └── app.js               # Frontend JavaScript
```

## Usage

### 1. Register/Login
- Create a new account or login with existing credentials
- All passwords are securely hashed

### 2. Upload Image
- Click on the upload area
- Select a retinal fundus image (PNG or JPG)
- Preview will be shown

### 3. Analyze
- Click "Analyze Image" button
- AI model will process the image
- Results will show the diagnosis and confidence levels

### 4. View History
- See all your previous predictions
- Track dates and confidence scores

## Diabetic Retinopathy Levels

The system detects 5 levels of diabetic retinopathy:

- **No DR** (0): No diabetic retinopathy
- **Mild** (1): Mild non-proliferative DR
- **Moderate** (2): Moderate non-proliferative DR
- **Severe** (3): Severe non-proliferative DR
- **Proliferative DR** (4): Proliferative diabetic retinopathy

## Model Information

- **Architecture**: Xception CNN
- **Input Size**: 229x229 pixels
- **Training Dataset**: Diabetic Retinopathy Level Detection from Kaggle
- **Classes**: 5 (No DR, Mild, Moderate, Severe, Proliferative)

## Security Features

- Password hashing using SHA-256
- Session-based authentication
- Login required for predictions
- CORS enabled for API security

## API Endpoints

- `GET /` - Main page
- `POST /register` - User registration
- `POST /login` - User login
- `POST /logout` - User logout
- `GET /check-auth` - Check authentication status
- `POST /predict` - Image prediction (auth required)
- `GET /history` - Get prediction history (auth required)

## Note

⚠️ **Important**: This is an AI-based diagnostic tool and should not replace professional medical advice. Always consult with a qualified healthcare professional for proper diagnosis and treatment.

## License

This project is for educational purposes.

## Author

Developed for college project
