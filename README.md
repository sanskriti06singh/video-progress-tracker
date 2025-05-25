# 🎓 Video Progress Tracker – Online Learning Platform

An interactive and beginner-friendly online learning platform where students can watch educational video lectures without skipping, and their progress is automatically tracked and saved.

> 🚀 Ideal for assignments, real-world projects, and future scalability into a full-fledged LMS.

---

## 📌 Features

- 🎥 **Unskippable Video Lectures** – Students must watch 100% of each video to complete it.
- ✅ **Progress Tracking** – Real-time video progress is stored locally via backend APIs.
- 📊 **Student Dashboard** – View progress of all lectures watched and completed.
- 💾 **Simple Backend Storage** – Uses JSON files for lightweight and easy-to-read data.
- 🔗 **Frontend-Backend Integration** – Clean and connected user experience.

---

## 🛠️ Tech Stack

| Layer       | Technology             |
|-------------|------------------------|
| Frontend    | HTML, CSS, JavaScript  |
| Backend     | Node.js, Express       |
| Storage     | JSON files (No DB)     |
| Deployment  | Localhost / GitHub     |

---

## 📁 Folder Structure

video-progress-tracker/
│
├── public/ # Frontend files
│ ├── video.html # Video viewing page
│ ├── progress.html # Progress dashboard
│ ├── style.css # Styling
│ └── script.js # Main JS logic
│
├── data/
│ ├── lectures.json # List of lecture metadata
│ └── progress.json # Student progress records
│
├── server.js # Node.js backend server
├── package.json # NPM dependencies
├── .gitignore # Git ignore list
└── README.md # This file

yaml
Copy
Edit

---

## 🚀 How to Run This Project Locally

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/video-progress-tracker.git
cd video-progress-tracker
2. Install Dependencies
bash
Copy
Edit
npm install
3. Start the Backend Server
bash
Copy
Edit
node server.js
Your backend will run on: http://localhost:3000

4. Open Frontend in Browser
Open the following HTML files in browser:

public/video.html → to watch lectures

public/progress.html → to see progress

🔌 Backend API Documentation
GET /lectures
Returns the list of all lecture videos.

Response:

json
Copy
Edit
[
  {
    "id": 1,
    "title": "Introduction to Biology",
    "src": "https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm",
    "duration": 600
  }
]
GET /progress/:studentId
Returns the student's watched lecture progress.

Example:

http
Copy
Edit
GET /progress/student123
Response:

json
Copy
Edit
{
  "1": 100,
  "2": 50
}
POST /progress/:studentId
Updates or adds the progress for a student.

Body:

json
Copy
Edit
{
  "lectureId": 1,
  "watchedPercentage": 100
}
