# Heatmap Dashboard

Use existing properties for heatmaps. Do not duplicate fields unless a specific plugin requires a fixed property name.

## Recommended Property Mappings

| Heatmap purpose            | Notes folder                            | Date property    | Value property            |
| -------------------------- | --------------------------------------- | ---------------- | ------------------------- |
| Daily training consistency | `00 Daily Logs`                         | `date`           | `training_sessions_count` |
| Daily training duration    | `00 Daily Logs`                         | `date`           | `total_training_minutes`  |
| Strength volume            | `01 Workouts (raw logs)`                | `date`           | `total_volume_lbs`        |
| Technique practice         | `01 Workouts (raw logs)`                | `date`           | `duration_minutes`        |
| Skill progress             | `01 Workouts (raw logs)`                | `last_practiced` | `current_best`            |
| Weekly consistency         | `01 Workouts (raw logs)/Weekly Reviews` | `week_start`     | `sessions_count`          |

## Daily Training Minutes

```dataview
TABLE date, total_training_minutes, training_sessions_count
FROM "00 Daily Logs"
WHERE note_type = "daily_log" AND total_training_minutes
SORT date DESC
```

## Strength Volume

```dataview
TABLE date, total_volume_lbs, workout_name, split
FROM "01 Workouts (raw logs)"
WHERE note_type = "workout_session" AND total_volume_lbs
SORT date DESC
```

## Technique Minutes

```dataview
TABLE date, discipline, skill_focus, duration_minutes
FROM "01 Workouts (raw logs)"
WHERE note_type = "technique_session" AND duration_minutes
SORT date DESC
```

## Skill Bests

```dataview
TABLE last_practiced, discipline, skill, current_best, current_best_unit
FROM "01 Workouts (raw logs)"
WHERE note_type = "skill_progression" AND current_best
SORT last_practiced DESC
```

## Minimal Daily Workflow

For daily use, fill only:
- `date`
- done booleans, such as `strength_done`
- `training_sessions_count`
- `total_training_minutes`
- `total_volume_lbs`, only if lifting happened

Everything else can stay blank until it is useful.

