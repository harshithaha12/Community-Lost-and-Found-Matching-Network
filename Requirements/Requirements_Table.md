# Requirements Table

## Problem Statement #59
### Community Lost & Found Matching Network


| ID          | Type               | Description                                                                                                                  | Priority | Acceptance Criteria                                                                         | Rationale                                           |
| ----------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------------- | -------- | ------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| **FR-001**  | Functional         | Allow Finder/Owner to create Lost/Found reports with item details, location, date and optional image.                        | High     | Valid report receives unique ID and Active status; invalid/incomplete reports are rejected. | Reports are the primary input to the system.        |
| **FR-002**  | Functional         | Extract visual/text tags such as category, colour, brand and keywords from item information and images.                      | High     | Relevant tags are extracted and associated with the report.                                 | Tags improve matching accuracy.                     |
| **FR-003**  | Functional         | Match Lost and Found reports using category, tags, colour and geographical proximity.                                        | High     | Compatible reports receive a match score; incompatible reports are not matched.             | Automated matching speeds up item recovery.         |
| **FR-004**  | Functional         | Allow Finder to create private ownership questions and require claimants to answer them before contact details are revealed. | High     | Correct answers allow verification; incorrect answers prevent contact access.               | Prevents fraudulent claims.                         |
| **FR-005**  | Functional         | Allow Community Admin to review, approve, reject, remove reports and manage disputed claims.                                 | Medium   | Authorized administrative actions update report status correctly.                           | Maintains platform reliability and prevents misuse. |
| **NFR-001** | Security & Privacy | Protect verification questions, answers and contact information from unauthorized access.                                    | High     | Unauthorized users cannot access protected information before verification.                 | Protects user privacy and ownership evidence.       |
| **NFR-002** | Performance        | Process matching and display potential matches within the defined response-time target under normal and peak load.           | High     | Performance testing meets the response-time target under simulated load.                    | Timely matching improves recovery chances.          |
