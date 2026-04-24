# Marketing Measurement Academy

A self-contained browser-based study tool for mastering marketing measurement concepts — built to make you conversant with executives and credible with analysts.

**[▶ Open the tool](https://chawk1634.github.io/marketing-measurement-academy/)** — no install, just open in any browser.

---

## What's inside

### 🃏 Flashcards (51 cards across 8 categories)
Drill definitions and formulas. Rate yourself after each flip — cards graduate to "Mastered" after 3 consecutive correct answers and leave the active deck.

| Category | Cards |
|----------|-------|
| MMM (Marketing Mix Modeling) | 11 |
| MTA (Multi-Touch Attribution) | 6 |
| Incrementality Testing | 7 |
| CAC / LTV | 6 |
| Churn | 4 |
| Brand Health | 5 |
| TV Measurement | 7 |
| MER / ROAS | 5 |

### 🧩 Case Studies (12 scenarios)
Real-world multiple-choice scenarios — choose the right model, diagnose the problem, or defend the decision. Full explanation revealed after each answer.

Topics include: attribution conflicts, TV measurement design, CAC/LTV math, churn spike diagnosis, retargeting ROAS traps, geo holdout test design, payback vs. LTV trade-offs, brand health vs. ROAS, lower-funnel budget spirals, and more.

### Gamification
- 🔥 Streak counter
- ⭐ Mastered card tracking (3 consecutive correct = mastered)
- ✓ All-time score
- Progress bars per category
- All progress persists via `localStorage` across sessions

---

## How to use

**Option 1 — Live link:** [chawk1634.github.io/marketing-measurement-academy](https://chawk1634.github.io/marketing-measurement-academy/)

**Option 2 — Run locally:** Clone the repo and open `index.html` in any browser. No server, no dependencies, no build step.

```bash
git clone https://github.com/chawk1634/marketing-measurement-academy.git
cd marketing-measurement-academy
open index.html   # macOS
```

---

## How to contribute or fork

The entire app is a single `index.html` file. All content lives in two JavaScript arrays near the top of the `<script>` block:

```js
const CARDS = [ ... ]   // flashcard data
const CASES = [ ... ]   // case study data
```

**To add a flashcard:**
```js
{
  id: 'unique_id',
  cat: 'Category Name',   // must match an existing category or creates a new one
  q: 'Question on the front of the card',
  a: 'Answer text on the back',
  f: 'Optional formula (shown in green monospace block, supports \n newlines)'
}
```

**To add a case study:**
```js
{
  id: 'unique_id',
  title: 'Short title',
  cat: 'Category tag',
  scenario: 'The scenario description shown to the user.',
  opts: ['Option A text', 'Option B text', 'Option C text', 'Option D text'],
  correct: 1,   // 0-indexed: 0=A, 1=B, 2=C, 3=D
  explain: 'Explanation shown after answering.'
}
```

Pull requests welcome — especially new case studies, additional categories (e.g., attribution modeling, media planning, incrementality test design), or corrections to existing content.

---

## Topics covered

Marketing Mix Modeling (MMM) · Multi-Touch Attribution (MTA) · Incrementality Testing · Geo Lift Tests · CAC · LTV · Payback Period · Churn Rate · Gross vs Net Revenue Churn · Brand Awareness · Brand Consideration · Share of Voice · GRPs · Reach & Frequency · CTV vs Linear TV · iSpot / EDO · ROAS · MER · iROAS · Budget Death Spiral · Attribution Windows · Statistical Power · Saturation Curves · Adstock · Bayesian MMM · DAGs · Multicollinearity · Budget Optimization

---

## Content sources & inspiration

- [Recast Blog](https://getrecast.com/blog/) — Bayesian MMM methodology, incrementality testing, TV measurement
- Binet & Field — *The Long and the Short of It* (eSOV, long-term brand effects)
- Erwin Ephron — Recency planning theory
- Industry-standard benchmarks for CAC, LTV, payback periods, and churn

---

*Built as a personal study tool. All content is educational — verify benchmarks and formulas against primary sources before applying to your own organization.*
