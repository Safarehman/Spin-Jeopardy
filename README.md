# Spin Jeopardy

A Jeopardy-style quiz game where a spinning wheel picks the section, question and points.
Single static page (no build step), ready for GitHub + Netlify.

## Files
- `index.html` – the whole app (HTML, CSS, JS)
- `netlify.toml` – tells Netlify to publish the repo root

## Deploy
1. Create a new GitHub repo (e.g. `spin-jeopardy`) and upload these files to the root.
2. In Netlify: **Add new site → Import an existing project → GitHub** → pick the repo.
3. Leave build command empty, publish directory `.` → **Deploy**.
Every push to `main` redeploys automatically.

## How it works
- **Setup tab** (game host): title, rules, sections, questions (difficulty + points), players/teams, options.
- **Play tab**: spin (button or Space bar), question pops up with timer, host awards/deducts points.
- Answered questions are greyed out (wheel never lands on them) or removed – host's choice.
- Wheel can be one slice per question, or one slice per section.
- Data autosaves in the browser (localStorage). Use **Export game file** to move a game between devices.

## Bulk import format
One line per question:
```
Section, Question, Answer, Difficulty, Points
Science, "Which planet is known as the Red Planet?", Mars, Easy, 100
```
