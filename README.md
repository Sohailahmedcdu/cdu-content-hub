# CDU Content Hub

Educational content library for **Car Dealership University** — quizzes, flashcards,
infographics, and lead magnets generated from CDU Digital Dealer Program class recordings.

**Live site:** https://sohailahmedcdu.github.io/cdu-content-hub/

## Structure

```
index.html              # Hub landing page (searchable, filterable)
dec-1/                   # Dec 1, 2025 — Export & Digital Dealership Onboarding
  quiz.html
  flashcards.html
  infographic.html
  lead-magnet.html
dec-9/                   # Dec 9, 2025 — Export Cars Program Live Class
  quiz.html
```

## Status

5 live study assets across 2 classes. Remaining classes are marked **Coming Soon**
on the hub and will be wired in as their assets are produced.

## Adding new content

1. Drop the asset HTML files into a dated folder (e.g. `dec-16/quiz.html`).
2. In `index.html`, find the matching class in the `classes` array and replace
   `status: 'coming'` with `url: 'dec-16/quiz.html'` for that asset.
3. Commit and push — GitHub Pages redeploys automatically.
