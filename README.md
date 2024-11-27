# face-recognition-based-attendance-system  


![Face Recognition Based Attendance System](ss.png)

A facial recognition-based attendance system that marks attendance based on real-time face detection. The system captures faces using a webcam and matches them with registered users. If a match is found, the attendance is recorded with the timestamp and stored in an Excel/CSV file.

Features
- Real-time facial detection using Haar Cascade Classifier.
- User registration via webcam, where images are captured and stored.
- Attendance marking with name, date, and time for recognized faces.
- Attendance records are saved in an Excel/CSV file.
- A web-based interface for face detection and attendance management.
- No need for pre-built datasets; the system builds its own dataset by capturing images of registered users.

Technologies Used
- Python for the backend.
- **OpenCV** for facial detection and image processing.
- **KNN (K-Nearest Neighbors)** classifier for face recognition.
- **Haar Cascade Classifier** for face detection.
- **Pandas** for managing and storing attendance data in CSV/Excel.
- **Flask** (optional, for web interface if included).
- **Matplotlib** for displaying attendance history (optional).

 **Installation**

 **Clone the Repository**

```bash
git clone https://github.com/<your-username>/facial-recognition-attendance-system.git
cd facial-recognition-attendance-system
```

 **Dependencies**

Install the required Python libraries using `pip`:

```bash
pip install -r requirements.txt
```

 **Dependencies List**

- `opencv-python`
- `numpy`
- `scikit-learn`
- `pandas`
- `matplotlib`
- `flask` (if using web interface)

 **Setting Up the System**

1. **Run the system:**
   - Execute the script to start capturing faces and mark attendance:
   
   ```bash
   python face_attendance.py
   ```

2. **Face Registration:**
   - The system will ask you to press "c" to capture your face for registration.
   - Capture several images of each person to improve accuracy.
   - After capturing the face, the system stores the images in a folder, ready for training.

3. **Training the Model:**
   - Once you have enough images of all registered users, the system will automatically train the KNN classifier.

4. **Face Recognition and Attendance:**
   - The system will start detecting faces from the webcam feed.
   - If a match is found, attendance is marked and stored in the `attendance.csv` file.

5. **Viewing Attendance:**
   - Open the `attendance.csv` file to view the attendance records, which include the name, date, and time.

 **Usage**

 **Capturing Face Images**

1. Run the system and press the "c" key when prompted to capture your face.
2. The system will capture and store multiple images of your face for training the KNN classifier.

 **Marking Attendance**

1. Once the face is registered, the system will start detecting faces in real-time.
2. If a face matches any of the registered users, attendance is marked with the corresponding name, date, and time.

 **Attendance Records**

- Attendance records will be saved in a CSV/Excel file named `attendance.csv`.
- The file will contain columns such as:
  - **Name**: The recognized user's name.
  - **Date**: The date of the attendance.
  - **Time**: The time at which the attendance was marked.

Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Create a new Pull Request.

