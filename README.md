# CampusFlow — College Management System

A modern, role-based college management mobile application designed to simplify academic administration and improve communication between students, professors, and college administrators.

CampusFlow brings essential college activities into one unified mobile platform, providing different experiences and permissions based on user roles.

---

## Table of Contents

- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [User Roles](#user-roles)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Project Architecture](#project-architecture)
- [Application Navigation](#application-navigation)
- [Getting Started](#getting-started)
- [Environment Configuration](#environment-configuration)
- [Development Workflow](#development-workflow)
- [Security and Access Control](#security-and-access-control)
- [Future Roadmap](#future-roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

CampusFlow is a mobile-first College Management System built to manage academic and administrative activities through a single application.

Instead of maintaining separate applications for different users, CampusFlow provides three role-specific experiences within one mobile app:

- Student Portal
- Professor Portal
- Admin Portal

Each user receives access to the appropriate dashboard and features based on their assigned role.

The project follows a modular architecture to support future expansion, maintainability, and integration with additional services.

## Project Objectives

- Simplify college administration and academic management.
- Provide students with easy access to academic information.
- Help professors manage attendance, assignments, and academic records.
- Allow administrators to manage users and institutional information.
- Maintain secure, role-based access to application features.
- Build a scalable foundation for future college management requirements.

---

## User Roles

### 1. Student

The Student Portal provides students with access to their academic information and college activities.

Planned features:

- Student authentication
- Personal profile
- Attendance records
- Class timetable
- Examination results
- Assignments and submissions
- Academic notices and announcements
- Course and subject information

### 2. Professor

The Professor Portal provides tools for managing classroom and academic activities.

Planned features:

- Professor authentication
- Professor profile
- Assigned classes and subjects
- Student information
- Attendance management
- Assignment creation and management
- Marks and result management
- Academic announcements

### 3. Admin

The Admin Portal provides centralized control over college information and operations.

Planned features:

- Secure administrator authentication
- Admin dashboard
- Student management
- Professor management
- Department management
- Course and subject management
- Class and semester management
- Attendance overview
- Examination management
- Reports and analytics
- Notice and announcement management

**Note:** All three portals are part of one mobile application. Access to features will be controlled through role-based authorization.

---

## Key Features

The following features represent the planned functionality of CampusFlow:

| Module | Description |
|---|---|
| Authentication | Secure login and user authentication |
| Role Management | Student, Professor, and Admin access |
| Dashboard | Role-specific dashboard |
| Attendance | Attendance recording and tracking |
| Timetable | Class schedules and academic planning |
| Assignments | Assignment creation and submission |
| Results | Examination marks and results |
| User Management | Student and professor administration |
| Notifications | Important academic updates |
| Reports | Academic and administrative reports |

---

## Technology Stack

### Mobile Application — Frontend

- **React Native** — Cross-platform mobile application development.
- **Expo** — Development and application tooling.
- **TypeScript** — Type-safe application development.
- **Expo Router** — File-based navigation and routing.

### Backend

Proposed backend technologies:

- **Node.js** — JavaScript runtime.
- **Express.js** — REST API development.
- **MongoDB** — Database management.
- **Mongoose** — MongoDB object modeling.
- **JWT** — Authentication and authorization.

### Development Tools

- Visual Studio Code
- Git and GitHub
- Expo Go
- Postman
- MongoDB Compass

---

## Project Architecture

CampusFlow follows a modular frontend-backend architecture.

```text
CampusFlow/
│
├── frontend/                       # React Native mobile application
│   │
│   ├── src/
│   │   └── app/                    # Expo Router application routes
│   │       │
│   │       ├── _layout.tsx         # Root navigation layout
│   │       ├── index.tsx           # Application entry screen
│   │       │
│   │       ├── student/            # Student portal screens
│   │       │   ├── login.tsx
│   │       │   ├── dashboard.tsx
│   │       │   ├── profile.tsx
│   │       │   ├── attendance.tsx
│   │       │   ├── timetable.tsx
│   │       │   ├── assignments.tsx
│   │       │   └── results.tsx
│   │       │
│   │       ├── professor/          # Professor portal screens
│   │       │   ├── login.tsx
│   │       │   ├── dashboard.tsx
│   │       │   ├── profile.tsx
│   │       │   ├── attendance.tsx
│   │       │   ├── assignments.tsx
│   │       │   └── students.tsx
│   │       │
│   │       └── admin/              # Admin portal screens
│   │           ├── login.tsx
│   │           ├── dashboard.tsx
│   │           ├── students.tsx
│   │           ├── professors.tsx
│   │           ├── departments.tsx
│   │           ├── courses.tsx
│   │           └── reports.tsx
│   │
│   ├── components/                 # Reusable UI components
│   ├── assets/                     # Images, icons and fonts
│   ├── constants/                  # App constants and configuration
│   ├── hooks/                      # Custom React hooks
│   ├── services/                   # API communication
│   ├── types/                      # TypeScript type definitions
│   ├── utils/                      # Helper functions
│   ├── app.json
│   ├── package.json
│   └── tsconfig.json
│
├── backend/                        # Backend REST API (planned)
│   │
│   ├── src/
│   │   ├── config/                 # Database and app configuration
│   │   ├── controllers/            # Request handling logic
│   │   ├── middleware/             # Authentication and validation
│   │   ├── models/                 # Database models
│   │   ├── routes/                 # API route definitions
│   │   ├── services/               # Business logic
│   │   ├── utils/                  # Helper functions
│   │   └── app.js                  # Express application setup
│   │
│   ├── scripts/                    # Database and utility scripts
│   ├── tests/                      # Backend tests
│   ├── server.js                   # Backend entry point
│   ├── package.json
│   └── .env.example
│
├── .gitignore
└── README.md
```

**Architecture note:** This is the target structure. Some directories and files are planned and will be added as development progresses. Expo Router uses `frontend/src/app/` as its route root.

---

## Application Navigation

The application will follow a role-based navigation flow.

```text
                  CampusFlow
                      |
               Welcome Screen
                      |
               Select User Role
                      |
          +-----------+-----------+
          |           |           |
       Student    Professor     Admin
          |           |           |
        Login       Login        Login
          |           |           |
      Dashboard   Dashboard    Dashboard
          |           |           |
      Student     Professor      Admin
      Features     Features     Features
```

Each role will have its own navigation structure and protected screens.

---

## Getting Started

Follow these steps to set up the project locally.

### Prerequisites

Install the following tools:

- Node.js (LTS version recommended)
- npm
- Git
- Visual Studio Code
- Expo Go (Android testing)

### 1. Clone the Repository

```bash
git clone https://github.com/ritam-201/college-management-system.git
```

### 2. Navigate to the Project

```bash
cd college-management-system
```

### 3. Set Up the Frontend

```bash
cd frontend
npm install
```

### 4. Start the Expo Development Server

```bash
npx expo start
```

Scan the displayed QR code using Expo Go on your Android device.

### 5. Backend Setup

Backend setup instructions will be added when the backend implementation is available.

The planned backend will use Node.js, Express.js, and MongoDB.

---

## Environment Configuration

The frontend will use environment variables for configuration.

Example:

```env
EXPO_PUBLIC_API_URL=http://YOUR_LOCAL_IP:5000/api
```

Replace `YOUR_LOCAL_IP` with your computer's local network IP address when testing on a physical device.

For example:

```env
EXPO_PUBLIC_API_URL=http://192.168.1.5:5000/api
```

The backend will use a separate `.env` file for private configuration.

Example backend configuration:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_long_random_secret
```

**Important security practices:**

- Never commit `.env` files.
- Never expose database credentials or JWT secrets.
- Keep `.env.example` files free of real credentials.
- Add environment files to `.gitignore`.
- Validate all sensitive operations on the backend.

---

## Development Workflow

CampusFlow will be developed using a modular and incremental approach.

### Frontend Development

1. Create the main application entry screen.
2. Implement role selection.
3. Build separate login experiences.
4. Develop role-specific dashboards.
5. Implement individual modules.
6. Integrate frontend screens with backend APIs.

### Backend Development

1. Configure the Express server.
2. Connect MongoDB.
3. Design database schemas.
4. Implement authentication.
5. Implement role-based authorization.
6. Develop REST APIs for each module.
7. Integrate and test APIs with the mobile application.

### Git Workflow

Use meaningful commit messages to track development.

```bash
git add .
git commit -m "Add student dashboard"
git push origin main
```

---

## Security and Access Control

Security is an important part of CampusFlow.

Planned security measures:

- JWT-based authentication.
- Role-based access control (RBAC).
- Password hashing.
- Backend request validation.
- Protected API endpoints.
- Secure token storage on mobile devices.
- Proper error handling.
- Environment-based secret management.

The backend will remain the source of truth for user permissions. Frontend navigation restrictions alone will not provide security.

---

## Future Roadmap

CampusFlow will be developed in multiple phases.

- [ ] **Phase 1 — Project Foundation**
  - [x] Initialize React Native + Expo project.
  - [x] Configure Expo Router.
  - [ ] Establish project architecture.
  - [ ] Set up backend project.

- [ ] **Phase 2 — Authentication**
  - [ ] Role selection screen.
  - [ ] Student login.
  - [ ] Professor login.
  - [ ] Admin login.
  - [ ] Backend authentication and authorization.

- [ ] **Phase 3 — Student Portal**
  - [ ] Student dashboard.
  - [ ] Profile management.
  - [ ] Attendance tracking.
  - [ ] Timetable.
  - [ ] Assignments.
  - [ ] Examination results.

- [ ] **Phase 4 — Professor Portal**
  - [ ] Professor dashboard.
  - [ ] Student management.
  - [ ] Attendance management.
  - [ ] Assignment management.
  - [ ] Marks management.

- [ ] **Phase 5 — Admin Portal**
  - [ ] Admin dashboard.
  - [ ] Student management.
  - [ ] Professor management.
  - [ ] Department and course management.
  - [ ] Reports and analytics.

- [ ] **Phase 6 — Integration and Testing**
  - [ ] Frontend-backend integration.
  - [ ] API testing.
  - [ ] Authentication testing.
  - [ ] Role-permission testing.
  - [ ] Application performance testing.

- [ ] **Phase 7 — Deployment**
  - [ ] Production backend deployment.
  - [ ] Database deployment.
  - [ ] Android application build.
  - [ ] Google Play Store release.

---

## Contributing

CampusFlow is being developed as a modular software project.

Contributions, suggestions, and improvements are welcome.

Before contributing:

1. Fork or clone the repository.
2. Create a separate branch for your changes.
3. Follow the existing project structure.
4. Test your changes before submitting.
5. Use clear and descriptive commit messages.

---

## License

This project currently does not specify an open-source license.

A license will be added when the project's distribution and usage terms are decided.

---

## Project Information

**Project Name:** CampusFlow  
**Project Type:** College Management System  
**Platform:** Android / iOS (cross-platform mobile application)  
**Frontend:** React Native + Expo  
**Language:** TypeScript  
**Backend:** Node.js + Express.js (planned)  
**Database:** MongoDB (planned)  
**Repository:** https://github.com/ritam-201/college-management-system

---

*CampusFlow — Connecting Students, Professors, and Administration in One Platform.*