# Technique Session Dashboard

```dataview
TABLE
  date,
  discipline,
  skill_focus,
  session_type,
  duration_minutes,
  rounds,
  reps,
  quality_1_to_5,
  confidence_1_to_5,
  fatigue_1_to_5
FROM "01 Workouts (raw logs)"
WHERE note_type = "technique_session"
SORT date DESC
```

