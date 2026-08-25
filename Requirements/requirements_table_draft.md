# Requirements Table

## Problem Statement #17
### Vaccination Cohort & Dose Scheduling System

| Req ID | Type | Description | Priority | Acceptance Criteria | Rationale |
|---|---|---|---|---|---|
| FR-001 | Functional | The system shall enforce the minimum required interval between vaccination doses before unlocking booking for the next dose. | High | Pass: Dose 2 booking is blocked when fewer than 28 days have elapsed since Dose 1. Pass: Dose 2 booking is available when the required interval has been satisfied. | Prevents invalid early vaccination scheduling. |
| FR-002 | Functional | The system shall allow a Citizen Registrant to register and maintain the demographic information required for vaccination scheduling. | High | Pass: When all required information is valid, the system creates a citizen profile and assigns a unique registration ID. Fail: The profile is not created when required information is missing. | Provides the information needed to identify and schedule citizens. |
| FR-003 | Functional | The system shall allow a Vaccination Officer to create and manage vaccination center appointment slots with a specified date, time and capacity. | High | Pass: A Vaccination Officer can create a slot with a center, date, time and capacity, and the slot becomes available for booking. Fail: A slot cannot be created when required slot information is missing. | Allows vaccination centers to manage appointment capacity. |
| FR-004 | Functional | The system shall allow an eligible Citizen Registrant to book an available vaccination center slot. | High | Pass: An eligible citizen can select an available slot and receives a booking confirmation. Fail: Booking is rejected when the citizen is ineligible or the slot is full. | Provides the core vaccination scheduling function. |
| FR-005 | Functional | The system shall generate a digitally verifiable QR vaccination certificate after a vaccination dose has been recorded. | High | Pass: After successful vaccination recording, the system generates a unique QR certificate that can be verified. Fail: No certificate is generated when vaccination has not been recorded. | Provides verifiable proof of vaccination. |
| NFR-001 | Nonfunctional – Performance & Security | The system shall authenticate digitally signed QR vaccination certificates through offline or online verification in under 150 ms. | High | Pass: Benchmark testing confirms that QR certificate verification completes in less than 150 ms under the specified test conditions. | Ensures fast and secure certificate verification. |
| NFR-002 | Nonfunctional – Security | The system shall protect citizen demographic and vaccination information using encrypted communication and secure data storage. | High | Pass: Security testing confirms that sensitive information is transmitted using encrypted communication and stored using encryption. | Protects sensitive citizen and vaccination information. |

