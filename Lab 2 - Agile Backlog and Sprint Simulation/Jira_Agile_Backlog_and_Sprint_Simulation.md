# Lab 2: Jira Hands-on — Agile Backlog Creation & Sprint Simulation

**Student Name:** Harshitha Vangaveti  
**SRN:** PES2UG24AM064  
**Project Name:** Community Lost & Found Matching Network  
**Project Key:** `CLFMN`  
**Jira Board URL:** https://harshivangaveti.atlassian.net/jira/software/projects/CLFMN/boards/35/backlog  
**GitHub Repository:** https://github.com/harshithaha12/Community-Lost-and-Found-Matching-Network  

---

## 1. Problem Context & Traceability Matrix (Lab 1 to Lab 2)

Based on the requirements established in **Lab 1 (Requirements Engineering)**, the requirements are translated into Agile Epics, User Stories, and Tasks:

| Lab 1 Requirement | Agile Work Item | Summary | Story Points | Sprint |
|:---|:---|:---|:---:|:---:|
| **FR-1** | User Story (US-01) | Create Lost and Found Item Reports with location & image | 5 | Sprint 1 |
| **FR-2** | User Story (US-02) | Automated visual and text tag extraction from reports | 5 | Sprint 1 |
| **FR-3 & NFR-2** | User Story (US-03) | Proximity and attribute-based matching engine | 8 | Sprint 2 |
| **FR-4 & NFR-1** | User Story (US-04) | Security question verification for ownership proof | 5 | Sprint 2 |
| **FR-5** | User Story (US-05) | Admin report moderation and dispute management | 3 | Sprint 2 |

---

## 2. Epics Definition

### EPIC 1: Item Reporting & Automated Tagging (`CLFMN-EP1`)
- **Summary:** End-to-end capture of lost and found listings with automated tag generation.
- **Includes:** US-01, US-02

### EPIC 2: Proximity Matching & Verification Engine (`CLFMN-EP2`)
- **Summary:** Intelligent geo-proximity matching and anti-fraud proof of ownership verification.
- **Includes:** US-03, US-04

### EPIC 3: Community Administration & Moderation (`CLFMN-EP3`)
- **Summary:** Administrative workflows for report approval, rejection, and dispute handling.
- **Includes:** US-05

---

## 3. Product Backlog: User Stories & Acceptance Criteria

### User Story 1 (US-01): Create Lost and Found Reports
- **Epic:** Item Reporting & Automated Tagging
- **Priority:** High
- **Story Points:** 5
- **User Story:**
  > *As a Finder or Owner,*  
  > *I want to log a detailed Lost or Found item report with item characteristics, date, location, and optional photos,*  
  > *So that the item is catalogued on the network for matching.*
- **Acceptance Criteria:**
  - **Pass:** The report is saved with a unique ID and `Active` status.
  - **Pass:** Mandatory fields (item name, category, date, geo-location) are validated.
  - **Fail:** Incomplete or corrupted submissions display clear validation errors.

---

### User Story 2 (US-02): Automated Tag Extraction
- **Epic:** Item Reporting & Automated Tagging
- **Priority:** High
- **Story Points:** 5
- **User Story:**
  > *As a System / User,*  
  > *I want the system to extract keywords, category, colour, and visual attributes automatically,*  
  > *So that reports are indexed accurately without requiring manual exhaustive tagging.*
- **Acceptance Criteria:**
  - **Pass:** Category, colour, brand, and prominent keywords are tagged to the report.
  - **Pass:** User can review and edit auto-extracted tags before submission.
  - **Fail:** Corrupted or unrecognized image formats are handled with a fallback to manual tagging.

---

### User Story 3 (US-03): Geo-Proximity & Attribute Matching Engine
- **Epic:** Proximity Matching & Verification Engine
- **Priority:** High
- **Story Points:** 8
- **User Story:**
  > *As a Lost Item Owner,*  
  > *I want the system to match my report against active Found items within a defined geographical radius,*  
  > *So that I am promptly alerted to high-probability matches.*
- **Acceptance Criteria:**
  - **Pass:** Computes similarity score across category, tags, colour, and GPS distance.
  - **Pass:** Response time remains under 2 seconds under peak load (NFR-2).
  - **Fail:** Incompatible item categories (e.g., electronics vs. clothing) are never matched together.

---

### User Story 4 (US-04): Proof of Ownership Security Verification
- **Epic:** Proximity Matching & Verification Engine
- **Priority:** High
- **Story Points:** 5
- **User Story:**
  > *As an Item Finder,*  
  > *I want claimants to answer private security questions set by me before handover details are displayed,*  
  > *So that fraudulent claims are prevented and privacy is protected.*
- **Acceptance Criteria:**
  - **Pass:** Correct answers unlock the finder's handover contact details.
  - **Pass:** Contact information and answers remain strictly encrypted/masked prior to verification (NFR-1).
  - **Fail:** Incorrect attempts exceeding 3 tries lock the claim and alert the user.

---

### User Story 5 (US-05): Admin Moderation & Dispute Handling
- **Epic:** Community Administration & Moderation
- **Priority:** Medium
- **Story Points:** 3
- **User Story:**
  > *As a Community Administrator,*  
  > *I want an admin console to review, approve, reject reports, and arbitrate contested claims,*  
  > *So that the network remains safe, accurate, and free of spam.*
- **Acceptance Criteria:**
  - **Pass:** Admin can change report status (`Active`, `Suspended`, `Resolved`).
  - **Pass:** Disputed items are flagged for human review with uploaded verification evidence.
  - **Fail:** Unauthorized regular users cannot access administrative endpoints.

---

## 4. Sprint Simulation

### Sprint 1: Core Item Reporting & Tag Extraction
- **Sprint Goal:** Establish the baseline reporting flow and automated tagging mechanism.
- **Duration:** 2 Weeks (Simulated)
- **Committed Story Points:** 10 Points
- **Items in Sprint 1:**
  1. `CLFMN-1`: US-01 — Create Lost and Found Reports (5 pts) — **Status: DONE**
  2. `CLFMN-2`: US-02 — Automated Tag Extraction (5 pts) — **Status: DONE**
- **Simulation Outcome:** Sprint completed successfully. Reporting UI and Tagging pipeline functional.

### Sprint 2: Proximity Matching, Verification & Administration
- **Sprint Goal:** Deliver automated matching, fraud-prevention security questions, and admin moderation.
- **Duration:** 2 Weeks (Simulated)
- **Committed Story Points:** 16 Points
- **Items in Sprint 2:**
  1. `CLFMN-3`: US-03 — Geo-Proximity & Attribute Matching Engine (8 pts) — **Status: IN PROGRESS**
  2. `CLFMN-4`: US-04 — Proof of Ownership Security Verification (5 pts) — **Status: IN PROGRESS**
  3. `CLFMN-5`: US-05 — Admin Moderation & Dispute Handling (3 pts) — **Status: TO DO**
