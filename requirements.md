# Aushadhi 360 - Requirements Specification

## Project Overview
Aushadhi 360 is an AI-powered healthcare ecosystem that connects patients, doctors, pharmacies, and vendors through an integrated platform with intelligent health management capabilities.

---

## 1. FUNCTIONAL REQUIREMENTS

### 1.1 Patient Mobile Application

#### 1.1.1 User Management
- FR-P-001: Users shall register using phone number, email, or social media accounts
- FR-P-002: System shall support multi-factor authentication (OTP, biometric)
- FR-P-003: Users shall create and manage health profiles for family members
- FR-P-004: System shall maintain complete medical history per profile
- FR-P-005: Users shall set privacy preferences for health data sharing

#### 1.1.2 Medical Reports Management
- FR-P-006: Users shall upload medical reports (PDF, images, DICOM)
- FR-P-007: System shall use OCR to extract data from scanned reports
- FR-P-008: Reports shall be categorized by type (lab, radiology, prescription, etc.)
- FR-P-009: Users shall search and filter reports by date, type, or doctor
- FR-P-010: System shall provide timeline view of health records
- FR-P-011: Users shall share reports securely with doctors via time-limited links
- FR-P-012: System shall support bulk upload and cloud sync

#### 1.1.3 AI Health Assistant
- FR-P-013: AI shall analyze uploaded medical reports using RAG architecture
- FR-P-014: AI shall provide health insights in user's preferred language
- FR-P-015: AI shall answer health-related queries based on user's medical history
- FR-P-016: System shall provide medication reminders and adherence tracking
- FR-P-017: AI shall detect abnormal values and alert users
- FR-P-018: System shall suggest preventive health measures
- FR-P-019: AI responses shall include disclaimer about consulting healthcare professionals
- FR-P-020: System shall maintain conversation history with AI assistant

#### 1.1.4 3D Virtual Doctor
- FR-P-021: System shall provide 3D avatar-based doctor consultation interface
- FR-P-022: 3D doctor shall use text-to-speech for voice responses
- FR-P-023: Users shall interact via text or voice input
- FR-P-024: 3D doctor shall demonstrate exercises, medication usage, or procedures
- FR-P-025: System shall support multiple avatar options (gender, language)
- FR-P-026: 3D doctor shall provide symptom assessment and triage
- FR-P-027: System shall record consultation summaries

#### 1.1.5 Emergency Services
- FR-P-028: Users shall access emergency button from any screen
- FR-P-029: System shall share real-time location with emergency contacts
- FR-P-030: System shall auto-dial emergency services (ambulance, hospital)
- FR-P-031: Emergency contacts shall receive SMS/push notifications with location
- FR-P-032: System shall share critical health info (blood type, allergies, conditions)
- FR-P-033: Users shall find nearest hospitals/pharmacies on map
- FR-P-034: System shall provide first-aid guidance for common emergencies
- FR-P-035: Emergency profile shall be accessible without login

#### 1.1.6 Appointments & Consultations
- FR-P-036: Users shall search doctors by specialty, location, rating
- FR-P-037: Users shall book in-person or video consultation appointments
- FR-D-011: Doctors shall mark slots as unavailable for leave/breaks
- FR-D-012: System shall manage waitlist for fully booked slots

#### 1.2.3 Patient Consultation
- FR-D-013: Doctors shall access patient medical history before consultation
- FR-D-014: Doctors shall conduct video consultations with recording option
- FR-D-015: Doctors shall view patient's uploaded reports during consultation
- FR-D-016: System shall provide AI-suggested diagnoses based on symptoms
- FR-D-017: Doctors shall create digital prescriptions with e-signature
- FR-D-018: Doctors shall add consultation notes and treatment plans
- FR-D-019: System shall support voice-to-text for quick note-taking
- FR-D-020: Doctors shall order lab tests or imaging directly

#### 1.2.4 Practice Management
- FR-D-021: Doctors shall view earnings dashboard (daily, monthly, yearly)
- FR-D-022: System shall generate invoices for consultations
- FR-D-023: Doctors shall track patient follow-ups and pending cases
- FR-D-024: System shall provide analytics on patient demographics and conditions
- FR-D-025: Doctors shall export patient data for research (anonymized)
- FR-D-026: Doctors shall manage clinic staff access and permissions

---

### 1.3 Medical Store Application

#### 1.3.1 Inventory Management
- FR-M-001: Store shall add medicines with batch number, expiry, MRP
- FR-M-002: System shall track stock levels in real-time
- FR-M-003: System shall alert when stock falls below threshold
- FR-M-004: Store shall scan barcodes for quick product entry
- FR-M-005: System shall track medicine expiry and alert 3 months before
- FR-M-006: Store shall categorize medicines (prescription, OTC, controlled)
- FR-M-007: System shall support multi-location inventory for chains
- FR-M-008: Store shall perform stock audits and reconciliation

#### 1.3.2 B2C Operations (Patient Orders)
- FR-M-009: Store shall receive patient orders with prescriptions
- FR-M-010: Pharmacist shall verify prescription validity
- FR-M-011: System shall check medicine availability and suggest alternatives
- FR-M-012: Store shall accept/reject orders based on stock
- FR-M-013: Store shall assign delivery personnel for home delivery
- FR-M-014: System shall generate bills with GST breakdown
- FR-M-015: Store shall process payments (cash, card, UPI, wallet)
- FR-M-016: System shall update inventory after order fulfillment

#### 1.3.3 B2B Operations (Vendor Orders)
- FR-M-017: Store shall browse vendor catalogs and place bulk orders
- FR-M-018: System shall compare prices across multiple vendors
- FR-M-019: Store shall track order status from vendors
- FR-M-020: System shall manage purchase orders and invoices
- FR-M-021: Store shall receive goods and update inventory
- FR-M-022: System shall handle returns and replacements with vendors
- FR-M-023: Store shall maintain vendor payment history

#### 1.3.4 Sales & Analytics
- FR-M-024: System shall generate daily sales reports
- FR-M-025: Store shall view top-selling and slow-moving medicines
- FR-M-026: System shall track profit margins per product
- FR-M-027: Store shall analyze customer purchase patterns
- FR-M-028: System shall forecast demand based on historical data
- FR-M-029: Store shall export reports for tax filing

---

### 1.4 Vendor Dashboard

#### 1.4.1 Product Management
- FR-V-001: Vendors shall register with business license and GST details
- FR-V-002: Vendors shall add products with specifications, pricing, MOQ
- FR-V-003: System shall support bulk product upload via CSV/Excel
- FR-V-004: Vendors shall set different prices for different buyer tiers
- FR-V-005: Vendors shall manage product catalogs by category
- FR-V-006: System shall track product certifications and compliance docs

#### 1.4.2 Order Management
- FR-V-007: Vendors shall receive orders from medical stores
- FR-V-008: System shall send real-time notifications for new orders
- FR-V-009: Vendors shall accept/reject orders based on availability
- FR-V-010: Vendors shall update order status (processing, shipped, delivered)
- FR-V-011: System shall generate shipping labels and invoices
- FR-V-012: Vendors shall manage returns and refunds
- FR-V-013: System shall track delivery performance metrics

#### 1.4.3 B2B Marketplace
- FR-V-014: Vendors shall view marketplace analytics (views, inquiries, orders)
- FR-V-015: System shall recommend products to stores based on demand
- FR-V-016: Vendors shall offer discounts and promotional campaigns
- FR-V-017: System shall support RFQ (Request for Quotation) process
- FR-V-018: Vendors shall communicate with stores via in-app messaging

#### 1.4.4 Financial Management
- FR-V-019: Vendors shall view earnings dashboard with payment status
- FR-V-020: System shall process payments with configurable settlement cycles
- FR-V-021: Vendors shall download invoices and tax reports
- FR-V-022: System shall calculate and display commission/platform fees

---

### 1.5 AI System

#### 1.5.1 RAG (Retrieval-Augmented Generation)
- FR-AI-001: System shall index medical literature, drug databases, and guidelines
- FR-AI-002: AI shall retrieve relevant context for user queries
- FR-AI-003: System shall use vector embeddings for semantic search
- FR-AI-004: AI shall cite sources for medical information provided
- FR-AI-005: System shall update knowledge base with latest medical research
- FR-AI-006: AI shall handle multi-turn conversations with context retention

#### 1.5.2 Report Analysis
- FR-AI-007: AI shall extract structured data from unstructured reports
- FR-AI-008: System shall identify abnormal lab values based on reference ranges
- FR-AI-009: AI shall detect trends in patient health metrics over time
- FR-AI-010: System shall generate plain-language summaries of complex reports
- FR-AI-011: AI shall correlate findings across multiple reports
- FR-AI-012: System shall support analysis of radiology images (X-ray, CT, MRI)

#### 1.5.3 Health Alerts & Predictions
- FR-AI-013: System shall generate alerts for critical health conditions
- FR-AI-014: AI shall predict disease risk based on patient history
- FR-AI-015: System shall recommend preventive screenings based on age/risk
- FR-AI-016: AI shall detect drug interactions and contraindications
- FR-AI-017: System shall alert doctors about patient deterioration patterns
- FR-AI-018: AI shall provide personalized health recommendations

#### 1.5.4 Natural Language Processing
- FR-AI-019: System shall support voice input in multiple languages
- FR-AI-020: AI shall understand medical terminology and colloquialisms
- FR-AI-021: System shall translate medical terms to layman language
- FR-AI-022: AI shall handle symptom descriptions and map to conditions

---

### 1.6 Admin Panel

#### 1.6.1 User Management
- FR-A-001: Admin shall view and manage all user accounts
- FR-A-002: Admin shall suspend/ban users for policy violations
- FR-A-003: System shall log all admin actions for audit trail
- FR-A-004: Admin shall assign roles and permissions to staff
- FR-A-005: Admin shall handle user complaints and disputes

#### 1.6.2 Content Moderation
- FR-A-006: Admin shall review and approve doctor registrations
- FR-A-007: Admin shall verify vendor business credentials
- FR-A-008: Admin shall moderate user reviews and ratings
- FR-A-009: System shall flag inappropriate content automatically
- FR-A-010: Admin shall manage platform policies and guidelines

#### 1.6.3 Analytics & Reporting
- FR-A-011: Admin shall view platform-wide usage statistics
- FR-A-012: System shall generate reports on transactions and revenue
