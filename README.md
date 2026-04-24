# Experiment 10: CRUD Operations on Database using Node.js + Express.js Backend

## 🎯 Objective
Build REST APIs using Node.js and Express.js to perform CRUD Operations (Create, Read, Update, Delete) on a database.

## 🧩 Features Implemented
1. **Create Record** - Add new student/user data into database
2. **Read Records** - Fetch all records and single record using ID
3. **Update Record** - Modify existing data using ID
4. **Delete Record** - Remove record using ID

## 💻 Tech Stack
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **CORS** - Cross-Origin Resource Sharing
- **Postman** - API Testing

## 📁 Project Structure
```
experiment10/
├── server.js
├── models/
│   └── Student.js
├── routes/
│   └── studentRoutes.js
├── package.json
└── README.md
```

## ⚙️ Installation & Setup
```bash
mkdir experiment10
cd experiment10
npm init -y
npm install express mongoose cors nodemon
```

## 🚀 Running the Project
```bash
nodemon server.js
```
Server runs on: `http://localhost:5000`

## 🧪 API Endpoints

### 1. Create Record
**POST** `/api/students`
```json
{
  "name": "Rahul",
  "email": "rahul@gmail.com",
  "course": "BCA"
}
```

### 2. Get All Records
**GET** `/api/students`

### 3. Get Single Record
**GET** `/api/students/:id`

### 4. Update Record
**PUT** `/api/students/:id`
```json
{
  "name": "Rahul Updated",
  "email": "rahul.updated@gmail.com",
  "course": "BCA"
}
```

### 5. Delete Record
**DELETE** `/api/students/:id`

## 📝 Implementation Details

### server.js
- Initializes Express application
- Sets up middleware (express.json, CORS)
- Connects to MongoDB using Mongoose
- Mounts student routes

### models/Student.js
- Defines Student schema with fields: name, email, course
- Creates and exports Student model

### routes/studentRoutes.js
- Implements all CRUD operations
- POST: Create new student record
- GET: Retrieve all or single student records
- PUT: Update student record by ID
- DELETE: Remove student record by ID

## 📸 Testing with Postman
1. Create a new request and select the HTTP method
2. Enter the endpoint URL (e.g., http://localhost:5000/api/students)
3. For POST/PUT requests, add JSON body
4. Send the request and view the response

## 🔧 Prerequisites
- MongoDB installed and running on port 27017
- Node.js and npm installed
- Postman or similar API testing tool

## ✅ Features Verified
✓ MongoDB connection message displayed  
✓ Create Record API working  
✓ Read All Records working  
✓ Read Single Record working  
✓ Update Record working  
✓ Delete Record working  
✓ Database collection created and data stored
