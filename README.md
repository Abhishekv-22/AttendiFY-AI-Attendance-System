# AttendiFY – AI-Powered Attendance System

AttendiFY is a Python-based face recognition attendance system designed for educational institutions.  
It detects faces from a classroom image, matches them against a student database, and automatically generates attendance records along with an annotated group image.

This project focuses on **backend logic and computer vision**, and is structured to be easily extendable to APIs or UI layers.

---

## 🚀 Features
- Face recognition using `face_recognition` and OpenCV
- Automatic attendance marking from a single group image
- CSV attendance report generation
- Annotated output image with bounding boxes and names
- Clean, modular, backend-ready architecture

---

## 🛠 Tech Stack
- **Python**
- **face_recognition**
- **OpenCV**
- **NumPy**

---

## 📁 Project Structure
AttendiFY/
│
├── app/
│   ├──  __init__.py
│   └── face_recognition_service.py   # Core face recognition logic
│
├── students/
│   ├── student_data.csv              # Student metadata (name, roll no, etc.)
│   └── *.jpg                          # One clear image per student
│
├── test_images/
│   └── class_photo.jpg               # Sample classroom/group image
│
├── outputs/
│   └── (generated CSV & images)
│
├── run_local.py                      # Entry point to run locally
├── requirements.txt
└── README.md


---

## ⚙️ How It Works
1. Student face encodings are generated from images in the `students/` directory.
2. A classroom image is processed to detect and encode faces.
3. Detected faces are matched with known encodings.
4. Attendance is marked automatically.
5. Results are saved as:
   - A CSV attendance file
   - An annotated group image with names

---

## ▶️ How to Run Locally

### 1. Install dependencies
```bash
pip install -r requirements.txt
