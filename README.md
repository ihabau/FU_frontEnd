# W36-05 — Flexbox

> 🔵 **In progress** — Folkuniversitetet MU26, Vecka 36 (Wed 2/9 + Thu 3/9)

## Topic
Flexbox layout — cards in a row, gap, wrap, justify-content, align-items.

Course material: https://github.com/linuszocom/mu26-frontend-grundkurs/tree/main/vecka-36/05-flexbox
Teaching guide: https://regal-choux-578278.netlify.app/v36-t2-flexbox/

---

## 🟢 Track A — Attended lesson (Wed 13:00–16:00)
- [ ] `03-ovningar.md` — exercises
- [ ] `05-sjalvtest.md` — self-test
- Use `01-teoriguide.md` as reference when stuck

## 🟡 Track B — Missed lesson
- [ ] `01-teoriguide.md` → `02-visuell.md` → `03-ovningar.md` → `04-ai-traning.md` → `05-sjalvtest.md`

---

## Checklist — Cykel 1–5 (Bas)

### Setup (Cykel 1)
- [ ] Created `v36-flex-camp` repo on GitHub
- [ ] Created `index.html` + `style.css`
- [ ] Linked CSS in `<head>`

### Aktivitetskort — semantisk HTML (Cykel 2)
- [ ] Created `<section class="highlights">` with `h2`
- [ ] Created `.kort-rad` div inside section
- [ ] Added 3× `<article class="kort">` with `img` (alt, width, height), `h3`, `p`
- [ ] Cards stack vertically (block elements) — this is correct at this stage

### Lådan — Box Model (Cykel 3)
- [ ] `.kort` has `padding: 1rem`, `background-color: #f8fafc`, `border: 1px solid #e2e8f0`
- [ ] `.kort` has `color: #0f172a`, `font-family: sans-serif`
- [ ] `.kort img` has `max-width: 100%`, `height: auto`
- [ ] Cards styled but still stacked

### Block-fällan (Cykel 4)
- [ ] Understood WHY cards stack (block elements take 100% width)
- [ ] Tested `width: 30%` + `margin-right: 3%` hack — saw it breaks with 4 cards
- [ ] Recognized this is the problem Flexbox solves

### Flexbox (Cykel 5)
- [ ] Removed manual `width` and `margin-right` from `.kort`
- [ ] `.kort-rad` has `display: flex`, `gap: 1rem`, `flex-wrap: wrap`
- [ ] `.kort` has `flex: 1 1 200px`
- [ ] **Test:** Added 4th card — it fits automatically
- [ ] **Test:** Resized window — cards wrap to new row

### README + Feedback
- [ ] Created `README.md` explaining why Flexbox fits activity cards
- [ ] Wrote 3 FEEDBACK lines on peer code example
- [ ] Used concrete code references, not vague praise

---

## Checklist — Cykel 6–7 (Fördjupning)

### Rattarna (Cykel 6)
- [ ] `.kort-rad` has `justify-content: space-between`
- [ ] `.kort-rad` has `align-items: stretch`
- [ ] Understood: justify = along the board, align = across the board

### Kolumn inuti kortet (Cykel 7)
- [ ] `.kort` has `display: flex`, `flex-direction: column`, `gap: 0.5rem`
- [ ] Added `<a class="btn" href="#">` to each card
- [ ] `.kort .btn` has `margin-top: auto` — button aligns at bottom

---

## Study questions
1. What is the difference between Flexbox and CSS Grid?
2. What does `flex: 1 1 200px` mean — grow, shrink, basis?
3. Why does `gap` replace `margin` between flex items?
4. What is the "block-fällan" and why do cards stack by default?
5. When do you use `justify-content` vs `align-items`?
6. What does `flex-direction: column` do inside a card?
7. Why is `flex-wrap: wrap` important for responsive design?

## Key concepts
| Concept | Definition |
|---|---|
| **Flexbox** | One-dimensional layout — arranges items along ONE axis |
| **display: flex** | Turns element into a flex container |
| **gap** | Space between flex items (replaces margin) |
| **flex: 1 1 200px** | grow=1, shrink=1, basis=200px |
| **flex-wrap: wrap** | Allows items to wrap to next row |
| **justify-content** | Aligns items ALONG the main axis |
| **align-items** | Aligns items ACROSS the cross axis |
| **flex-direction: column** | Stacks items vertically inside a flex container |
