# 🏥 TopDoctorsJaipur – Online Appointment & Review System

## 📌 Project Overview

**TopDoctorsJaipur** is a full-stack web application developed as part of the MCA 4th semester Industrial Training Project. It allows users to book appointments with doctors online and submit reviews based on their experience. The system uses a client-server architecture with MySQL as the backend database.

---

## 🚀 Features

- 🔹 Book doctor appointments online
- 🔹 Submit patient reviews with location
- 🔹 Responsive UI with modern layout
- 🔹 MySQL database integration
- 🔹 RESTful APIs using Express.js
- 🔹 Doctor listing and patient forms

---

## 🛠️ Technology Stack

- **Frontend:** React.js, HTML5, CSS3, JavaScript
- **Backend:** Node.js, Express.js
- **Database:** MySQL
- **Libraries:** Axios, dotenv, CORS, MySQL2

---

## 🗂️ Folder Structure

```
TopDoctorsJaipur/
│
├── Client/               # React frontend
│   └── public/
│   └── src/
│       ├── Assets/
│       ├── Components/
│       ├── Pages/
│       ├── Scripts/
│       ├── Styles/
│       └── App.js
│
├── Server/               # Node + Express backend
│   ├── index.js
│   ├── db.sql
│   └── .env
│
├── README.md
├── package.json (both Client & Server)
```

---

## 📋 Database Structure

### 1. `appointments` Table

| Field            | Type         |
|------------------|--------------|
| id               | INT (PK)     |
| patient_name     | VARCHAR(100) |
| patient_number   | VARCHAR(15)  |
| patient_gender   | VARCHAR(10)  |
| appointment_time | DATETIME     |
| doctor_name      | VARCHAR(100) |
| created_at       | TIMESTAMP    |

### 2. `reviews` Table

| Field      | Type          |
|------------|---------------|
| id         | INT (PK)      |
| name       | VARCHAR(255)  |
| location   | VARCHAR(255)  |
| message    | TEXT          |
| created_at | TIMESTAMP     |

---

## 🛠️ SQL Setup

```sql
CREATE DATABASE topjaipurdoctor;

CREATE TABLE appointments (
  id INT AUTO_INCREMENT PRIMARY KEY,
  patient_name VARCHAR(100),
  patient_number VARCHAR(15),
  patient_gender VARCHAR(10),
  appointment_time DATETIME,
  doctor_name VARCHAR(100),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
CREATE TABLE reviews (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  location VARCHAR(255) NOT NULL,
  message TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


```

---

## 🔗 API Endpoints

### ➤ `POST /api/appointments`  
Save a new appointment to the database.

### ➤ `POST /api/reviews`  
Save a patient review to the database.

---

## ⚙️ Setup Instructions

### 🔧 Prerequisites:
- Node.js
- MySQL

### 🖥️ React Frontend:
```bash
npx create-react-app topjaipurdoctor
cd topjaipurdoctor
npm start
```

### 🖧 Backend Setup:
1. Create a `.env` file:
```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=topjaipurdoctor
PORT=5000
```

2. Start server:
```bash
node index.js
```

---

## 👨‍💻 Developed By

**Mohammad Danish**  
MCA (4th Semester)  
Rajasthan Technical University  
📧 khandanishindia04@gmail.com  
📱 8920424789

---

## 📜 License

This project is developed for academic purposes only.  
**All rights reserved © 2023–2025 by Mohammad Danish, MCA, RTU.**