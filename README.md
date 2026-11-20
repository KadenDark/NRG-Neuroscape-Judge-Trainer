# Neuroscape Judge Trainer: NRG Events edition (N1 only)

A standalone copy of the judge trainer for NRG Events, themed to match nrgevents.gg.
It only contains the N1 Store Judge exam. The N2 and N3 questions are not in this folder at all,
so they can't be read from the page source.

## Files
- `index.html` the page
- `support.js` the same runtime the main site uses (unchanged copy)
- `data/n1_quiz.json` the 24 N1 questions, pulled from quiz bank v4.2
- `cards/` only the 7 card images the N1 questions use

## Hosting
Upload the whole folder as is to any static host (GitHub Pages, Netlify, Cloudflare Pages).
It must be served over http(s); opening index.html straight from disk won't load the quiz data.

## Changing the event
Edit the `EVENT` block at the top of the script in `index.html` (name, dates, venue and link).

## Updating questions
When the main bank changes, regenerate `data/n1_quiz.json` from
`uploads/neuroscape_judge_quiz_bank.json` by keeping only tier 1 questions and the tier 1 entry.
If a new N1 question uses a card that isn't in `cards/`, copy the image in and add its name to
`CARD_FILES` in `index.html`.
