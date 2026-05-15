# Metadata Field Guide

Use YAML front matter for repeatable facts you may want to sort, filter, graph, export, or query later.

## Core Fields
- `note_type`: Groups notes for Dataview and Bases. Examples: `daily_log`, `workout_session`, `skill_progression`, `technique_session`, `weekly_log`, `observation`, `essay_draft`, `published_note`.
- `date`: Best for daily/session notes. Use `YYYY-MM-DD`.
- `status`: Workflow state. Examples: `logged`, `active`, `raw`, `draft`, `published-ready`.
- `public`: Use `true` for notes intended for publishing and `false` for client/private notes.
- `discipline`: Training area. Examples: `strength`, `calisthenics`, `taekwondo`, `boxing`, `muay_thai`, `skating`.
- `media`: Links to screenshots, photos, or videos.
- `daily_log`: Link from a session back to the daily note.
- `related_sessions`: Links from progression notes to detailed practice notes.

## Publishing Boundary
- Public notes live in `07 Fitness Site (public)`.
- Private client notes live in `08 Client CRM (private)`.
- Personal evidence lives in daily logs, workouts, observations, and dashboards.
- Client notes may link to public notes.
- Public notes should not link back to client notes.

## Daily Log Fields
- `strength_done`, `calisthenics_done`, `taekwondo_done`, `boxing_done`, `muay_thai_done`, `skating_done`: Boolean fields for easy filtering.
- `body_weight_lbs`, `sleep_hours`, `energy_1_to_5`, `soreness_1_to_5`: Numeric fields for graphing later.
- `total_training_minutes`, `total_active_minutes`, `total_volume_lbs`: Useful roll-up fields.

## Strength Fields
- `source_app`: Use `JeFIT` when the data came from screenshots or app logs.
- `total_volume_lbs`: Keep this numeric. Use `14145`, not `14,145 lbs`.
- `duration_minutes` and `active_minutes`: Keep these numeric.
- `primary_muscles`, `equipment`, `exercises`: Lists for filtering.

## Skill And Technique Fields
- `skill`: Main skill being tracked.
- `skill_category`: Larger category, such as `core`, `balance`, `kicking`, `striking`, or `locomotion`.
- `current_best` and `current_best_unit`: Use for measurable progress, such as `20` and `seconds`.
- `quality_1_to_5`, `confidence_1_to_5`, `fatigue_1_to_5`: Useful for technique sessions where quality matters more than load.

## Dataview Examples

```dataview
TABLE date, discipline, total_volume_lbs, duration_minutes, source_app
FROM "01 Workouts (raw logs)"
WHERE note_type = "workout_session"
SORT date DESC
```

```dataview
TABLE skill, discipline, current_level, current_best, current_best_unit, last_practiced
FROM "01 Workouts (raw logs)"
WHERE note_type = "skill_progression"
SORT discipline ASC, skill ASC
```

```dataview
TABLE date, body_weight_lbs, sleep_hours, energy_1_to_5, total_training_minutes
FROM "00 Daily Logs"
WHERE note_type = "daily_log"
SORT date DESC
```

## Heatmap Plugin Mappings
Use existing properties as the plugin inputs:

| Heatmap purpose | Date property | Value property |
|-----------------|---------------|----------------|
| Daily training consistency | `date` | `training_sessions_count` |
| Daily training duration | `date` | `total_training_minutes` |
| Strength volume | `date` | `total_volume_lbs` |
| Technique practice | `date` | `duration_minutes` |
| Skill progress | `last_practiced` | `current_best` |

Only add separate heatmap fields if the plugin cannot choose custom date/value properties.

## Dummy Templates
Filled examples live in [[Templates/Dummy Templates/Dummy Daily Log]]. Use the dummy copies when you want prefilled properties for testing Bases, Dataview, or plugin behavior without touching real notes.
