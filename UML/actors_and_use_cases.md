# Actors and Use Cases

## Problem Statement #17
### Vaccination Cohort & Dose Scheduling System

## Actors

### ACT-01 – Citizen Registrant
The Citizen Registrant registers demographic information, checks vaccination eligibility, books vaccination slots, and verifies vaccination certificates.

### ACT-02 – Vaccination Officer
The Vaccination Officer manages vaccination-center slots, records administered doses, and supports certificate generation and verification.

### ACT-03 – Public Health Administrator
The Public Health Administrator manages vaccination scheduling operations and oversees vaccination-center slot information and certificate verification.

## Use Cases

| Use Case ID | Use Case | Primary Actor | Purpose |
|---|---|---|---|
| UC-01 | Register Citizen | Citizen Registrant | Register and maintain citizen demographic information required for vaccination scheduling. |
| UC-02 | Check Dose Eligibility | Citizen Registrant | Check whether the citizen has satisfied the required interval before booking a dose. |
| UC-03 | Book Vaccination Slot | Citizen Registrant | Book an available vaccination-center slot when the citizen is eligible. |
| UC-04 | Manage Vaccination Slots | Vaccination Officer | Create and manage vaccination-center appointment slots and their capacity. |
| UC-05 | Record Vaccination Dose | Vaccination Officer | Record that a vaccination dose has been administered to a citizen. |
| UC-06 | Generate QR Certificate | Vaccination Officer | Generate a digitally verifiable QR vaccination certificate after a dose is recorded. |
| UC-07 | Verify QR Certificate | Citizen Registrant / Vaccination Officer / Public Health Administrator | Verify the authenticity of a vaccination certificate. |

## Use-Case Relationships

### Include

**UC-03 Book Vaccination Slot** `«include»` **UC-02 Check Dose Eligibility**

Dose eligibility checking is included in the vaccination booking process.

### Extend

**UC-06 Generate QR Certificate** `«extend»` **UC-05 Record Vaccination Dose**

QR certificate generation is additional behavior associated with successful recording of a vaccination dose.
