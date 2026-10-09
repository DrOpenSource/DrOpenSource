# Dr. Shubham Kashyap

**MBBS doctor turned product builder. I love taking hard problems apart and building the thing that solves them.**

I trained in medicine and became an entrepreneur first. Then AI closed the gap between knowing what a product should do and being able to build it myself — and I kept learning until I could ship. Now I take products end to end: spec, architecture, code, release.

Most of what I build is health software. The rest is whatever someone I know actually needed.

---

## What I'm building

### FieldMap — offline-first field mapping for Android
*Private, in active development*

A geologist friend needed to carry georeferenced maps into the field, hold his position with no signal, and record waypoints, lines, areas, tracks and photos — then have all of it syncs when a connection came back. So I'm building it. He validates every sprint on a real phone, in real terrain.

The hard parts, and why they were hard:

- **GDAL compiled for Android**, so map format conversion happens on the device. Importing a map cannot require a server, because there is no server where this app gets used.
- **Sync that converges without trusting the phone's clock.** Two people editing the same feature offline for a week must end up agreeing, in any order, with no coordinator.
- **Every write and its sync event commit in one transaction.** A crash mid-save can never leave a record that exists locally but will never sync, or a sync event for a record that was never written.

### GitWizard — safe Git for AI-assisted development
[Repository](https://github.com/DrOpenSource/GitWizard) · VS Code, Cursor, Antigravity · TypeScript · Vitest · MIT

I was teaching a student to build with AI and he kept destroying his own work. Not through carelessness — because when you ask a model to change thirty files at once, Git stops being a safety net and becomes a hazard.

GitWizard takes a shadow checkpoint before every transaction, aborts and restores the workspace on conflict, translates reflog into plain English with one-click undo, and splits a sprawling AI change set into clean, PR-ready branches.

### Health software
*Several applications in private development*

Clinical and patient-facing tools: pathology assistance, cardiovascular risk, maternal health, nutrition tracking. These stay private while they are in development — medicine is not a domain to ship half-finished.

---

## Stack

TypeScript · React Native / Expo · Next.js · Supabase / PostgreSQL · SQLite · MapLibre · GDAL · Vitest · Deno

---

## Elsewhere

**[LinkedIn](https://www.linkedin.com/in/imkashyaps)**

Open to collaboration on health, offline-first and geospatial software.

