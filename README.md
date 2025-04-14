# Easy Attendance: Automated Facial Recognition Attendance System

## Overview

Easy Attendance is a Python-based attendance management system that leverages facial recognition technology to automatically mark student attendance. This project aims to simplify and modernize the attendance process, eliminating the need for manual roll calls or card swiping. By utilizing real-time facial analysis, Easy Attendance provides an efficient and accurate solution for educational institutions.

The facial recognition logic behind this project is based on the principles outlined in [Adam Geitgey's excellent blog post: "Machine Learning is Fun! Part 4: Modern Face Recognition with Deep Learning"](https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78). This approach utilizes deep learning techniques to generate facial embeddings, allowing for robust and accurate face identification.

## Key Features

* **Automated Attendance:** Marks student attendance automatically through facial recognition.
* **Real-time Analysis:** Utilizes OpenCV for real-time video stream processing and facial detection.
* **Secure Data Storage:** Employs Firebase for storing student data, facial embeddings, and attendance records.
* **Easy to Use:** Provides a user-friendly interface (intended for future development) for managing student data and viewing attendance reports.
* **Scalable:** Designed to handle a large number of students with efficient processing.

## Technologies Used

* **Python:** The primary programming language.
* **OpenCV (cvzone, cv2):** For real-time video capture and facial analysis.
* **face-recognition:** A Python library for face recognition based on dlib's state-of-the-art face recognition built with deep learning.
* **dlib:** Contains the implementation of modern C++ algorithms used by the `face-recognition` library.
* **Firebase:** A Backend-as-a-Service (BaaS) platform used for:
    * **Database:** Storing student information, facial embeddings, and attendance logs.
    * **(Potentially) Authentication:** Managing user accounts (for administrators).
* **NumPy:** For numerical computations and array manipulation.
* **Pillow (PIL):** For image processing tasks.
* **Other supporting libraries:** As listed in the `requirements.txt` (to be generated).

## Installation

Follow these steps to set up the Easy Attendance project on your local machine:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Fisk-Easy-Attendance/fisk-easy-attendance
    cd EasyAttendance
    ```

2.  **Install Dependencies:**
    It is highly recommended to create a virtual environment to isolate the project dependencies.

    **On macOS and Linux:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **On Windows:**
    ```bash
    python -m venv venv
    .\venv\Scripts\activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```
3.  **Set up Firebase:**
    * Create a new project on the [Firebase Console](https://console.firebase.google.com/).
    * Set up a Firebase Realtime Database.
    * Obtain your Firebase project's configuration details (API key, auth domain, database URL, etc.). This information is usually found in the Firebase project settings.

4.  **Configure Firebase Credentials:**
    * Add configuration information to serviceAccountKey.json.
    * Paste your Firebase configuration details into this file as a Python dictionary:

5.  **Run the Application:**
    Navigate to the project directory in your terminal and run the main script (e.g., `main.py`):

    ```bash
    python main.py
    ```