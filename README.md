# 🚀 JOBNEX — Career Intelligence & AI Resume Platform

**JOBNEX** is a full-stack, AI-powered career acceleration and resume analysis platform. It pairs candidates with job opportunities by evaluating resume-to-job-description fit, detecting skill gaps, generating targeted interview preparation questions, and tracking job applications in real time.

---

## ✨ Features

- 📄 **AI Resume & JD Analyzer**: Match resumes against job descriptions with percentage compatibility scores, identified skills, and missing requirements.
- 🎯 **Skill Gap & Course Recommendations**: Automated suggestions to bridge identified technical and domain gaps.
- 🎙️ **AI Mock Interview Coach**: Tailored interview questions and practice prompts generated from target job descriptions.
- 📊 **Candidate Command Center (Dashboard)**: Real-time KPIs tracking active applications, review statuses, and interview schedules.
- 💼 **Job Match Portal**: Browse, filter, and track relevant job postings.
- 🤖 **Interactive AI Assistant**: Career advisor chatbot for guidance and resume enhancement advice.
- 🔐 **Secure Authentication & Privacy**: Session-based auth with scrypt password hashing and user-controlled data privacy settings.

---

## 🛠️ Tech Stack

- **Backend**: Python 3.10+, [FastAPI](https://fastapi.tiangolo.com/), [SQLAlchemy 2.0](https://www.sqlalchemy.org/), [Uvicorn](https://www.uvicorn.org/)
- **Database**: MySQL / MariaDB (via `mysql-connector-python`)
- **Frontend**: Responsive HTML5, CSS3 custom design system, Modern JavaScript (ES6+ Fetch API)
- **AI Integrations**: [Anthropic Claude API](https://www.anthropic.com/) *(optional for advanced AI prompts & chat)*
- **Authentication**: Starlette SessionMiddleware with secure cookie signing, scrypt password hashing

---

## 📂 Project Structure

```text
Jobnex/
├── backend/
│   ├── main.py                 # FastAPI application, auth routes & static file hosting
│   ├── database.py             # SQLAlchemy models & database connection pooling
│   ├── analyzer.py             # Skill extraction & match scoring logic
│   ├── ai_analyzer.py          # AI interview question & course recommendation engine
│   ├── test_ai_analyzer.py     # Unit tests for AI analyzer
│   ├── test_analyzer.py        # Unit tests for scoring algorithm
│   ├── test_api_integration.py # Integration test suite
│   └── test_db.py              # Database connection tests
├── frontend/
│   ├── index.html              # Entry point redirect
│   ├── login.html              # User login & registration
│   ├── dashboard.html          # Candidate KPI dashboard & metrics
│   ├── analyzer.html           # Resume upload & JD analyzer interface
│   ├── jobs.html               # Job listings & application portal
│   ├── applications.html       # Applied jobs & status tracker
│   ├── interview.html          # AI mock interview practice
│   ├── courses.html            # Course & skill-building suggestions
│   ├── chatbot.html            # AI career advisor assistant
│   ├── common.css              # Centralized stylesheet & theme
│   ├── common.js               # Common navigation, auth & utility functions
│   └── api.js                  # Frontend API client layer
├── .gitignore                  # Git ignore rules (secrets, venv, caches)
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

- **Python 3.10+** (Python 3.10, 3.11, 3.12, or 3.15)
- **MySQL / MariaDB** (e.g. through [XAMPP](https://www.apachefriends.org/))
- **Git**

---

### Step 1: Clone the Repository

```bash
git clone https://github.com/Vamshi2691990/Jobnex.git
cd Jobnex
```

### Step 2: Set Up Virtual Environment

#### On Windows (PowerShell):
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

#### On Linux / macOS:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Configure MySQL Database

1. Start MySQL (e.g., open XAMPP and start the MySQL module).
2. Create the `jobnex` database:
   ```sql
   CREATE DATABASE jobnex CHARACTER SET utf8mb4;
   ```

### Step 5: Configure Environment Variables

Create a `.env` file in the project root (`Jobnex/.env`):

```env
# Database Configuration
DATABASE_URL=mysql+mysqlconnector://root:@127.0.0.1:3306/jobnex
DB_HOST=127.0.0.1
DB_PORT=3306
DB_USER=root
DB_PASSWORD=
DB_NAME=jobnex

# App Security
SESSION_SECRET_KEY=your-random-secret-key-here

# Optional: AI Features (Claude)
# ANTHROPIC_API_KEY=your-api-key
```

> **Note:** `.env` is ignored by Git to protect your local credentials.

### Step 6: Start the Server

```powershell
cd backend
python -m uvicorn main:app --reload
```

---

## 🌐 Accessing the Platform

Once the server is running, open your browser:

- **Web Application**: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
- **Login / Register**: [http://127.0.0.1:8000/login.html](http://127.0.0.1:8000/login.html)
- **Interactive Swagger API Docs**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- **ReDoc API Documentation**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 🧪 Running Tests

To run the test suite:

```bash
cd backend
pytest
```

---

## 📌 How to Push Changes to GitHub

Whenever you make improvements or updates to your code:

```powershell
# 1. Navigate to the Jobnex repository folder
cd D:\Vamshi\Project\Algonex\Jobnex

# 2. Check changed files
git status

# 3. Stage changes
git add .

# 4. Commit with a meaningful message
git commit -m "Add new feature / update documentation"

# 5. Push to GitHub
git push origin main
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

