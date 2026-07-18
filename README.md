# 🎬 Social Media Video Downloader

<p align="center">
  <img src="https://img.shields.io/github/stars/akash098p/Social-Media-Video-Downloader?style=for-the-badge&color=FFE15D&logo=github" alt="GitHub stars">
  <img src="https://img.shields.io/github/forks/akash098p/Social-Media-Video-Downloader?style=for-the-badge&color=93B5C6&logo=github" alt="GitHub forks">
  <img src="https://img.shields.io/github/license/akash098p/Social-Media-Video-Downloader?style=for-the-badge&color=E4BAD4" alt="License">
  <br>
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>

A full-featured Social Media like YouTube, Instagram, Facebook, X(Twitter) video downloader built using **FastAPI + yt-dlp**.

This project allows users to: - 🎥 Download videos in all available
qualities (144p to 4K) - 🎵 Download audio-only formats - 🔄 Track
real-time download progress - ❌ Cancel downloads - 📜 View download
history - 📂 Automatically save files locally

------------------------------------------------------------------------

# 📁 Project Structure

After cloning, your project should look like this:

    SocialMediaVideoDownloader/
    │
    ├── backend.py
    ├── requirements.txt
    ├── README.md
    ├── .gitignore
    │
    ├── static/
    │     ├── index.html
    │     ├── script.js
    │     └── style.css
    │
    ├── downloads/        (auto-created)
    └── venv/             (NOT uploaded to GitHub)

⚠ Important: - `venv/` not uploaded. - `downloads/` not uploaded. - These are ignored using `.gitignore`.

------------------------------------------------------------------------

# 💻 Preview

<p align="center">
  <img src="https://i.postimg.cc/dtVq0FT6/SMD-demo.png" width="95%">
</p>

------------------------------------------------------------------------

# 🛠 Requirements

-   Python 3.9 or higher
-   pip

Check Python version:

    python --version

------------------------------------------------------------------------

# 📦 Installation Guide 

## 1️⃣ Clone the Repository

    git clone https://github.com/akash098p/SocialMediaVideoDownloader.git
    cd SocialMediaVideoDownloader

------------------------------------------------------------------------

## 2️⃣ Create Virtual Environment

Windows:

    python -m venv venv
    venv\Scripts\activate

Mac/Linux:

    python3 -m venv venv
    source venv/bin/activate

------------------------------------------------------------------------

## 3️⃣ Install Dependencies

    pip install -r requirements.txt

If requirements.txt is missing:

    pip install fastapi uvicorn yt-dlp python-multipart

------------------------------------------------------------------------

# 🚀 Running the Project (Local Only)

## 1️⃣ Start Backend Server

    uvicorn backend:app --reload --port 8000

Backend runs at:

    http://127.0.0.1:8000

------------------------------------------------------------------------

## 2️⃣ Start Frontend Server

Open a new terminal (keep backend running), then:

    python -m http.server 8080 --directory static

Frontend runs at:

    http://127.0.0.1:8080

Now open in browser:

    👉👉 http://127.0.0.1:8080 👈👈

------------------------------------------------------------------------

## 3️⃣ Quick Run with a Batch File (Windows)
Instead of opening multiple terminals manually, you can automate the process with a batch file.

1. Create a new file named `run.bat` in the root folder of your project (same level as `backend.py`).
2. Paste the following code inside it:

```batch
@echo off
REM Activate virtual environment and run Uvicorn in the first window
start cmd /k "venv\Scripts\activate && uvicorn backend:app --reload --port 8000"

REM Open a new command window for the static server
start cmd /k "venv\Scripts\activate && python -m http.server 8080 --directory static"

REM Launch the browser pointing to the static server
start "" http://127.0.0.1:8080
```
Double-click the `run.bat` file to instantly launch the backend, frontend and open the downloader in your browser!

### 💡 A quick tip for your script:
In your batch script, you are running `venv\Scripts\activate` before launching the Python HTTP server. Since `python -m http.server` is a built-in module that doesn't rely on the dependencies installed inside your virtual environment, activating `venv` for the frontend window isn't strictly necessary. It won't break anything, but keeping it as `start cmd /k "python -m http.server 8080 --directory static"` would make it slightly cleaner!

------------------------------------------------------------------------

# 📂 Downloaded Files

All downloaded videos/audio files are stored in:

    downloads/

This folder is automatically created when the backend runs.

------------------------------------------------------------------------

# ⚠ Important Notes

-   GitHub Pages cannot run this project (requires Python backend).
-   This project is designed for local execution.
-   Cloud hosting may face YouTube bot detection issues.

------------------------------------------------------------------------

# 🧠 Technologies Used

-   FastAPI
-   yt-dlp
-   Python
-   HTML / CSS / JavaScript

------------------------------------------------------------------------

# 👨‍💻 Author

<h3>Akash Pramanik</h3>

<p>
  <strong>For questions or support: </strong>
<a href="https://instagram.com/akash.098p" target="_blank">
  <img src="https://img.shields.io/badge/akash.098p-E4405F?style=flat&logo=instagram&logoColor=white"/>
</a> 

<a href="mailto:akashpramanik098@gmail.com">
  <img src="https://img.shields.io/badge/akashpramanik422%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white"/>
</a>
</p>

------------------------------------------------------------------------

# ⭐ If you found this project useful, consider giving it a star!
