# Gym Guide — Next.js

A fitness guide web application built with Next.js 14 (App Router), TypeScript, and Tailwind CSS. Provides exercise references, gear recommendations, and curated workout routines.

## Project Tracking

**Linear Project:** Gym Guide — Next.js

## Getting Started

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the app.

## Tech Stack

- **Framework:** Next.js 14 with App Router
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Data:** Static JSON files

## Folder Structure

```
test-adw/
├── src/
│   ├── app/                    # Next.js App Router pages and layouts
│   │   ├── layout.tsx          # Root layout with global font and metadata
│   │   ├── page.tsx            # Home page
│   │   └── globals.css         # Global styles and Tailwind directives
│   └── data/                   # Static JSON data schemas
│       ├── exercises.json      # Exercise entries (name, slug, muscles, difficulty, equipment, instructions, tips)
│       ├── gear.json           # Gym gear entries (name, slug, category, description, usedFor)
│       └── routines.json       # Workout routines (name, slug, days, exercises per day)
├── public/                     # Static assets (SVGs, images)
├── next.config.ts              # Next.js configuration
├── tailwind.config.ts          # Tailwind CSS configuration (auto-generated)
├── postcss.config.mjs          # PostCSS configuration for Tailwind
├── tsconfig.json               # TypeScript compiler configuration
├── eslint.config.mjs           # ESLint configuration
└── package.json                # Dependencies and npm scripts
```

## Data Schemas

### Exercise (`src/data/exercises.json`)

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Display name of the exercise |
| `slug` | string | URL-friendly identifier |
| `muscles` | string[] | Primary muscles targeted |
| `difficulty` | string | `beginner`, `intermediate`, or `advanced` |
| `equipment` | string[] | Required equipment (empty array = bodyweight) |
| `instructions` | string[] | Step-by-step instructions |
| `tips` | string[] | Form cues and coaching tips |

### Gear (`src/data/gear.json`)

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Display name of the equipment |
| `slug` | string | URL-friendly identifier |
| `category` | string | `free-weights`, `machines`, `accessories`, or `bodyweight` |
| `description` | string | What the equipment is and how it's used |
| `typicalWeight` | string \| null | Common weight range, null if not applicable |
| `usedFor` | string[] | Common exercises performed with this gear |
| `beginner_friendly` | boolean | Whether suitable for beginners |
| `image` | string | Path to equipment image |

### Routine (`src/data/routines.json`)

| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Display name of the routine |
| `slug` | string | URL-friendly identifier |
| `description` | string | Summary of the program |
| `difficulty` | string | `beginner`, `intermediate`, or `advanced` |
| `daysPerWeek` | number | Training frequency |
| `durationWeeks` | number | Recommended program length |
| `goal` | string | Primary training objective |
| `days` | object[] | Array of training days with exercises, sets, reps, and rest |

## Available Scripts

```bash
npm run dev       # Start development server
npm run build     # Build for production
npm run start     # Start production server
npm run lint      # Run ESLint
```
