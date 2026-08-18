# Face Detection with OpenCV

A simple real-time **face detection project using Python and OpenCV**. The application accesses the computer's webcam, detects human faces using a Haar Cascade classifier, and draws a green rectangle around each detected face.

## 📌 Project Overview

This project demonstrates the basics of computer vision and real-time face detection using OpenCV.

The program:

1. Opens the computer's webcam.
2. Captures video frames in real time.
3. Converts each frame from RGB/BGR to grayscale.
4. Uses the **Haar Cascade Classifier** to detect faces.
5. Draws a green rectangle around every detected face.
6. Displays the result in a window.
7. Stops the webcam when the **ESC** key is pressed.

## 🛠️ Technologies Used

- **Python**
- **OpenCV (cv2)**
- Haar Cascade Classifier
- Computer Vision
- Real-time Video Processing

## 📂 Project Structure

```text
face_recognition/
│
├── face_reco.py
├── haarcascade_frontalface_default.xml
└── README.md
```

## ⚙️ Installation

Make sure Python is installed on your computer.

Install OpenCV with:

```bash
pip install opencv-python
```

You can verify the installation with:

```python
import cv2
print(cv2.__version__)
```

## 🚀 How to Run

Clone the repository:

```bash
git clone https://github.com/USERNAME/REPOSITORY_NAME.git
```

Navigate to the project directory:

```bash
cd face_recognition
```

Run the Python script:

```bash
python face_reco.py
```

Your webcam should open automatically, and detected faces will be highlighted with green rectangles.

### ⌨️ Controls

Press **ESC** to stop the program and close the webcam window.

## 🧠 How It Works

The project uses OpenCV's `CascadeClassifier` with the Haar Cascade model:

```python
face_cascade = cv2.CascadeClassifier(
    'haarcascade_frontalface_default.xml'
)
```

Each webcam frame is converted to grayscale:

```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```

The classifier then searches for faces:

```python
faces = face_cascade.detectMultiScale(gray, 1.5, 4)
```

For every detected face, the program draws a rectangle:

```python
cv2.rectangle(
    img,
    (x, y),
    (x+w, y+h),
    (0, 255, 0),
    3
)
```

## 📷 Example

When the program detects a face, a green bounding box appears around it in the webcam window.

