---
note_type: clients_index
status: active
public: false
---

# Clients Index

Create one note per client using [[Templates/Client Profile Template]].

## Clients
- [[08 Client CRM (private)/Clients/Lisa/Lisa - Client Dashboard]]

## Client Profiles
```dataview
TABLE client, status, first_met, how_we_met, where_we_met, training_frequency_goal, payment_status
FROM "08 Client CRM (private)/Clients"
WHERE note_type = "client_profile"
SORT client ASC
```

## Recent Appointments
```dataview
TABLE client, date, start_time, appointment_type, attendance_status
FROM "08 Client CRM (private)/Clients"
WHERE note_type = "client_appointment"
SORT date DESC
```
