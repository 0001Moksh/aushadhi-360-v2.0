# Aushadhi 360 – System Design Document
## AI for Bharat Hackathon (Initial Phase – MVP)

---

## 1. Architecture Overview

Aushadhi 360 follows a serverless, cloud-native architecture built on AWS services to ensure scalability, security, and cost efficiency.

Frontend (Web/App)
    ↓
API Gateway
    ↓
AWS Lambda (Business Logic)
    ↓
Amazon Bedrock (AI Processing)
    ↓
DynamoDB (Metadata) + S3 (File Storage)

---

## 2. Technology Stack

### Frontend
- React / Next.js
- Role-based dashboards

### Backend
- AWS Lambda (Serverless functions)
- API Gateway (Secure API exposure)

### AI Layer
- Amazon Bedrock for:
  - Report summarization
  - RAG-based chatbot
  - Health insights generation

### Storage
- Amazon S3:
  - Medical reports
  - Documents
- Amazon DynamoDB:
  - User metadata
  - Appointments
  - Orders
  - Inventory data

### Security
- AWS IAM (Role-based access)
- Encryption at rest (S3)
- HTTPS for API communication

---

## 3. System Workflow (MVP)

1. Patient uploads report → stored in S3.
2. Lambda triggers AI summarization via Bedrock.
3. Summary stored in DynamoDB.
4. Patient views insights.
5. Patient books doctor appointment.
6. Doctor accesses shared report.
7. Prescription generated.
8. Patient orders medicine.
9. Store fulfills order.
10. Delivery partner completes delivery.

---

## 4. Data Flow

Patient → API Gateway → Lambda → Bedrock → Response  
Reports → S3  
Metadata → DynamoDB  
Orders → Store → Delivery Partner  

---

## 5. Design Principles

- Serverless-first approach.
- Modular role-based system.
- Secure data ownership.
- AI-assisted, human-supervised decisions.
- Scalable architecture.

---

## 6. Security & Privacy Model

- Role-based access control.
- Patient-controlled data sharing.
- Encrypted storage.
- Secure API authentication.
- Verified doctors and vendors.

---

## 7. Justification for AWS Usage

- Amazon Bedrock provides responsible, enterprise-grade AI.
- Lambda ensures cost-efficient scalability.
- S3 provides secure healthcare document storage.
- DynamoDB supports high-speed structured data management.
- API Gateway ensures secure and controlled access.


