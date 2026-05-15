# START HERE - Vault Operating Manual

This vault is a movement documentation system, personal training record, public fitness site draft, and private client CRM.

Use this file as the beginner walkthrough. If the vault is copied as a template for someone else, this is the document they should read first.

```button
name Fitness Home
type link
action obsidian://open?vault=Personal%20Fitness&file=Fitness%20Home
color blue
```

```button
name Visual Canvas
type link
action obsidian://open?vault=Personal%20Fitness&file=Movement%20Archive%20Home.canvas
color blue
```

```button
name Portland Startup Guide
type link
action obsidian://open?vault=Personal%20Fitness&file=PORTLAND%20FITNESS%20STEWARD%20STARTUP%20GUIDE
color blue
```

```button
name Client CRM
type link
action obsidian://open?vault=Personal%20Fitness&file=08%20Client%20CRM%20(private)%2FClient%20CRM%20Hub
color blue
```

## Core Identity

The vault is organized around this idea:

> Movement Under Discipline and Training Archive

The purpose is not only to log workouts. The purpose is to steward fitness documentation: what was practiced, what was learned, what was observed, what became useful, and what can eventually become public teaching material.

## The Three Main Domains

### 1. Public Knowledge

Folder:

```text
07 Fitness Site (public)/
```

This is the publishable documentation site. It contains movement notes, anatomy notes, discipline notes, common problems, goals, programming notes, resources, essays, question notes, vocabulary, physiology, psychology, environment, skill acquisition, and decision-making notes.

Start here:

- [[07 Fitness Site (public)/00 Start Here/Movement Under Discipline and Training Archive]]
- [[07 Fitness Site (public)/02 Movement Library/Movement Library Index]]
- [[07 Fitness Site (public)/02 Movement Library/Anatomy/Anatomy Index]]
- [[07 Fitness Site (public)/02 Movement Library/Disciplines/Disciplines Index]]

Rule:

Public notes can be published. Do not put private client names, private medical information, payment information, or personal-sensitive details here.

### 2. Personal Evidence

Folders:

```text
00 Daily Logs/
01 Workouts (raw logs)/
02 Observations (raw thinking)/
03 Essays (refined writing)/
04 Published (ready for public)/
05 Dashboards/
06 Bases/
Assets/
```

This is where personal training, personal observations, screenshots, progress notes, and dashboards live.

Use it to answer:

- What did I do?
- What am I noticing?
- What is changing over time?
- What personal evidence supports a future essay or public note?

Public notes may link to general personal essays or observations if you choose, but raw daily logs should stay private by default.

### 3. Private Client CRM

Folder:

```text
08 Client CRM (private)/
```

This is for coaching clients, appointments, progress, workouts, waivers, billing, injuries, allergies, documents, and resources shared.

Start here:

- [[08 Client CRM (private)/Client CRM Hub]]
- [[08 Client CRM (private)/Clients/Clients Index]]
- [[08 Client CRM (private)/Clients/Lisa/Lisa - Client Dashboard]]

Rule:

Client notes may link to public knowledge notes. Public knowledge notes should not link back to client notes.

## How To Use The Vault Daily

### Fast Daily Use

1. Open today’s daily note in `00 Daily Logs/YYYY/MM Month/`.
2. Fill only the fields that matter:
   - `date`
   - training booleans like `strength_done`
   - `training_sessions_count`
   - `total_training_minutes`
   - `total_volume_lbs`, if lifting happened
3. Add quick observations in the body.
4. Link detailed workout notes only when detail is useful.

Do not force yourself to fill every property every day. Blank properties are acceptable.

### Workout Use

Use `01 Workouts (raw logs)` for personal workouts and progression tracking.

Use:

- [[Templates/Workout Template]]
- [[Templates/Technique Practice Template]]
- [[Templates/Skill Progression Template]]

The workout app or JeFIT can hold detailed exercise logging. Obsidian should capture the higher-value layer:

- what mattered
- what changed
- what pattern repeated
- what should be remembered
- what could become public teaching later

### Knowledge Base Use

When learning from a video, PDF, coaching session, or personal practice:

1. Decide what type of note it is.
2. Put it in the correct public site section.
3. Link it to anatomy, discipline, problems, goals, or principles.
4. Keep it atomic.

Good note:

```text
Scapular Stability
```

Weak note:

```text
Everything About Upper Body Training
```

## The Three Kinds Of Knowledge Notes

### Information Notes

These answer:

> What is generally known?

Examples:

- [[07 Fitness Site (public)/02 Movement Library/Disciplines/Weight Lifting/Hip Hinge]]
- [[07 Fitness Site (public)/02 Movement Library/Anatomy/Ankles/Dorsiflexion]]

Use for mechanics, anatomy, benefits, regressions, progressions, resources, and coaching cues.

### Observation Notes

These answer:

> What did I personally notice?

Examples:

- [[_Observations Hub]]
- [[Upper Body Structure]]

Use for lived experience, personal training patterns, client-session observations, and repeated practical findings.

### Conclusion Notes

These answer:

> What judgment am I forming from the evidence?

Examples:

- [[03 Essays (refined writing)/Essays Hub]]
- [[07 Fitness Site (public)/16 Decision Making/Decision Making Index]]

Use for essays, frameworks, public claims, coaching principles, and decision-making notes.

## Client CRM Workflow

Each client gets their own folder:

```text
08 Client CRM (private)/Clients/Client Name/
  Client Name - Client Dashboard.md
  Profile/
  Appointments/
  Workouts/
  Progress/
  Assessments/
  Programs/
  Documents/
    Waivers/
    Injuries/
    Allergies/
  Billing/
  Notes/
  Resources Shared/
```

For a new client:

1. Copy the Lisa folder structure.
2. Rename the folder and notes.
3. Fill the client profile.
4. Add appointments as they are scheduled.
5. Add workouts only when you actually train them.
6. Add progress check-ins on a reasonable interval.
7. Put signed documents and waivers under that client’s `Documents` folder.
8. Track payments in `Billing`.

Templates:

- [[Templates/Client Profile Template]]
- [[Templates/Client Appointment Template]]
- [[Templates/Client Workout Template]]
- [[Templates/Client Progress Check-In Template]]
- [[Templates/Client Payment Template]]
- [[Templates/Client Document Template]]
- [[Templates/Client Injury Template]]
- [[Templates/Client Allergy Template]]

## Publishing Boundary

Publish:

- public movement notes
- anatomy notes
- resources
- general essays
- general coaching frameworks
- selected progress reflections

Do not publish:

- client names
- client health information
- payment notes
- private appointments
- raw personal daily logs
- anything that identifies another person without consent

## CSS And Visual Setup

Enabled snippets:

- `.obsidian/snippets/bear-inspired.css`
- `.obsidian/snippets/image-gallery.css`

Visual home:

- [[Movement Archive Home.canvas]]

The Bear-inspired snippet uses requested font names:

- `Bear Sans UI`
- `Bear Sans UI Heading`
- `Roboto Mono`

Those fonts must be installed on your Mac to render exactly. Otherwise Obsidian will use fallback fonts.

The image gallery snippet makes embedded images cleaner and more gallery-like in reading mode.

Folder Notes:

- The Folder Notes plugin is configured to use a same-name note inside each folder.
- Clicking a folder should open the matching folder note.
- Example: clicking `Templates/` opens `Templates/Templates.md`.
- Folder notes include a Dataview contents list.

Buttons:

- Buttons are only added to private/navigation notes.
- Buttons are intentionally not added to public-site notes because publish output may not render plugin syntax correctly.

## Templates

General:

- [[Templates/Daily Log Template]]
- [[Templates/Workout Template]]
- [[Templates/Technique Practice Template]]
- [[Templates/Skill Progression Template]]
- [[Templates/Weekly Log Template]]
- [[Templates/Observation Template]]
- [[Templates/Essay Draft Template]]
- [[Templates/Published Note Template]]

Public site:

- [[Templates/Public Movement Note Template]]
- [[Templates/Public Anatomy Note Template]]
- [[Templates/Public Resource Note Template]]

Client CRM:

- [[Templates/Client Profile Template]]
- [[Templates/Client Appointment Template]]
- [[Templates/Client Workout Template]]
- [[Templates/Client Progress Check-In Template]]
- [[Templates/Client Payment Template]]
- [[Templates/Client Document Template]]
- [[Templates/Client Injury Template]]
- [[Templates/Client Allergy Template]]

Reference:

- [[Templates/_Metadata Field Guide]]

Dummy examples:

- [[Templates/Dummy Templates/Dummy Daily Log]]

## Heatmap Strategy

Do not duplicate heatmap fields.

Use existing properties:

| Heatmap purpose | Date property | Value property |
|-----------------|---------------|----------------|
| Daily consistency | `date` | `training_sessions_count` |
| Daily duration | `date` | `total_training_minutes` |
| Strength volume | `date` | `total_volume_lbs` |
| Technique practice | `date` | `duration_minutes` |
| Skill progress | `last_practiced` | `current_best` |
| Weekly consistency | `week_start` | `sessions_count` |

## If This Vault Becomes A Template

Before sharing:

1. Delete private client folders.
2. Delete personal daily logs.
3. Delete private observations.
4. Delete progress photos and personal screenshots.
5. Keep templates, public site structure, CSS snippets, dashboards, and this operating manual.
6. Keep dummy templates if you want people to see examples.

## Maintenance Rule

If the vault structure changes at the macro level, update this file.
