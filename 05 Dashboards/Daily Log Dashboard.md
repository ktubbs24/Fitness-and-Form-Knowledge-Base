# Daily Log Dashboard

```dataview
TABLE
  date,
  body_weight_lbs,
  sleep_hours,
  energy_1_to_5,
  soreness_1_to_5,
  total_training_minutes,
  strength_done,
  calisthenics_done,
  taekwondo_done,
  boxing_done,
  muay_thai_done,
  skating_done
FROM "00 Daily Logs"
WHERE note_type = "daily_log"
SORT date DESC
```

