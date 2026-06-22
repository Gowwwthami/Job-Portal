MERN Job Portal

A full-stack Job Portal application built using the MERN stack that connects job seekers with employers through a secure and scalable recruitment platform. The system enables employers to post and manage job listings while allowing job seekers to search, apply, and track applications seamlessly.

## 🚀 Features

### Authentication & Authorization

* Secure JWT-based authentication
* Role-based access control
* Separate workflows for:

  * Job Seekers
  * Employers
* Password encryption using bcrypt
* Protected routes and secure session handling

### Job Management

* Create and publish job listings
* Update and delete jobs
* View all available jobs
* Search and filter jobs by category and location
* Track posted jobs

### Application Management

* Apply to jobs with resume upload
* Upload resumes through Cloudinary integration
* Submit cover letters and applicant details
* View submitted applications
* Employer-side application management

### Employer Dashboard

* Post new job opportunities
* Manage active job listings
* Review candidate applications
* Access applicant details and resumes

### Job Seeker Dashboard

* Browse available opportunities
* View job details
* Submit applications
* Track applied jobs

### Responsive User Interface

* Modern React-based frontend
* Mobile-friendly design
* Fast navigation using React Router
* Interactive notifications using React Hot Toast

---

## 🏗️ System Architecture

### Frontend

* React.js
* React Router DOM
* Axios
* React Hot Toast
* Vite

### Backend

* Node.js
* Express.js
* JWT Authentication
* RESTful APIs

### Database

* MongoDB
* Mongoose ODM

### Cloud Services

* Cloudinary (Resume Storage)

---

## 📂 Project Structure

```bash
Job-Portal/
│
├── backend/
│   ├── controllers/
│   ├── database/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── app.js
│   └── server.js
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── vite.config.js
│
└── README.md
```

---

## 🔐 Authentication Flow

### User Registration

1. User registers as:

   * Job Seeker
   * Employer
2. Password is hashed using bcrypt.
3. User information is stored in MongoDB.
4. JWT token is generated upon successful registration.

### User Login

1. Credentials are validated.
2. Password is compared using bcrypt.
3. JWT token is issued.
4. Protected resources become accessible.

---

## 🗄️ Database Design

### User Schema

```javascript
{
  name,
  email,
  phone,
  password,
  role,
  createdAt
}
```

### Job Schema

```javascript
{
  title,
  description,
  category,
  country,
  city,
  location,
  fixedSalary,
  salaryFrom,
  salaryTo,
  expired,
  postedBy
}
```

### Application Schema

```javascript
{
  name,
  email,
  phone,
  address,
  coverLetter,
  resume,
  applicantID,
  employerID
}
```

---

## 📡 API Modules

### User APIs

* Register User
* Login User
* Logout User
* Get User Profile

### Job APIs

* Post Job
* Get All Jobs
* Get Single Job
* Delete Job
* Get Employer Jobs

### Application APIs

* Apply for Job
* Get Applicant Applications
* Get Employer Applications
* Delete Application

---

## ☁️ Cloudinary Integration

Resumes are uploaded and stored securely using Cloudinary.

Benefits:

* Scalable cloud storage
* Secure file hosting
* Easy retrieval of applicant resumes
* Reduced backend storage overhead

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/your-username/job-portal.git
cd job-portal
```

### Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file:

```env
PORT=4000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET_KEY=your_secret_key
JWT_EXPIRE=7d

FRONTEND_URL=http://localhost:5173

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

Run backend:

```bash
npm start
```

---

### Frontend Setup

```bash
cd frontend
npm install
```

Run frontend:

```bash
npm run dev
```

Application runs at:

```bash
http://localhost:5173
```

---

## 🧪 Key Engineering Highlights

* JWT-based secure authentication
* Role-based authorization system
* RESTful API architecture
* Cloudinary-powered resume management
* Modular backend architecture
* MongoDB schema design for scalability
* Error handling middleware
* Secure password hashing with bcrypt
* Separation of concerns using controllers, routes, and models

---

## 🎯 Future Enhancements

* Email notifications
* Job recommendations using AI
* Resume parsing
* Advanced job filtering
* Company profiles
* Interview scheduling
* Real-time messaging
* Application analytics dashboard
* Admin panel
* Docker deployment

---

## 📈 Learning Outcomes

Through this project, I gained hands-on experience in:

* Full-stack MERN development
* Authentication and authorization
* REST API development
* MongoDB schema design
* Cloudinary file storage
* Backend architecture and middleware
* Agile development workflows
* Git version control and collaborative development

---

## 👩‍💻 Author

**M Gowthami**

B.Tech, Computer Science Engineering
IIITDM Jabalpur

