# 🚀 AgileFlow - Complete Project Management Solution

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen)](https://nodejs.org/)
[![React Version](https://img.shields.io/badge/react-18.2.0-blue)](https://reactjs.org/)
[![SQLite Version](https://img.shields.io/badge/sqlite-5.1.6-blue)](https://www.sqlite.org/)

A full-stack Agile Project Management application for small teams to manage projects, user stories, tasks, and team collaboration efficiently.

## 🚀 Live Demo

### 🌐 Website URL
**[https://agile-project-management-code-review-1.onrender.com](https://agile-project-management-code-review-1.onrender.com)**

---

## 🔐 Demo Credentials

### Test Account (Use this to login)

| Field | Value |
|-------|-------|
| **Email** | `rantdev0@gmail.com` |
| **Email** | `rantdev9179@gmail.com` |
| **Password** | `123456` |

> ⚠️ **Note:** If you face any login issues, please register a new account. Registration is quick and easy!

---

## 🎥 Demo Video

**[▶️ Click here to watch the demo video](https://www.veed.io/view/3925a6ff-1a12-49b1-9678-248255e81319?source=editor&panel=share)**

### What's in the video:
- Login with demo credentials
- Create projects, stories, and tasks
- Team management and chat
- Performance analytics

---

## 📱 Quick Start

1. **Go to:** https://agile-project-management-code-review-1.onrender.com
2. **Use credentials:** `rantdev9179@gmail.com` / `123456`
3. **Or register** a new account
4. **Start exploring** the features!

---

## ❓ Having Trouble Logging In?

### Option 1: Register a New Account
1. Click "Create Account" on the login page
2. Enter your name, email, and password
3. Complete the OTP verification
4. Login with your new credentials

### Option 2: Use Google Login
- Click "Sign in with Google"
- Use your Google account

---

## 📞 Support

- **Email:** rantdev0@gmail.com
- **GitHub Issues:** [Create issue](https://github.com/Rantdev/agile-project-management/issues)

---

**Thank you for checking out AgileFlow! 🚀**
## 📋 Table of Contents
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Database Schema](#-database-schema)
- [Installation](#-installation)
- [Environment Variables](#-environment-variables)
- [API Endpoints](#-api-endpoints)
- [Usage Guide](#-usage-guide)
- [Security Features](#-security-features)
- [AI Usage](#-ai-usage)
- [Future Improvements](#-future-improvements)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)

## ✨ Features

### 🔐 Authentication & Security
- Email/Password login with JWT authentication
- Google OAuth 2.0 integration
- OTP (One-Time Password) verification for new users
- Password hashing with bcrypt (10 rounds)
- Protected routes and API endpoints
- Session management with 7-day token expiry

### 📊 Project Management
- Create, read, update, delete projects
- Project status tracking (Planning, Active, Completed, Archived)
- Project owner assignment
- Project statistics (tasks, members, stories count)
- Search and filter projects

### 📝 User Story Management
- Create stories within projects
- Story status tracking (To Do, In Progress, Done)
- Hierarchical structure: Project → Story → Task
- Story prioritization
- Story points estimation

### ✅ Task Management
- Create tasks within stories
- Assign tasks to team members
- Set deadlines and priorities
- Task status updates
- Kanban-style task board (To Do, In Progress, Done)
- Task completion tracking
- Overdue task highlighting

### 👥 Team Collaboration
- Add/remove team members to projects
- Role-based access control:
  - **Product Owner**: Full CRUD operations
  - **Team Member**: View and update task status only
- Team member roles and permissions
- Activity tracking

### 💬 Real-time Chat
- Project-based team chat rooms
- Live message updates (polling every 5 seconds)
- Delete own messages
- User avatars and identification
- Message timestamps
- Chat history (last 100 messages)

### 📈 Performance Analytics
- **Individual Performance Dashboard**
  - Task completion rate
  - Task breakdown (completed, in-progress, pending)
  - Overdue tasks count
  - Average completion time
  - Projects and stories contribution

- **Team Performance Dashboard**
  - Team overview metrics
  - Individual member performance
  - Completion rates by member
  - Project progress tracking

- **Company Analytics**
  - Total users, projects, tasks statistics
  - Overall completion rate
  - Top performers leaderboard
  - Weekly activity trends

### 👤 User Profile Management
- View and edit profile information
- Add/remove skills with proficiency levels (Beginner, Intermediate, Advanced, Expert)
- Change password functionality
- Role selection during registration
- Department and contact information
- Social links (GitHub, LinkedIn)

### 📧 Email Notifications
- Email notification on task assignment
- Daily cron job for overdue task reminders (9:00 AM)
- Rich HTML email templates
- OTP emails for verification

## 🛠️ Tech Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| React | 18.2.0 | UI Framework |
| React Router DOM | 6.20.1 | Routing |
| Axios | 1.6.2 | API calls |
| Tailwind CSS | 3.4.0 | Styling |
| React Hot Toast | 2.4.1 | Notifications |
| React Icons | 5.0.1 | Icons |
| Vite | 5.0.8 | Build tool |
### Frontend
- **React 18** with JavaScript/JSX
- React Router DOM for navigation
- Axios for API integration
- Tailwind CSS for styling
- Vite as build tool

### Or more accurately:
- **Language**: JavaScript (ES6+)
- **Framework**: React 18
- **File Syntax**: JSX (JavaScript XML)

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| Node.js | 14+ | Runtime |
| Express | 4.18.2 | Web framework |
| SQLite3 | 5.1.6 | Database |
| JWT | 9.0.2 | Authentication |
| bcryptjs | 2.4.3 | Password hashing |
| Nodemailer | 6.9.7 | Email service |
| node-cron | 3.0.3 | Scheduled jobs |

## 📂 Project Structure

```bash
agile-project-management/
│
├── server/                         # Backend application
│   ├── config/
│   │   ├── db.js                   # Database connection
│   │   └── env.js                  # Environment validation
│   │
│   ├── controllers/
│   │   ├── authController.js       # Authentication logic
│   │   ├── projectController.js    # Project CRUD operations
│   │   ├── storyController.js      # Story management
│   │   ├── taskController.js       # Task management
│   │   ├── teamController.js       # Team member management
│   │   ├── chatController.js       # Real-time chat
│   │   ├── performanceController.js# Analytics & reports
│   │   ├── profileController.js    # User profile management
│   │   ├── emailController.js      # Email notifications
│   │   └── otpController.js        # OTP verification
│   │
│   ├── middleware/
│   │   ├── auth.js                 # JWT verification
│   │   ├── errorHandler.js         # Global error handling
│   │   └── validation.js           # Input validation
│   │
│   ├── models/
│   │   └── initDB.js               # Database schema initialization
│   │
│   ├── routes/
│   │   ├── authRoutes.js           # Authentication endpoints
│   │   ├── projectRoutes.js        # Project endpoints
│   │   ├── storyRoutes.js          # Story endpoints
│   │   ├── taskRoutes.js           # Task endpoints
│   │   ├── teamRoutes.js           # Team endpoints
│   │   ├── chatRoutes.js           # Chat endpoints
│   │   ├── performanceRoutes.js    # Analytics endpoints
│   │   ├── profileRoutes.js        # Profile endpoints
│   │   └── otpRoutes.js            # OTP endpoints
│   │
│   ├── jobs/
│   │   └── reminderJob.js          # Daily overdue task reminder
│   │
│   ├── .env                        # Environment variables
│   ├── .env.example                # Example environment variables
│   ├── package.json                # Dependencies
│   ├── package-lock.json           # Lock file
│   ├── app.js                      # Express app configuration
│   └── server.js                   # Server entry point
│
├── client/                         # Frontend application
│   ├── public/
│   │   └── vite.svg
│   │
│   ├── src/
│   │   ├── assets/
│   │   │   └── logo.svg
│   │   │
│   │   ├── components/
│   │   │   ├── Layout/
│   │   │   │   ├── Sidebar.jsx
│   │   │   │   ├── Navbar.jsx
│   │   │   │   └── ProtectedRoute.jsx
│   │   │   │
│   │   │   ├── Projects/
│   │   │   │   ├── ProjectCard.jsx
│   │   │   │   └── ProjectModal.jsx
│   │   │   │
│   │   │   ├── Stories/
│   │   │   │   ├── StoryCard.jsx
│   │   │   │   └── StoryModal.jsx
│   │   │   │
│   │   │   ├── Tasks/
│   │   │   │   ├── TaskCard.jsx
│   │   │   │   ├── TaskBoard.jsx
│   │   │   │   └── TaskModal.jsx
│   │   │   │
│   │   │   ├── Chat/
│   │   │   │   ├── ChatBox.jsx
│   │   │   │   └── ChatMessage.jsx
│   │   │   │
│   │   │   ├── Performance/
│   │   │   │   ├── StatsCard.jsx
│   │   │   │   ├── TaskChart.jsx
│   │   │   │   └── Leaderboard.jsx
│   │   │   │
│   │   │   └── Common/
│   │   │       ├── LoadingSpinner.jsx
│   │   │       ├── ConfirmDialog.jsx
│   │   │       └── Toast.jsx
│   │   │
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── OTPVerification.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── Projects.jsx
│   │   │   ├── ProjectDetails.jsx
│   │   │   ├── StoryTasks.jsx
│   │   │   ├── MyTasks.jsx
│   │   │   ├── Team.jsx
│   │   │   ├── Performance.jsx
│   │   │   ├── Profile.jsx
│   │   │   └── RoleSetup.jsx
│   │   │
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   │
│   │   ├── hooks/
│   │   │   ├── useAuth.js
│   │   │   ├── useToast.js
│   │   │   └── useLocalStorage.js
│   │   │
│   │   ├── services/
│   │   │   └── api.js
│   │   │
│   │   ├── utils/
│   │   │   ├── constants.js
│   │   │   ├── helpers.js
│   │   │   └── validators.js
│   │   │
│   │   ├── styles/
│   │   │   └── global.css
│   │   │
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── .env
│   ├── .env.example
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   ├── tailwind.config.js
│   ├── postcss.config.js
│   └── vite.config.js
│
├── database/
│   └── agile.db                   # SQLite database
│
├── docs/
│   ├── api-docs.md                # API documentation
│   ├── architecture.md            # Architecture docs
│   └── schema.md                  # Database schema
│
├── .gitignore
├── README.md
├── LICENSE
└── package.json
```

## 🗄️ Database Schema

### Tables Structure

```sql
-- Users table
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  email TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  role TEXT DEFAULT 'member',
  bio TEXT,
  avatar TEXT,
  department TEXT,
  phone TEXT,
  location TEXT,
  github TEXT,
  linkedin TEXT,
  is_verified INTEGER DEFAULT 0,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP
);

-- Projects table
CREATE TABLE projects (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  description TEXT,
  status TEXT DEFAULT 'Planning',
  created_by INTEGER NOT NULL,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (created_by) REFERENCES users(id)
);

-- Stories table
CREATE TABLE stories (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  project_id INTEGER NOT NULL,
  title TEXT NOT NULL,
  description TEXT,
  status TEXT DEFAULT 'To Do',
  created_by INTEGER,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (project_id) REFERENCES projects(id),
  FOREIGN KEY (created_by) REFERENCES users(id)
);

-- Tasks table
CREATE TABLE tasks (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  story_id INTEGER NOT NULL,
  title TEXT NOT NULL,
  assignee TEXT NOT NULL,
  deadline DATE,
  status TEXT DEFAULT 'To Do',
  created_by INTEGER,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  updated_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (story_id) REFERENCES stories(id),
  FOREIGN KEY (created_by) REFERENCES users(id)
);

-- Team members table
CREATE TABLE team_members (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  project_id INTEGER NOT NULL,
  user_email TEXT NOT NULL,
  role TEXT DEFAULT 'member',
  joined_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  UNIQUE(project_id, user_email),
  FOREIGN KEY (project_id) REFERENCES projects(id)
);

-- Chat messages table
CREATE TABLE chat_messages (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  project_id INTEGER NOT NULL,
  user_id INTEGER NOT NULL,
  user_name TEXT NOT NULL,
  user_email TEXT NOT NULL,
  user_avatar TEXT,
  message TEXT NOT NULL,
  file_url TEXT,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (project_id) REFERENCES projects(id),
  FOREIGN KEY (user_id) REFERENCES users(id)
);

-- OTP codes table
CREATE TABLE otp_codes (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  email TEXT NOT NULL,
  otp_code TEXT NOT NULL,
  expires_at DATETIME NOT NULL,
  is_used INTEGER DEFAULT 0,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (email) REFERENCES users(email)
);

-- User skills table
CREATE TABLE user_skills (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  user_id INTEGER NOT NULL,
  skill_name TEXT NOT NULL,
  skill_level TEXT DEFAULT 'Beginner',
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
