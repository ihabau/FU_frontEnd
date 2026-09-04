# W36-07 — Grid, Nav, Media Queries & Exam 1

> 🔵 **In progress** — Folkuniversitetet MU26, Vecka 36 (Fri 4/9)

## Topic
CSS Grid for departure board, nav with anchor links, footer, media queries + Examination 1 "Eventsidan" brief.

Course material: https://github.com/linuszocom/mu26-frontend-grundkurs/tree/main/vecka-36/07-nav-mq-exam1
Teaching guide: https://regal-choux-578278.netlify.app/v36-t3-linje/

---

## 🟢 Track A — Attended lesson (Fri 13:00–16:00)
- [ ] `03-ovningar.md` — exercises
- [ ] `05-sjalvtest.md` — self-test
- Use `01-teoriguide.md` as reference when stuck

## 🟡 Track B — Missed lesson
- [ ] `01-teoriguide.md` → `02-visuell.md` → `03-ovningar.md` → `04-ai-traning.md` → `05-sjalvtest.md`

---

## Checklist — Cykel 1–5 (Bas)

### Setup (Cykel 1)
- [ ] Created `v36-linje-camp` repo on GitHub
- [ ] Created `index.html` + `style.css`
- [ ] Linked CSS in `<head>`
- [ ] First commit pushed

### Linjeinfo — semantisk HTML (Cykel 2)
- [ ] Created `<header class="linjeinfo" id="linjeinfo">`
- [ ] Added `h1` "Linje 47"
- [ ] Added `img` with descriptive `alt`, `width`, `height`
- [ ] Added `p.stracka`, `p.frekvens`, `p.tagline`
- [ ] Opened `<main></main>` under header

### Avgångar utan Grid (Cykel 3)
- [ ] Created `<section id="tabla">` with `h2`
- [ ] Created `.tabla` div inside section
- [ ] Added 6–8 `<article class="avgang">` with `p.tid` + `p.dest`
- [ ] No Grid CSS yet — cards stack vertically (this is the point)

### Rutnätet — CSS Grid (Cykel 4)
- [ ] `.tabla` has `display: grid`
- [ ] `.tabla` has `grid-template-columns: 1fr 1fr 1fr`
- [ ] `.tabla` has `gap: 1rem`
- [ ] Departures fill cells left→right, row by row
- [ ] **Test:** Added 7th departure — still works without manual recalculation

### Nav, destinationer, footer (Cykel 5)
- [ ] `<nav>` with links `#linjeinfo`, `#tabla`, `#destinationer`
- [ ] `<section id="destinationer">` with `.kort-rad` Flex + 3+ cards
- [ ] `.kort-rad`: `display: flex`, `gap: 1rem`, `flex-wrap: wrap`
- [ ] `.kort`: `flex: 1 1 200px`, padding, border
- [ ] `<footer>` with contact + 2+ fictional sponsors
- [ ] `@media (max-width: 600px)` → `.tabla { grid-template-columns: 1fr }`
- [ ] All nav links scroll to correct sections

### README
- [ ] Created `README.md` with Flex vs Grid explanation (three-step method)
- [ ] Added ownership statement: "I can explain every line I pushed"

---

## Checklist — Cykel 6–7 (Fördjupning)

### DevTools viewport test (Cykel 6)
- [ ] Opened DevTools → Inspect `.tabla`
- [ ] Toggled device toolbar to 375px width
- [ ] Verified `grid-template-columns` = `1fr` (one column)
- [ ] Confirmed `@media` rule is active in Styles panel
- [ ] Tested nav — may need `flex-wrap: wrap` in MQ

### Variation & nav-flex (Cykel 7)
- [ ] Tested `1fr 1fr` (2 columns) vs `1fr 1fr 1fr` (3 columns)
- [ ] Styled `nav` with `display: flex`, `justify-content`, `gap`
- [ ] All nav links tested — page scrolls to correct section
- [ ] Wrote explanation in README for column choice

---

## Checklist — Cykel 8 (Exam 1 transfer)

### Planning (NOT building exam page here)
- [ ] Read `examination_1_eventsidan.md` from course material
- [ ] Chose group's event theme (NOT Linje 47)
- [ ] Created group repo on GitHub (or documented who creates it)
- [ ] Added all group members to repo
- [ ] Wrote README-outline with headers for all 3 theory questions
- [ ] Distributed sections: who owns welcome, schedule, highlights, nav/footer
- [ ] Made planning commits with clear messages (include names)

### Mapping table — Linje camp → Exam 1
| Linje camp | Exam 1 equivalent |
|---|---|
| `header.linjeinfo` / `#linjeinfo` | Welcome block (name, image, date, location) |
| `section#tabla` + `.tabla` Grid | `#schedule` — program with Grid |
| `section#destinationer` + `.kort-rad` Flex | `#highlights` — activity cards with Flex |
| `nav` + `#` anchors | Same technique, exam IDs |
| `footer` contact + sponsors | Same structure, event content |
| `@media` on tabla | MQ on schedule/nav in exam |
| README outline | Answer all 3 theory questions with own code |

### Stop rule
- You should NOT leave cykel 8 with a finished exam page — only plan + first commits

---

## Study questions
1. Why does `display: grid` sit on `.tabla` (parent) and not on each `.avgang` (child)?
2. What does `1fr` do compared to `width: 33%` on each cell?
3. What happens if `href="#tabla"` is correct but `section` is missing `id="tabla"`?
4. Why does tabla need a media query but destination cards often work with just `flex-wrap`?
5. What is the difference between Flexbox and Grid — when to use which?
6. How do you prove a media query is active in DevTools?

## Key concepts
| Concept | Definition |
|---|---|
| **CSS Grid** | Two-dimensional layout — rows AND columns simultaneously |
| **`display: grid`** | Turns element into grid container (set on PARENT) |
| **`grid-template-columns`** | Defines column track sizes |
| **`fr` unit** | Fraction of available space — fair shares |
| **`gap`** | Space between grid cells or flex items |
| **`<nav>`** | Semantic element for navigation links |
| **Anchor links** | `href="#id"` scrolls to element with matching `id` |
| **Media query** | `@media (max-width: 600px)` applies styles at breakpoints |
| **Flex vs Grid** | Flex = 1D (band), Grid = 2D (board) |
