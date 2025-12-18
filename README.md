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

```text
AttendiFY_Project/
├── app/
│   └── face_recognition_service.py
├── students/
│   ├── student_data.csv
│   └── *.jpg
├── test_images/
│   └── class_photo.jpg
├── outputs/
│   ├── attendance_2025-12-17_13-49-12.csv
│   ├── result_2025-12-17_13-49-12.jpg
│   └── docs/
│       └── sample_attendance_output.jpg
├── run_local.py
├── requirements.txt
└── README.md
```
---

## 📸 Sample Output

Below is an example of the system marking attendance from a single classroom image.

- Known students are identified and labeled
- Unknown faces are explicitly marked as "Unknown"
- Bounding boxes are drawn using OpenCV
- Attendance is saved automatically as a CSV file

> Note: Sample images are used for demonstration purposes.
![Sample Attendance Output](outputs/docs/sample_attendance_output.jpg)

---

## 🧩 Design Decisions

- Core face recognition logic is isolated in a service module (`face_recognition_service.py`)
- Student metadata is loaded from a CSV file for easy scalability
- The system is UI-agnostic and can be extended to REST APIs or Streamlit
- Unknown faces are intentionally excluded from attendance to avoid false positives

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
```

### 2. Run the project
```bash
python run_local.py

