# Use-Case Flow

## UC-03 – Book Vaccination Slot

### Primary Actor
Citizen Registrant

### Goal
Book an available vaccination appointment after confirming that the citizen is eligible for the required vaccination dose.

### Preconditions
1. The Citizen Registrant has a valid registered profile.
2. The vaccination center has available appointment slots.
3. The citizen's vaccination history is available to the system.
4. The system can determine whether the required dose interval has been satisfied.

### Postconditions
1. A valid vaccination appointment is recorded for the citizen.
2. The selected vaccination-center slot is marked as booked.
3. The citizen receives a booking confirmation.

### Main Success Scenario

1. The Citizen Registrant selects the option to book a vaccination slot.
2. The system identifies the citizen and retrieves the vaccination history.
3. The system checks the citizen's eligibility for the required dose.
4. The system confirms that the minimum required dose interval has been satisfied.
5. The system displays available vaccination-center slots.
6. The Citizen Registrant selects a preferred available slot.
7. The system validates that the selected slot is still available.
8. The system records the vaccination appointment.
9. The system marks the selected slot as booked.
10. The system displays a booking confirmation to the Citizen Registrant.

### Alternate Flow

**A1 – Required dose interval has not been satisfied**

1. At Step 4, the system determines that the minimum required interval has not been satisfied.
2. The system prevents the Citizen Registrant from booking the next dose.
3. The system informs the Citizen Registrant that the dose is not yet eligible for booking.
4. The use case ends without creating an appointment.
