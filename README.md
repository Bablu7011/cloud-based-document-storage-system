# 🗂️ File Storage Web Application

A **secure cloud-based file storage system** built using **Flask**, **MongoDB**, and **AWS S3**.  
It allows users to upload, categorize, and manage their certificates and important documents safely in the cloud.

---

## 🚀 Overview

This project is a complete **document management platform** where users can:
- Upload certificates, licenses, and other important files.
- Categorize them (e.g., *Education*, *Job*, *Training*, etc.).
- View and manage uploaded files securely.
- Store files in **AWS S3** while keeping metadata in **MongoDB**.

It’s designed for scalability, security, and easy deployment.

---

## 🧱 Tech Stack

| Component | Technology Used |
|------------|------------------|
| **Backend** | Flask (Python) |
| **Database** | MongoDB  |
| **Cloud Storage** | AWS S3 |
| **Authentication** | Flask Sessions + Bcrypt |
| **Frontend** | HTML, CSS, Jinja2 Templates |
| **Environment Variables** | `.env` for credentials & configuration |

---

## ⚙️ Features

✅ **User Authentication**  
- Secure registration & login system using bcrypt for password hashing.  

✅ **File Upload to AWS S3**  
- Files are uploaded directly to your configured AWS S3 bucket.  

✅ **Metadata Storage in MongoDB**  
- Stores file information like name, category, upload time, and user reference.  

✅ **Category Management**  
- Predefined categories like Education, Job, Training, Certification, License, and Workshop.  
- Automatically created in MongoDB on startup.  

✅ **Dashboard UI**  
- Simple web interface (Flask templates) for users to view and manage their uploaded files.  

✅ **Secure Configuration**  
- Uses `.env` file for credentials such as `MONGO_URI`, `AWS_ACCESS_KEY_ID`, and `S3_BUCKET_NAME`.

---

## 📂 Project Structure

file-storage-source-code-main/
│
├── app.py # Main Flask application
├── requirements.txt # Python dependencies
├── .env # Environment variables (not committed to GitHub)
│
├── templates/ # Frontend HTML templates
│ ├── index.html
│ ├── login.html
│ ├── upload.html
│ └── dashboard.html
│
├── static/ # CSS, JS, and image files
│ ├── styles.css
│ └── scripts.js
│
└── README.md # Project documentation



---

## 🔧 Installation & Setup

### 1️⃣ Clone this Repository
```bash
git clone https://github.com/your-username/file-storage-source-code-main.git
cd file-storage-source-code-main
2️⃣ Create Virtual Environment


python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
3️⃣ Install Dependencies


pip install -r requirements.txt
4️⃣ Configure Environment Variables
Create a file named .env in the project root with the following values:


MONGO_URI=mongodb+srv://your-mongo-uri
AWS_ACCESS_KEY_ID=your-aws-access-key
AWS_SECRET_ACCESS_KEY=your-aws-secret-key
AWS_REGION=ap-south-1
S3_BUCKET_NAME=your-s3-bucket-name
5️⃣ Run the Application

python app.py
Then open your browser and visit:


http://127.0.0.1:5000
☁️ Deployment Notes
Ensure your AWS IAM user has s3:PutObject and s3:GetObject permissions.

MongoDB can be hosted using MongoDB Atlas.

You can deploy this Flask app on platforms like Render, Vercel, or AWS Elastic Beanstalk.

📸 Preview
Feature	Description
🏠 Home Page	           Overview of the application
🔐 Login / Register	   Secure authentication using bcrypt
☁️ Upload Files	           Upload files to AWS S3 with categories
📋 Dashboard	           View uploaded documents and metadata

🧠 How It Works (Simplified Flow)
User logs in or registers.

Chooses a file to upload → selects a category.

File is sent to AWS S3 → metadata stored in MongoDB.

Dashboard displays all uploaded files with details.

Users can view or manage their documents anytime.

💡 Future Enhancements
Role-based access (Admin/User)

File versioning and history tracking

Search and filtering by category/date

Email notifications on new uploads

🧑‍💻 Author
Developed by: Bablu Kumar
💼 GitHub: Bablu7011
📧 Email: bablukumar8520080@gmail.com

🪪 License
This project is licensed under the MIT License – feel free to modify and distribute.
