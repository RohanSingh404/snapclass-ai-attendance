# 🎓 SnapClass AI — Intelligent Attendance Management System

**Making classroom attendance faster, smarter, and more efficient with AI.**

SnapClass is an AI-powered attendance management system designed to simplify classroom attendance using facial recognition and voice recognition. It provides dedicated interfaces for teachers and students, helping automate attendance tracking while reducing the need for traditional manual roll calls.

Built with Python, Streamlit, and Supabase, SnapClass combines computer vision, machine learning, audio processing, and database management in one application.

## ✨ Features

### 👨‍🏫 Teacher Portal

- **Teacher Authentication:** Register and log in to access the teacher dashboard.
- **Subject Management:** Create and manage subjects or classes.
- **Student Enrollment:** Allow students to enroll in subjects using a join code or QR code.
- **AI-Powered Face Attendance:** Identify enrolled students from classroom images using facial recognition.
- **Voice-Based Attendance:** Use voice recognition to help identify students through audio.
- **Attendance Records:** Access and manage attendance information.
- **Attendance Analytics:** Review attendance data to monitor classroom participation.

### 👨‍🎓 Student Portal

- **Face Recognition Login:** Access the student portal through facial identification.
- **Student Registration:** Register student details and facial information.
- **Optional Voice Enrollment:** Register voice information for voice-based identification.
- **Easy Subject Enrollment:** Join subjects using a subject code or QR code.
- **Attendance Tracking:** View enrolled subjects and attendance information.
- **Subject Management:** Manage subject enrollments through the student interface.

### 🤖 AI and Machine Learning

- **Facial Feature Extraction:** Generate numerical face embeddings for identification.
- **Face Matching:** Compare detected faces against registered student information.
- **Machine Learning Classification:** Use a Support Vector Machine (SVM) classifier to assist with student identification.
- **Voice Processing:** Process audio and extract speaker representations for voice-based identification.
- **Automated Attendance:** Use recognition results to support attendance recording.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Frontend and UI | Streamlit |
| Programming Language | Python |
| Database | Supabase (PostgreSQL) |
| Computer Vision | Dlib, face_recognition_models |
| Machine Learning | Scikit-learn, SVM |
| Audio Processing | Librosa, Resemblyzer |
| Data Processing | NumPy, Pandas |
| Image Processing | Pillow |
| QR Code Generation | Segno |
| Password Security | bcrypt |

## 🏗️ Project Structure

```text
snapclass-ai-attendance/
│
├── app.py
├── requirements.txt
├── README.md
│
└── src/
    ├── components/
    │   ├── Reusable UI components
    │   └── Dialogs and interaction components
    │
    ├── database/
    │   ├── config.py
    │   └── db.py
    │
    ├── pipelines/
    │   ├── face_pipeline.py
    │   └── voice_pipeline.py
    │
    ├── screens/
    │   ├── home_screen.py
    │   ├── teacher_screen.py
    │   └── student_screen.py
    │
    └── ui/
        └── base_layout.py
```

*Note: The structure above summarizes the main modules. Refer to the repository for the complete file listing.*

## ⚙️ Getting Started

Follow these steps to run SnapClass locally.

### Prerequisites

Make sure you have the following installed:

- Python
- Git
- pip
- A Supabase project with the required database configuration

**Note:** Face-recognition dependencies such as Dlib may require additional system dependencies or compatible Python versions.

### 1. Clone the Repository

```bash
git clone https://github.com/RohanSingh404/snapclass-ai-attendance.git
```

Navigate into the project directory:

```bash
cd snapclass-ai-attendance
```

### 2. Create a Virtual Environment

**Windows — PowerShell**

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

If PowerShell blocks script execution, use Command Prompt instead:

```bat
venv\Scripts\activate.bat
```

**macOS / Linux**

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

Upgrade pip and install the project requirements:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Some face-recognition packages may need extra installation steps depending on your operating system and Python version.

### 4. Configure Supabase

SnapClass uses Supabase for database operations.

1. Create or open your Supabase project.
2. Configure the database schema required by the application.
3. Check `src/database/config.py` for the exact connection settings expected by the project.
4. Provide your Supabase project URL and API key using the configuration method implemented in the code.

**Security reminder:** Never commit database credentials, service-role keys, passwords, or other secrets to GitHub. Use environment variables or an appropriate secrets-management mechanism.

### 5. Run the Application

Start the Streamlit application from the project root:

```bash
streamlit run app.py
```

Streamlit will display a local URL in the terminal, typically:

```text
http://localhost:8501
```

Open that URL in your browser to access SnapClass.

## 🔄 How It Works

### 1. Student Registration

Students register through the application. The system can generate facial embeddings from registration images and optionally process voice samples for speaker identification.

### 2. Subject Enrollment

Teachers create subjects and share enrollment codes or QR codes with students. Students can use these to join the relevant classes.

### 3. AI-Based Attendance

Teachers initiate an attendance workflow using classroom images or the available voice-based workflow. The recognition pipelines process the provided input and compare it with registered student information.

### 4. Attendance Management

Recognition results are used by the application to support attendance recording and classroom attendance management.

### 5. Student and Teacher Dashboards

The application provides separate interfaces for students and teachers to access the functionality relevant to their roles.

## 🔐 Security and Privacy

SnapClass works with personal information and biometric data, so responsible handling is essential.

- Passwords should be stored using secure password hashing.
- Supabase credentials should be kept out of source control.
- Access to student records should be restricted according to user roles.
- Facial embeddings and voice data should be protected against unauthorized access.
- Biometric data should only be collected and processed with appropriate consent and safeguards.

## 🚀 Future Improvements

Potential enhancements for SnapClass include:

- Improved face recognition under varying lighting conditions.
- More robust voice identification in noisy classrooms.
- Better handling of unknown faces and uncertain predictions.
- Exportable attendance reports.
- Enhanced attendance analytics and visualization.
- More comprehensive automated testing.
- Improved deployment and configuration documentation.

## 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add your feature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/your-feature
   ```

5. Open a Pull Request describing your changes.

## 👨‍💻 Author

**Rohan Singh**

- GitHub: [@RohanSingh404](https://github.com/RohanSingh404)
- Project Repository: [SnapClass AI Attendance](https://github.com/RohanSingh404/snapclass-ai-attendance)

## 📄 License

No license has been specified in this README. Check the repository for an existing license before redistributing or reusing the project.

---

⭐ If you find SnapClass interesting, consider starring the repository and sharing your feedback.