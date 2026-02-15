# Aushadhi 360 – Requirements Document
## AI for Bharat Hackathon (Initial Phase – MVP)

## 1. Project Overview

Aushadhi 360 is an AI-powered healthcare ecosystem designed to connect patients, doctors, pharmacies, vendors, and delivery partners on a unified, secure platform.

This document outlines the functional and non-functional requirements for the initial phase (MVP) of the project.

---

## 2. Problem Statement

Healthcare systems in India are fragmented:
- Patients struggle to understand medical reports.
- Pharmacies face inventory mismanagement and expiry losses.
- Doctor access is limited and unstructured.
- No unified AI-enabled ecosystem connects all stakeholders.

---

## 3. Scope (Initial Phase – MVP)

The MVP will focus on:
- Patient report upload and AI summarization.
- Doctor appointment workflow.
- Pharmacy inventory management.
- Vendor-to-store medicine procurement.
- Secure cloud-based storage.
- AI-based early risk detection (basic rule-based + AI).

---

## 4. Functional Requirements

### 4.1 Patient Module
- User registration and authentication.
- Upload medical reports (PDF/Image).
- AI-based report summarization using RAG.
- View health insights dashboard.
- Book doctor appointments.
- Order medicines from nearby stores.

### 4.2 Doctor Module
- Secure login and verification workflow.
- Appointment management.
- Online consultation interface (chat/voice).
- Access patient-shared reports.

### 4.3 Pharmacy (Store Owner) Module
- Inventory management (add/update/delete medicines).
- Expiry and low-stock alerts.
- Billing system.
- Receive patient medicine orders.
- B2B procurement from vendors.

### 4.4 Vendor Module
- Vendor registration and verification.
- Upload medicine catalog.
- Supply medicines to pharmacies.
- Track B2B orders.

### 4.5 Delivery Partner Module
- Accept delivery requests.
- Track order status.
- Confirm delivery completion.

### 4.6 AI System
- RAG-based medical report summarization.
- Basic abnormal value detection.
- Chat-based health query handling.

---

## 5. Non-Functional Requirements

- Scalability using AWS serverless services.
- Secure storage of medical data.
- Role-based access control.
- Encryption of sensitive data.
- High availability and reliability.
- Modular and extensible architecture.

---

## 6. Assumptions

- AI suggestions are assistive and not a replacement for medical professionals.
- Initial deployment will be limited-scale for validation.
- Users must consent before sharing medical data.

---

## 7. Future Enhancements

- Advanced emergency detection.
- 3D AI virtual doctor.
- Real-time video consultation.
- Predictive health analytics.
- Nationwide vendor marketplace expansion.

