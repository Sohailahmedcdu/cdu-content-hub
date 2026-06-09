# CDU Content Hub

Educational content library for **Car Dealership University**, built from the
CDU Digital Dealer Program class recordings.

**Live site:** https://sohailahmedcdu.github.io/cdu-content-hub/

## Two views

- **`index.html` — Browse by Topic** (primary). 12 topics distilled from 10 class
  recordings. Each topic links to the source classes (on Fathom) and has slots for a
  NotebookLM podcast + study guide. This is where topic-level content lives, because
  the program teaches the same topics (Dubai market, salvage, auctions, HST…) across
  many classes — so they're organized once, by subject, not repeated per class.
- **`classes.html` — Browse by Class** (secondary). The original per-class view, with
  the genuine Dec 1 (quiz, flashcards, infographic, lead magnet) and Dec 9 (quiz)
  assets. Everything else is marked Coming Soon.

```
index.html        # Topic hub (primary)
classes.html      # Class hub (secondary)
dec-1/            # Dec 1, 2025 — Onboarding (4 genuine assets)
  quiz.html  flashcards.html  infographic.html  lead-magnet.html
dec-9/            # Dec 9, 2025 — Live Class
  quiz.html       # genuine
```

## Adding content

### Add a NotebookLM podcast or study guide to a topic
In `index.html`, find the topic in the `topics` array. Each topic has an `assets`
list. To make a slot live, replace:

```js
{ name: 'NotebookLM Podcast', icon: '🎧', status: 'coming' }
```
with a real link (a NotebookLM share URL, or a local file you've added):
```js
{ name: 'NotebookLM Podcast', icon: '🎧', url: 'https://notebooklm.google.com/notebook/…' }
```
The slot flips from a dashed "ADD LINK" placeholder to a live "LIVE" link, and the
"Podcasts Linked" counter updates automatically.

### Add a per-class study asset
1. Drop the HTML file into a dated folder (e.g. `dec-16/quiz.html`).
2. In `classes.html`, find the class in the `classes` array and replace that asset's
   `status: 'coming'` with `url: 'dec-16/quiz.html'`.

### Deploy
Commit and push to `main` — GitHub Pages redeploys automatically.

## Note on content quality
Auto-generated per-class assets were found to be near-duplicate clones (same questions
restamped under different class names), so they were **not** published. Genuine,
topic-specific content (e.g. NotebookLM outputs) should be added via the slots above.
