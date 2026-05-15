---
note_type: client_dashboard
status: active
public: false
client: Lisa
---

# Lisa - Client Dashboard

```button
name Lisa Profile
type link
action obsidian://open?vault=Personal%20Fitness&file=08%20Client%20CRM%20(private)%2FClients%2FLisa%2FProfile%2FLisa
color blue
```

```button
name Lisa Appointment
type link
action obsidian://open?vault=Personal%20Fitness&file=08%20Client%20CRM%20(private)%2FClients%2FLisa%2FAppointments%2F2026-05-14%20-%20Lisa%20Appointment
color blue
```

```button
name Lisa Workout
type link
action obsidian://open?vault=Personal%20Fitness&file=08%20Client%20CRM%20(private)%2FClients%2FLisa%2FWorkouts%2F2026-05-14%20-%20Lisa%20Workout
color blue
```

```button
name Lisa Payment
type link
action obsidian://open?vault=Personal%20Fitness&file=08%20Client%20CRM%20(private)%2FClients%2FLisa%2FBilling%2F2026-05-14%20-%20Lisa%20Payment
color blue
```

## Profile
- [[08 Client CRM (private)/Clients/Lisa/Profile/Lisa]]

## Appointments
```dataview
TABLE date, start_time, duration_minutes, appointment_type, attendance_status
FROM "08 Client CRM (private)/Clients/Lisa/Appointments"
WHERE client = "Lisa"
SORT date DESC
```

## Workouts
```dataview
TABLE date, session_focus, duration_minutes, attendance_status, rpe_1_to_10, pain_0_to_10
FROM "08 Client CRM (private)/Clients/Lisa/Workouts"
WHERE client = "Lisa"
SORT date DESC
```

## Progress
```dataview
TABLE date, check_in_type, goal_progress_1_to_5, energy_1_to_5, pain_0_to_10
FROM "08 Client CRM (private)/Clients/Lisa/Progress"
WHERE client = "Lisa"
SORT date DESC
```

## Billing
```dataview
TABLE date, package_type, amount_due, amount_paid, status, payment_due_date, payment_date
FROM "08 Client CRM (private)/Clients/Lisa/Billing"
WHERE client = "Lisa"
SORT date DESC
```

## Documents
- [[08 Client CRM (private)/Clients/Lisa/Documents/Waivers/Lisa - Waiver]]
- [[08 Client CRM (private)/Clients/Lisa/Documents/Injuries/Lisa - Injury Notes]]
- [[08 Client CRM (private)/Clients/Lisa/Documents/Allergies/Lisa - Allergy Notes]]
