# Lab 3: Architectural Pattern Selection & Component Diagram

**Student Name:** Harshitha Vangaveti  
**SRN:** PES2UG24AM064  
**Project:** Community Lost & Found Matching Network (`CLFMN`)  
**GitHub:** https://github.com/harshithaha12/Community-Lost-and-Found-Matching-Network  

---

## 1. Architectural Pattern Selection

### Evaluated Architectural Patterns
1. **Layered (3-Tier) Architecture:** High cohesion, separated presentation, business logic, and database.
2. **Microservices Architecture:** Independently deployable services communicating over HTTP/gRPC.
3. **Event-Driven Architecture:** Asynchronous message buses reacting to post events.

### Selected Pattern: 3-Tier Layered Architecture
- **Rationale:**
  - **Separation of Concerns:** Clearly decouples UI, business processing (tagging, matching, security questions), and persistent storage.
  - **Traceability to Requirements:** Directly aligns with Lab 1 requirements (FR-1 through FR-5) and NFRs (Security & Performance).
  - **Simplicity & Maintainability:** Minimizes network overhead and operational complexity compared to microservices, while guaranteeing strict data consistency for claim verifications.

---

## 2. Component Diagram Structure

### Layer 1: Presentation Layer
- **Report Management UI:** Interface for Finders and Owners to submit and track items.
- **Matching & Alerts UI:** Displays potential match notifications and spatial match radius.
- **Admin Console UI:** Dashboard for community moderators.

### Layer 2: Business Logic / Service Layer
- **Report Intake Service (FR-1):** Validates and stores item reports with active status.
- **Tag Extraction Component (FR-2):** Parses keywords, category, colour, and visual metadata.
- **Geo-Matching Engine (FR-3, NFR-2):** Computes proximity and attribute similarity scores.
- **Verification & Claim Component (FR-4, NFR-1):** Enforces private proof-of-ownership questions and locks fraudulent attempts.
- **Admin Moderation Component (FR-5):** Arbitrates disputes and manages flagged listings.

### Layer 3: Data Persistence Layer
- **Item Reports Database:** Relational storage for item listings and tags.
- **Spatial / Geo Index Store:** Optimizes location radius search.
- **Verification & User Store:** Encrypted store for user credentials, private questions, and audit logs.
