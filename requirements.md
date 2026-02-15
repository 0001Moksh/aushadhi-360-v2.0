# Aushadhi 360 – Requirements Document
## AI for Bharat Hackathon (Initial Phase – MVP)

## 1. Project Overview

Aushadhi 360 is an AI-powered healthcare ecosystem designed to connect patients, doctors, pharmacies, vendors, and delivery partners on a unified, secure platform.

This document outlines the functional and non-functional requirements for the initial phase (MVP) of the project.

### 1.1 Success Metrics
- 100+ active users within first month
- <3 second average response time for AI summarization
- 99.5% uptime for critical services
- Zero data breaches or unauthorized access incidents
- 90% user satisfaction score

---

## 2. Problem Statement

Healthcare systems in India are fragmented:
- Patients struggle to understand medical reports.
- Pharmacies face inventory mismanagement and expiry losses.esign” flow to convert a natural language idea into the requirements.md and design.md artefacts.
Export the two files (Kiro export). If a team wants to refine the specs, they can iteratively prompt Kiro and re-export.
Upload the generated requirement
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

#### 4.1.1 User Registration and Authentication
**Priority:** P0 (Critical)

**User Story:** As a patient, I want to register and securely log in so that I can access my health records and services.

**Acceptance Criteria:**
- Patient can register with email/phone number
- OTP-based verification is required
- Password must meet security standards (min 8 chars, alphanumeric + special char)
- Session expires after 30 minutes of inactivity
- Multi-factor authentication option available
- User receives confirmation email/SMS upon successful registration

#### 4.1.2 Medical Report Upload
**Priority:** P0 (Critical)

**User Story:** As a patient, I want to upload my medical reports so that I can get AI-powered insights.

**Acceptance Criteria:**
- Supports PDF and image formats (JPG, PNG)
- Maximum file size: 10MB per upload
- OCR processing for scanned images
- Upload progress indicator shown
- Uploaded files are encrypted at rest
- User can view upload history
- Failed uploads show clear error messages

#### 4.1.3 AI Report Summarization
**Priority:** P0 (Critical)

**User Story:** As a patient, I want AI to summarize my medical reports so that I can understand them easily.

**Acceptance Criteria:**
- Summary generated within 5 seconds for standard reports
- Summary includes key findings, abnormal values, and recommendations
- Medical terminology explained in simple language
- Confidence score displayed for AI interpretations
- Disclaimer shown that AI is assistive, not diagnostic
- User can request detailed explanation for specific sections
- Summary available in English and Hindi

#### 4.1.4 Health Insights Dashboard
**Priority:** P1 (High)

**User Story:** As a patient, I want to view my health trends over time so that I can track my progress.

**Acceptance Criteria:**
- Dashboard shows key health metrics (blood pressure, sugar levels, etc.)
- Trend graphs for tracked parameters
- Color-coded alerts for abnormal values
- Historical data accessible for past 12 months
- Export data as PDF report
- Dashboard loads within 2 seconds

#### 4.1.5 Doctor Appointment Booking
**Priority:** P1 (High)

**User Story:** As a patient, I want to book appointments with doctors so that I can get professional consultation.

**Acceptance Criteria:**
- Search doctors by specialty, location, availability
- View doctor profiles with ratings and experience
- Select available time slots
- Receive booking confirmation via email/SMS
- Option to cancel/reschedule up to 2 hours before appointment
- Reminder sent 24 hours and 1 hour before appointment
- Can share specific reports with doctor during booking

#### 4.1.6 Medicine Ordering
**Priority:** P2 (Medium)

**User Story:** As a patient, I want to order medicines from nearby pharmacies so that I can get them delivered.

**Acceptance Criteria:**
- Search medicines by name or upload prescription
- View available pharmacies within 5km radius
- Compare prices across pharmacies
- Add multiple medicines to cart
- Choose delivery or pickup option
- Track order status in real-time
- Prescription verification for scheduled drugs

### 4.2 Doctor Module

#### 4.2.1 Doctor Registration and Verification
**Priority:** P0 (Critical)

**User Story:** As a doctor, I want to register with my credentials so that I can provide verified consultations.

**Acceptance Criteria:**
- Registration requires medical license number
- Upload medical degree certificates
- Verification process completed within 48 hours
- Profile includes specialty, experience, qualifications
- Can set consultation fees and availability
- Email notification upon verification approval/rejection

#### 4.2.2 Appointment Management
**Priority:** P0 (Critical)

**User Story:** As a doctor, I want to manage my appointments so that I can organize my schedule efficiently.

**Acceptance Criteria:**
- View daily/weekly/monthly appointment calendar
- Accept or decline appointment requests
- Set available time slots and working hours
- Block specific dates for unavailability
- Receive notifications for new appointment requests
- Can reschedule appointments with patient consent
- View patient basic info before appointment

#### 4.2.3 Online Consultation Interface
**Priority:** P1 (High)

**User Story:** As a doctor, I want to conduct online consultations so that I can provide remote healthcare.

**Acceptance Criteria:**
- Secure chat interface with end-to-end encryption
- Voice call option with clear audio quality
- Consultation session auto-starts at scheduled time
- Can access patient's shared medical reports during consultation
- Option to prescribe medicines digitally
- Consultation notes saved automatically
- Session recording available (with consent)

#### 4.2.4 Patient Report Access
**Priority:** P1 (High)

**User Story:** As a doctor, I want to access patient-shared reports so that I can provide informed consultation.

**Acceptance Criteria:**
- View only reports explicitly shared by patient
- Reports displayed with AI summary and original document
- Can download reports for offline review
- Access logs maintained for audit purposes
- Reports organized chronologically
- Search functionality within patient's report history

### 4.3 Pharmacy (Store Owner) Module

#### 4.3.1 Inventory Management
**Priority:** P0 (Critical)

**User Story:** As a pharmacy owner, I want to manage my medicine inventory so that I can track stock levels efficiently.

**Acceptance Criteria:**
- Add new medicines with details (name, batch, expiry, quantity, price)
- Update stock quantities on sales/procurement
- Delete discontinued medicines
- Bulk upload via CSV/Excel
- Search and filter medicines by name, category, manufacturer
- View current stock value
- Inventory sync across multiple store locations (if applicable)

#### 4.3.2 Expiry and Low-Stock Alerts
**Priority:** P0 (Critical)

**User Story:** As a pharmacy owner, I want automated alerts for expiring and low-stock medicines so that I can prevent losses.

**Acceptance Criteria:**
- Alert when medicine expires within 60 days
- Alert when stock falls below defined threshold
- Daily summary email of expiring/low-stock items
- In-app notification badge
- Configurable alert thresholds per medicine
- Generate expiry report for tax/compliance purposes

#### 4.3.3 Billing System
**Priority:** P1 (High)

**User Story:** As a pharmacy owner, I want a billing system so that I can process customer purchases efficiently.

**Acceptance Criteria:**
- Scan/search medicines to add to bill
- Apply discounts and offers
- Multiple payment methods (cash, card, UPI)
- Generate GST-compliant invoice
- Print/email invoice to customer
- Daily sales report generation
- Integration with inventory for auto stock deduction

#### 4.3.4 Patient Medicine Orders
**Priority:** P1 (High)

**User Story:** As a pharmacy owner, I want to receive and fulfill patient medicine orders so that I can expand my business.

**Acceptance Criteria:**
- Receive order notifications in real-time
- View order details with prescription (if applicable)
- Accept or reject orders based on availability
- Update order status (processing, ready, dispatched)
- Assign delivery partner for home delivery
- Track order completion and payment
- Customer rating and feedback visible

#### 4.3.5 B2B Vendor Procurement
**Priority:** P2 (Medium)

**User Story:** As a pharmacy owner, I want to order medicines from vendors so that I can restock inventory.

**Acceptance Criteria:**
- Browse vendor catalogs
- Search medicines by name/category
- Compare prices across vendors
- Place bulk orders
- Track order status from vendor
- Receive delivery confirmation
- Update inventory automatically upon delivery

### 4.4 Vendor Module

#### 4.4.1 Vendor Registration and Verification
**Priority:** P1 (High)

**User Story:** As a medicine vendor, I want to register on the platform so that I can supply to pharmacies.

**Acceptance Criteria:**
- Registration with business details (GST, drug license)
- Upload business registration documents
- Verification within 72 hours
- Profile includes company info, certifications, service areas
- Email notification upon approval

#### 4.4.2 Medicine Catalog Management
**Priority:** P1 (High)

**User Story:** As a vendor, I want to upload and manage my medicine catalog so that pharmacies can order from me.

**Acceptance Criteria:**
- Add medicines with details (name, manufacturer, price, MOQ)
- Bulk upload via CSV
- Update prices and availability
- Categorize medicines by type
- Set minimum order quantities
- Mark medicines as out of stock

#### 4.4.3 B2B Order Management
**Priority:** P1 (High)

**User Story:** As a vendor, I want to manage pharmacy orders so that I can fulfill them efficiently.

**Acceptance Criteria:**
- Receive order notifications
- View order details with pharmacy information
- Accept/reject orders based on availability
- Update order status (confirmed, dispatched, delivered)
- Generate invoice for pharmacy
- Track payment status
- View order history and analytics

#### 4.4.4 Supply Chain Tracking
**Priority:** P2 (Medium)

**User Story:** As a vendor, I want to track my deliveries so that I can ensure timely fulfillment.

**Acceptance Criteria:**
- Assign delivery partner/logistics
- Update delivery status
- Estimated delivery time shown
- Delivery confirmation with signature/photo
- Failed delivery handling workflow

### 4.5 Delivery Partner Module

#### 4.5.1 Delivery Partner Registration
**Priority:** P2 (Medium)

**User Story:** As a delivery partner, I want to register so that I can accept delivery jobs.

**Acceptance Criteria:**
- Registration with personal details and vehicle info
- Upload driving license and vehicle documents
- Background verification
- Set service areas and availability
- Approval within 48 hours

#### 4.5.2 Delivery Request Management
**Priority:** P2 (Medium)

**User Story:** As a delivery partner, I want to accept delivery requests so that I can earn income.

**Acceptance Criteria:**
- Receive nearby delivery requests based on location
- View delivery details (pickup, drop, distance, payment)
- Accept or decline requests
- Navigate to pickup and delivery locations
- Multiple delivery batching option
- Earnings tracker

#### 4.5.3 Order Status Tracking
**Priority:** P2 (Medium)

**User Story:** As a delivery partner, I want to update order status so that customers can track their delivery.

**Acceptance Criteria:**
- Update status (picked up, in transit, delivered)
- Real-time location sharing during delivery
- Upload delivery proof (photo/signature)
- Handle failed delivery scenarios
- Customer contact option (call/chat)
- Delivery completion confirmation

### 4.6 AI System

#### 4.6.1 RAG-Based Medical Report Summarization
**Priority:** P0 (Critical)

**User Story:** As the system, I want to use RAG to summarize medical reports so that patients get accurate insights.

**Acceptance Criteria:**
- Extract text from PDF/images using OCR
- Identify key medical parameters (blood tests, vitals, diagnoses)
- Generate summary with key findings and abnormalities
- Provide context from medical knowledge base
- Response time <5 seconds for standard reports
- Accuracy rate >90% for parameter extraction
- Handle multiple report formats (lab tests, radiology, prescriptions)

#### 4.6.2 Abnormal Value Detection
**Priority:** P0 (Critical)

**User Story:** As the system, I want to detect abnormal medical values so that patients are alerted to potential health risks.

**Acceptance Criteria:**
- Compare values against standard reference ranges
- Flag values outside normal range
- Consider age, gender, and other factors
- Severity classification (mild, moderate, severe)
- Suggest follow-up actions
- Maintain database of reference ranges
- Update detection rules based on medical guidelines

#### 4.6.3 Health Query Chatbot
**Priority:** P1 (High)

**User Story:** As a patient, I want to ask health-related questions so that I can get quick information.

**Acceptance Criteria:**
- Natural language understanding
- Context-aware responses based on user's health data
- Provide general health information
- Redirect to doctor for serious concerns
- Response time <2 seconds
- Disclaimer shown for all medical advice
- Support English and Hindi languages
- Conversation history maintained

#### 4.6.4 Early Risk Detection
**Priority:** P2 (Medium)

**User Story:** As the system, I want to detect early health risks so that patients can take preventive action.

**Acceptance Criteria:**
- Analyze trends in health parameters over time
- Identify patterns indicating potential risks
- Risk scoring for common conditions (diabetes, hypertension)
- Personalized health recommendations
- Alert patient and suggest doctor consultation
- Explainable AI - show reasoning for risk assessment

---

## 5. Non-Functional Requirements

### 5.1 Performance
**Acceptance Criteria:**
- API response time <500ms for 95% of requests
- AI summarization completes within 5 seconds
- Dashboard loads within 2 seconds
- Support 1000 concurrent users
- Database query response time <100ms
- File upload speed: 1MB per second minimum

### 5.2 Scalability
**Acceptance Criteria:**
- Horizontal scaling using AWS serverless (Lambda, ECS)
- Auto-scaling based on load (CPU >70%)
- Database supports 100,000+ records per table
- CDN for static assets (CloudFront)
- Microservices architecture for independent scaling
- Load balancer distributes traffic across instances

### 5.3 Security
**Acceptance Criteria:**
- All data encrypted at rest (AES-256)
- Data encrypted in transit (TLS 1.3)
- Role-based access control (RBAC) implemented
- JWT-based authentication with refresh tokens
- Session timeout after 30 minutes inactivity
- Password hashing using bcrypt (cost factor 12)
- API rate limiting (100 requests/minute per user)
- Regular security audits and penetration testing
- HIPAA/DISHA compliance for medical data
- Audit logs for all sensitive operations

### 5.4 Availability and Reliability
**Acceptance Criteria:**
- 99.5% uptime SLA
- Multi-AZ deployment for high availability
- Automated backups every 6 hours
- Point-in-time recovery capability
- Disaster recovery plan with RTO <4 hours
- Health checks and monitoring (CloudWatch)
- Automated failover for critical services
- Circuit breaker pattern for external dependencies

### 5.5 Maintainability
**Acceptance Criteria:**
- Modular microservices architecture
- Comprehensive API documentation (OpenAPI/Swagger)
- Code coverage >80% for unit tests
- Automated CI/CD pipeline
- Infrastructure as Code (Terraform/CloudFormation)
- Centralized logging (CloudWatch Logs)
- Monitoring and alerting (CloudWatch Alarms)
- Version control for all code and configurations

### 5.6 Usability
**Acceptance Criteria:**
- Mobile-responsive design (works on 320px+ screens)
- Accessibility compliance (WCAG 2.1 Level AA target)
- Multi-language support (English, Hindi)
- Intuitive UI with <3 clicks to key features
- Consistent design system across modules
- Help documentation and tooltips
- Error messages are clear and actionable

### 5.7 Compliance and Legal
**Acceptance Criteria:**
- DISHA (Digital Information Security in Healthcare Act) compliance
- User consent required before data sharing
- Data retention policy (7 years for medical records)
- Right to data deletion (GDPR-style)
- Terms of service and privacy policy displayed
- Age verification (18+ or parental consent)
- Medical disclaimer on all AI-generated content

---

## 6. Technical Constraints

### 6.1 Technology Stack
- Frontend: React.js or Next.js
- Backend: Node.js with Express or Python with FastAPI
- Database: PostgreSQL (RDS) for relational data, DynamoDB for NoSQL
- AI/ML: OpenAI API, LangChain for RAG, Hugging Face models
- Cloud: AWS (Lambda, S3, RDS, API Gateway, CloudFront)
- Authentication: AWS Cognito or Auth0
- File Storage: AWS S3 with encryption
- Monitoring: CloudWatch, Sentry for error tracking

### 6.2 Integration Requirements
- Payment gateway integration (Razorpay/Stripe)
- SMS/Email service (AWS SNS/SES or Twilio)
- Maps API for location services (Google Maps/Mapbox)
- OCR service for document processing (AWS Textract)
- Video calling (Twilio/Agora for future)

### 6.3 Data Requirements
- Medical reports stored for 7 years minimum
- User data backup retention: 30 days
- Audit logs retention: 1 year
- Maximum file upload size: 10MB
- Supported file formats: PDF, JPG, PNG
- Database backup frequency: Every 6 hours

## 7. Assumptions and Dependencies

### 7.1 Assumptions
- AI suggestions are assistive and not a replacement for medical professionals
- Initial deployment will be limited-scale for validation
- Users must consent before sharing medical data
- Users have access to smartphones or computers with internet
- Medical professionals have valid licenses and credentials
- Pharmacies have basic inventory management processes
- Vendors are registered businesses with proper licenses

### 7.2 Dependencies
- AWS account with appropriate service limits
- OpenAI API access for AI features
- Third-party API availability (payment, SMS, maps)
- Medical knowledge base for RAG system
- Reference ranges database for abnormal value detection
- User adoption and engagement
- Regulatory approvals for healthcare platform

## 8. Out of Scope (MVP)

The following features are explicitly out of scope for the MVP:
- Real-time video consultation (voice only in MVP)
- 3D AI virtual doctor
- Advanced predictive analytics and ML models
- Nationwide vendor marketplace (limited geography in MVP)
- Mobile native apps (web-responsive only)
- Integration with hospital EMR systems
- Insurance claim processing
- Telemedicine prescription delivery to government databases
- Multi-currency support (INR only)
- Wearable device integration

---

## 9. Future Enhancements

## 9. Future Enhancements

### Phase 2 (Post-MVP)
- Real-time video consultation with screen sharing
- 3D AI virtual doctor with voice interaction
- Advanced emergency detection with ambulance integration
- Predictive health analytics using ML models
- Wearable device integration (fitness trackers, smartwatches)
- Hospital EMR system integration
- Insurance claim processing automation

### Phase 3 (Long-term)
- Nationwide vendor marketplace expansion
- Multi-language support (10+ Indian languages)
- Blockchain for medical record security
- AI-powered drug interaction checker
- Mental health support module
- Chronic disease management programs
- Health insurance marketplace integration

---

## 10. Glossary

- **RAG:** Retrieval-Augmented Generation - AI technique combining retrieval and generation
- **OCR:** Optical Character Recognition - converting images to text
- **RBAC:** Role-Based Access Control - permission system based on user roles
- **JWT:** JSON Web Token - authentication token format
- **HIPAA:** Health Insurance Portability and Accountability Act
- **DISHA:** Digital Information Security in Healthcare Act (India)
- **MVP:** Minimum Viable Product
- **SLA:** Service Level Agreement
- **RTO:** Recovery Time Objective
- **MOQ:** Minimum Order Quantity
- **B2B:** Business-to-Business
- **EMR:** Electronic Medical Records