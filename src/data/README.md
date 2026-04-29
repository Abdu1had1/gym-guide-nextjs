# data

Static JSON data files that serve as the content layer for the Gym Guide application, providing sample schemas for exercises, gym equipment, and workout routines.

## Files

| File | Description |
|------|-------------|
| `exercises.json` | Array of exercise entries with fields: name, slug, muscles, difficulty, equipment, instructions, and tips |
| `gear.json` | Array of gym equipment entries with fields: name, slug, category, description, typicalWeight, usedFor, beginner_friendly, and image |
| `routines.json` | Array of workout routine entries with fields: name, slug, description, difficulty, daysPerWeek, durationWeeks, goal, and days (each day listing exercises with sets, reps, and rest) |
