# 🚗 Driver Drowsiness Detection System

An IoT and AI-based Driver Drowsiness Detection System designed to monitor driver alertness in real time and provide immediate alerts when drowsiness or yawning is detected.

## 📌 Project Overview

Driver fatigue is a major safety concern while driving. This project combines computer vision, artificial intelligence, IoT hardware, and a web application to detect signs of driver drowsiness and provide real-time alerts.

The system detects driver states such as:

- Normal
- Drowsy
- Yawning

When drowsiness is detected, the system communicates the detected state to an ESP32-based hardware module through MQTT, which activates visual and audible alerts.

## 🏗️ System Architecture

![System Architecture](docs/archi_diagram.jpeg)

## ⚙️ Technologies Used

### AI / Computer Vision
- Python
- OpenCV
- MediaPipe

### Frontend
- React.js
- HTML
- CSS
- JavaScript

### Backend
- Node.js
- Express.js
- WebSocket

### Database
- MongoDB
- Mongoose

### IoT / Communication
- ESP32
- MQTT
- LED
- Buzzer
- Relay Module

### Authentication
- JWT
- bcrypt

## 🔄 System Workflow

1. The camera captures the driver's face.
2. OpenCV and MediaPipe process the camera input.
3. The system analyzes facial features to identify signs of drowsiness and yawning.
4. The detected state is communicated to the backend through WebSocket.
5. The backend processes and stores status information in MongoDB.
6. MQTT communicates the driver state to the ESP32.
7. The ESP32 activates the LED and buzzer when an alert condition is detected.
8. The React dashboard displays the driver's status.

## 📁 Project Structure

```text
Driver-Drowsiness-Detection-System/
│
├── docs/
│   └── archi_diagram.jpeg
│
├── hardware/
│   └── drowsy_detection.ino
│
└── software/
    │
    ├── fullstack/
    │   ├── node_server/
    │   └── react_frontend/
    │
    └── opencv+mediapipe/
        └── ai_service/