# 📒 Serverless Notes API

A fully serverless REST API built using **AWS Lambda**, **Amazon API Gateway**, **Amazon DynamoDB**, and **AWS SAM**. This project demonstrates a complete CRUD (Create, Read, Update, Delete) REST API deployed on AWS using a serverless architecture.

---

## 🚀 Architecture

```
Client
   │
   ▼
Amazon API Gateway
   │
   ▼
AWS Lambda
   │
   ▼
Amazon DynamoDB
```

---

## 📌 Features

- ✅ Create a note
- ✅ Get all notes
- ✅ Get a note by ID
- ✅ Update a note
- ✅ Delete a note
- ✅ Fully serverless architecture
- ✅ Infrastructure as Code using AWS SAM
- ✅ IAM-based DynamoDB access
- ✅ Environment variables for configuration

---

## 🛠️ Tech Stack

- Node.js 20.x
- AWS Lambda
- Amazon API Gateway (REST API)
- Amazon DynamoDB
- AWS SAM (Serverless Application Model)
- AWS SDK for JavaScript v3

---

## 📂 Project Structure

```
serverless-notes-api/
│
├── hello-world/
│   ├── app.mjs
│   ├── package.json
│   └── package-lock.json
│
├── events/
├── template.yaml
└── README.md
```

---

## ⚙️ Prerequisites

Before running this project, install:

- AWS CLI
- AWS SAM CLI
- Node.js 20.x or later
- An AWS Account

Configure AWS credentials:

```bash
aws configure
```

---

## 🚀 Installation

### Clone the repository

```bash
git clone <repository-url>
cd serverless-notes-api
```

### Install dependencies

```bash
cd hello-world
npm install
```

### Build the application

```bash
cd ..
sam build
```

### Deploy the application

```bash
sam deploy --guided
```

For future deployments:

```bash
sam deploy
```

---

## 🌐 API Endpoints

Replace `<api-id>` and `<region>` with your deployed API details.

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/notes` | Create a note |
| GET | `/notes` | Get all notes |
| GET | `/notes/{id}` | Get note by ID |
| PUT | `/notes/{id}` | Update note |
| DELETE | `/notes/{id}` | Delete note |

Example:

```
https://<api-id>.execute-api.<region>.amazonaws.com/Prod
```

> Example from this deployment:
>
> ```
> https://9l3daljwd2.execute-api.ap-south-1.amazonaws.com/Prod
> ```

---

## 📝 Create Note

**POST** `/notes`

Request Body

```json
{
  "title": "AWS Lambda",
  "content": "Serverless Notes API"
}
```

---

## 📖 Get All Notes

**GET** `/notes`

---

## 📖 Get Note By ID

**GET** `/notes/{id}`

---

## ✏️ Update Note

**PUT** `/notes/{id}`

Request Body

```json
{
  "title": "Updated Title",
  "content": "Updated Content"
}
```

---

## 🗑️ Delete Note

**DELETE** `/notes/{id}`

---

## 🗄️ DynamoDB Table

| Property | Value |
|----------|-------|
| Table Name | Notes |
| Primary Key | noteId (String) |

---

## 🔐 Environment Variables

| Variable | Value |
|----------|-------|
| TABLE_NAME | Notes |

---

## 🔑 IAM Policy

The Lambda function uses the following AWS SAM policy:

- `DynamoDBCrudPolicy`

---

## 🧪 Testing

You can test the API using:

- Postman
- curl
- API Gateway Console

Example:

```bash
curl https://<api-id>.execute-api.<region>.amazonaws.com/Prod/notes
```

---

## 📚 Learning Outcomes

This project demonstrates:

- Serverless application development
- AWS Lambda functions
- Amazon API Gateway REST APIs
- DynamoDB CRUD operations
- AWS SDK v3
- Environment Variables
- IAM Permissions
- AWS SAM deployment
- Infrastructure as Code (IaC)

---

## 🚀 Future Improvements

- Amazon Cognito Authentication
- Request validation
- Pagination
- File upload with Amazon S3
- CloudWatch logging enhancements
- CI/CD using AWS CodePipeline and CodeBuild

---

## 📄 License

This project is created for learning and demonstration purposes.

---

## 👩‍💻 Author

**Vaishnavi Pawar**

AWS Certified Developer – Associate (DVA-C02)
