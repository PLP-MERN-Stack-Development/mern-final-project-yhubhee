# HealingNet Telemedicine App

HealingNet is a full-featured telemedicine platform that connects patients with doctors for online consultations, appointment booking, and medical record management.

---

## 🚀 Project Description

HealingNet allows users to:

- Register as a patient or doctor
- Book and manage appointments
- Conduct online consultations
- Access patient medical records securely
- Receive notifications and updates

This project is built with **Node.js, Express, and SQL (MySQL/PostgreSQL)** and deployed online for real-time use. I haven't really mastered REACT so i built it on a module i'm stable. 

---

## ⚙️ Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd healingnet

2. **Install the dependencies**
npm install

3. **Configure environment variables**
Create a .env file at the root
Add the following:
DB_HOST=<your-database-host>
DB_USER=<your-database-username>
DB_PASSWORD=<your-database-password>
DB_NAME=<your-database-name>
PORT=5000

4. **Run the backend**
npm start

6. **Access the application**
Backend API: http://localhost:4000

**🎥 Video Demonstration**

Watch a 5-10 minute walkthrough of HealingNet:
link: https://drive.google.com/file/d/1wYlR06CgBjLPSmFYcnJ6DjOixbubdhu0/view?usp=drive_link


**💻 Technologies Used**

Backend: Node.js, Express

Database: SQL (MySQL)

Authentication: JWT

Deployment: render

**🗄️ Database Schema**
Tables and Relationships:

patients – stores patient information

admins – stores admin users

doctors – stores doctor profiles, linked to admins

appointment – stores appointment details, linked to patients and doctors

prescription – stores prescriptions for patients, linked to doctors

doctor_schedules – stores doctor availability

token_blacklist – stores invalidated JWT tokens

Foreign keys enforce relationships:
doctors.admin_id → admins.admin_id
appointment.patient_id → patients.patient_id
appointment.doctor_id → doctors.doctor_id
prescription.patient_id → patients.patient_id
prescription.doctor_id → doctors.doctor_id
doctor_schedules.doctor_id → doctors.doctor_id