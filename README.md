# 📒 Serverless Notes API (AWS Lambda + DynamoDB + API Gateway)

A fully serverless REST API built using AWS Lambda, API Gateway, DynamoDB, and AWS SAM.  
This project demonstrates a complete CRUD backend using AWS cloud services.

---

## 🚀 Architecture

- API Gateway → Handles HTTP requests
- AWS Lambda → Business logic
- DynamoDB → NoSQL database
- AWS SAM → Infrastructure as Code

---

## 📌 Features

- Create a note
- Get all notes
- Get note by ID
- Update a note
- Delete a note
- Fully serverless architecture
- Auto scalable backend

---

## 🛠️ Tech Stack

- Node.js 20.x
- AWS Lambda
- Amazon API Gateway (REST API)
- Amazon DynamoDB
- AWS SAM
- AWS SDK v3

---

## 📂 Project Structure

serverless-notes-api/
│
├── hello-world/
│   ├── app.mjs              # Lambda handler (CRUD logic)
│   ├── package.json
│
├── template.yaml           # AWS SAM template
└── README.md

---

## ⚙️ Setup Instructions

### 1. Clone Repository
```bash
git clone <repo-url>
cd serverless-notes-api

### 2. Install Dependencies
```bash
cd hello-world
npm install

### 3. Build Project
```bash
cd ..
sam build

### 4. Deploy to AWS
```bash
sam deploy --guided

🌐 API Endpoints

Base URL:
https://9l3daljwd2.execute-api.ap-south-1.amazonaws.com/Prod/notes
