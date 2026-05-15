# Skill Progression Dashboard

```dataview
TABLE
  discipline,
  skill,
  skill_category,
  current_level,
  goal_level,
  current_best,
  current_best_unit,
  last_practiced,
  next_progression
FROM "01 Workouts (raw logs)"
WHERE note_type = "skill_progression"
SORT discipline ASC, skill ASC
```

