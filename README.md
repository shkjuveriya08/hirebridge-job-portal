# HireBridge – Full-Stack Job Portal

> **Connecting Talent with Opportunity**

HireBridge is a full-stack job portal designed to connect **job seekers and recruiters** through a centralized web platform.

The application allows job seekers to create accounts, explore job opportunities, view job details, apply for suitable positions, and manage their profiles. Recruiters can create and manage company profiles, publish job vacancies, view applicants, and manage recruitment activities.

---

## 📌 Project Overview

The objective of HireBridge is to simplify the job-search and recruitment process by providing separate functionalities for **Job Seekers** and **Recruiters** within a single platform.

The project follows a modern full-stack architecture with a React-based frontend and a Node.js/Express backend connected to MongoDB.

---

## ✨ Key Features

### 👤 Job Seeker

* User registration and login
* Secure authentication
* Browse available job opportunities
* Search and filter jobs
* View detailed job information
* Apply for jobs
* View applied jobs
* Manage user profile
* Update profile information
* Upload profile-related information
* Responsive user interface

### 🏢 Recruiter / Company

* Recruiter authentication
* Create company profile
* Update company information
* Upload company logo
* Post new job vacancies
* Manage posted jobs
* View applicants
* View applicant details
* Manage company information
* Protected recruiter routes
* Recruitment dashboard

### 💼 Job Management

* Create job listings
* Display latest jobs
* Browse jobs by category
* Filter jobs
* View complete job descriptions
* Track job applications
* Manage job listings

### 🔐 Authentication & Security

* User authentication
* Protected routes
* Role-based functionality
* Authentication middleware
* Secure API requests
* Environment variables for sensitive configuration

---

## 🛠️ Technology Stack

### Frontend

| Technology    | Purpose                             |
| ------------- | ----------------------------------- |
| React.js      | User interface                      |
| Vite          | Frontend development and build tool |
| JavaScript    | Application logic                   |
| Tailwind CSS  | Styling                             |
| Redux Toolkit | Global state management             |
| React Router  | Client-side routing                 |
| Axios         | API communication                   |
| Shadcn/UI     | Reusable UI components              |

### Backend

| Technology           | Purpose                 |
| -------------------- | ----------------------- |
| Node.js              | Server-side runtime     |
| Express.js           | Backend framework       |
| MongoDB              | Database                |
| Mongoose             | MongoDB object modeling |
| Cloudinary           | Image/file storage      |
| Multer               | File upload handling    |
| JWT / Authentication | User authentication     |

### Development Tools

* Visual Studio Code
* Git
* GitHub
* MongoDB
* MongoDB Atlas
* Postman

---

## 🏗️ Project Architecture

```text
HireBridge
│
├── backend/
│   │
│   ├── controllers/
│   │   ├── application.controller.js
│   │   ├── company.controller.js
│   │   ├── job.controller.js
│   │   └── user.controller.js
│   │
│   ├── middlewares/
│   │   ├── isAuthenticated.js
│   │   └── mutler.js
│   │
│   ├── models/
│   │   ├── application.model.js
│   │   ├── company.model.js
│   │   ├── job.model.js
│   │   └── user.model.js
│   │
│   ├── routes/
│   │   ├── application.route.js
│   │   ├── company.route.js
│   │   ├── job.route.js
│   │   └── user.route.js
│   │
│   ├── utils/
│   │   ├── cloudinary.js
│   │   ├── datauri.js
│   │   └── db.js
│   │
│   ├── index.js
│   ├── package.json
│   └── package-lock.json
│
├── frontend/
│   │
│   ├── public/
│   │
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── redux/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── package.json
│   ├── vite.config.js
│   ├── tailwind.config.js
│   └── package-lock.json
│
├── .gitignore
├── microsoft.jpg
├── technov.jpg
└── README.md
```

---

## 🔄 Application Workflow

### Job Seeker Workflow

```text
Register / Login
       ↓
   Home Page
       ↓
 Browse Jobs
       ↓
 Search / Filter
       ↓
 View Job Details
       ↓
   Apply for Job
       ↓
 View Applied Jobs
       ↓
 Manage Profile
```

### Recruiter Workflow

```text
Register / Login
       ↓
 Create Company Profile
       ↓
 Recruiter Dashboard
       ↓
    Post Job
       ↓
 Manage Job Listings
       ↓
 View Applicants
       ↓
 Manage Recruitment
```

---

## 📂 Frontend Structure

The frontend is developed using React and Vite.

Important frontend sections include:

### Components

* `Home.jsx` – Main home page
* `Jobs.jsx` – Job listing page
* `Job.jsx` – Individual job display
* `JobDescription.jsx` – Detailed job information
* `Browse.jsx` – Job browsing
* `Profile.jsx` – User profile
* `AppliedJobTable.jsx` – Applied jobs
* `Login.jsx` – User login
* `Signup.jsx` – User registration

### Recruiter Components

* `AdminJobs.jsx`
* `AdminJobsTable.jsx`
* `Applicants.jsx`
* `ApplicantsTable.jsx`
* `Companies.jsx`
* `CompaniesTable.jsx`
* `CompanyCreate.jsx`
* `CompanySetup.jsx`
* `PostJob.jsx`
* `ProtectedRoute.jsx`

### State Management

Redux is used to manage application state through:

```text
redux/
├── authSlice.js
├── applicationSlice.js
├── companySlice.js
├── jobSlice.js
└── store.js
```

---

## 📂 Backend Structure

The backend follows a controller-route-model architecture.

### Controllers

Controllers contain the application business logic for:

* Users
* Jobs
* Companies
* Applications

### Models

MongoDB data is organized using Mongoose models:

```text
User
Company
Job
Application
```

### Routes

API routes are separated according to functionality:

```text
User Routes
Company Routes
Job Routes
Application Routes
```

### Middleware

Authentication middleware protects routes that require an authenticated user.

---

## 🗄️ Database

HireBridge uses **MongoDB** as its database.

The main collections/entities are:

```text
User
  │
  ├── Applications
  │
  └── Profile

Company
  │
  └── Jobs
       │
       └── Applications
```

Mongoose is used to define schemas and interact with MongoDB.

---

## ☁️ Cloudinary Integration

Cloudinary is used for handling uploaded images such as:

* Company logos
* Profile images
* Other supported application media

Uploaded files are processed through the backend before being stored using Cloudinary.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/shkjuveriya08/hirebridge-job-portal.git
```

### 2. Navigate to the Project

```bash
cd hirebridge-job-portal
```

---

## 🔧 Backend Setup

Navigate to the backend:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file inside the `backend` directory.

Example:

```env
MONGO_URI=your_mongodb_connection_string
PORT=8000
SECRET_KEY=your_secret_key
CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
```

> **Important:** Never upload your actual `.env` file or private credentials to GitHub.

Start the backend:

```bash
npm run dev
```

---

## 💻 Frontend Setup

Open a new terminal.

Navigate to the frontend:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Vite will provide the local development URL in the terminal.

---

## 🔐 Environment Variables

Sensitive information is stored using environment variables instead of being hard-coded into the application.

The `.env` file is excluded from Git using `.gitignore`.

Example:

```env
MONGO_URI=
SECRET_KEY=
CLOUD_NAME=
API_KEY=
API_SECRET=
```

---

## 📸 Screenshots

Screenshots of the application can be added here to demonstrate the main features.

### Home Page

*Add screenshot here*

### Job Listings

*Add screenshot here*

### Job Description

*Add screenshot here*

### Login / Registration

*Add screenshot here*

### Recruiter Dashboard

*Add screenshot here*

### Post Job

*Add screenshot here*

### Applicants Management

*Add screenshot here*

---

## 🎯 Project Objectives

The main objectives of HireBridge are:

1. To provide a centralized job-search platform.
2. To allow users to discover suitable employment opportunities.
3. To provide recruiters with tools for publishing job vacancies.
4. To simplify the job application process.
5. To provide separate functionality for job seekers and recruiters.
6. To store and manage job-related data using MongoDB.
7. To provide a responsive and user-friendly web interface.

---

## 🚀 Future Enhancements

Possible future improvements include:

* Email notifications for applications
* Resume upload and management
* Advanced job recommendation system
* Application status tracking
* Admin panel
* Recruiter analytics dashboard
* Saved jobs
* Bookmark functionality
* Advanced search and filtering
* Real-time notifications
* Interview scheduling
* Deployment with a production database and hosting platform

---

## 🧪 Testing

The application can be tested by performing the following workflows:

### Job Seeker

* Register a new account
* Login
* Browse jobs
* Search for jobs
* View job details
* Apply for a job
* Check applied jobs
* Update profile

### Recruiter

* Register/login
* Create company profile
* Post a job
* View posted jobs
* View applicants
* Manage company information

---

## 📌 Project Highlights

* Full-stack web application
* React-based responsive frontend
* REST API based backend
* MongoDB database integration
* Authentication and protected routes
* Separate job seeker and recruiter workflows
* Job and application management
* Company management
* Cloudinary image storage
* Redux state management
* Modular backend architecture

---

## 👩‍💻 Developer

**Juveriya Shaikh**

BSc Information Technology

GitHub: [@shkjuveriya08](https://github.com/shkjuveriya08)

---

## 📄 License

This project was developed as an academic/college project for educational purposes.

---

## ⭐ Acknowledgement

This project was developed as part of the academic project work for learning and implementing full-stack web development concepts including frontend development, backend API development, database management, authentication, file handling, and state management.
