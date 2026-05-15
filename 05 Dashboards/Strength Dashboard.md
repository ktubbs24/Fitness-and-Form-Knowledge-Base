# Strength Dashboard

```dataview
TABLE
  date,
  workout_name,
  split,
  total_volume_lbs,
  duration_minutes,
  active_minutes,
  body_weight_lbs,
  rpe_1_to_10,
  source_app
FROM "01 Workouts (raw logs)"
WHERE note_type = "workout_session"
SORT date DESC
```

