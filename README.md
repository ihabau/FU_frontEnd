# W36-04 — CSS-arv & Hero-sektionen

> 🔵 **In progress** — Folkuniversitetet MU26, Vecka 36 (Mon 31/8 + Tue 1/9)

## Topic
CSS inheritance (ärv) + Hero section for an event page.

Course material: https://github.com/linuszocom/mu26-frontend-grundkurs/tree/main/vecka-36/04-css-arv-hero
Teaching guide: https://regal-choux-578278.netlify.app/v36-t1-arv-hero/index.html

---

## 🟢 Track A — Attended lesson (Mon 13:00–16:00)
Do these in order:
- [ ] `03-ovningar.md` — exercises
- [ ] `05-sjalvtest.md` — self-test
- Use `01-teoriguide.md` as reference when stuck

## 🟡 Track B — Missed lesson
Do the full chain:
- [ ] `01-teoriguide.md` — theory
- [ ] `02-visuell.md` — diagrams/mental models
- [ ] `03-ovningar.md` — exercises
- [ ] `04-ai-traning.md` — AI code review
- [ ] `05-sjalvtest.md` — self-test

---

## Checklist — Cykel 1–5 (Bas)

### Setup
- [ ] Created `v36-hero-camp` repo on GitHub
- [ ] Created `index.html` + `style.css`
- [ ] Linked CSS in `<head>`: `<link rel="stylesheet" href="style.css">`
- [ ] Page renders in browser

### Semantisk Hero (Cykel 2)
- [ ] Created `<header class="hero">` in `<body>`
- [ ] Added `h1` with event name
- [ ] Added `img` from placehold.co with descriptive `alt`, `width`, `height`
- [ ] Added `p.datum`, `p.plats`, `p.tagline`
- [ ] Five unstyled elements visible in browser

### Lådan — Box Model (Cykel 3)
- [ ] `.hero` has `background-color: #0f3d3e`
- [ ] `.hero` has `padding: 3rem 1.5rem`
- [ ] Box visible with dark background and padding

### CSS-arv (Cykel 5)
- [ ] Removed manual color rules on each child
- [ ] Set `color: #ffffff` on `.hero` ONCE
- [ ] Set `font-family: sans-serif` on `.hero` ONCE
- [ ] All children inherit text color automatically
- [ ] **Test:** Changed `.hero` color → all children follow

### README
- [ ] Created `README.md` explaining CSS inheritance
- [ ] Used three-step method: parent → children → result
- [ ] Concrete example from own Hero code

---

## Checklist — Cykel 6–7 (Fördjupning)

### Bryta arvet — .btn (Cykel 6)
- [ ] Added `<a class="btn" href="#">Köp biljett</a>` to Hero
- [ ] `.hero .btn` has own background `#fde68a` and color `#0f172a`
- [ ] Button breaks inheritance — rest of text stays white

### Ny komponent — .card (Cykel 7)
- [ ] Created `<article class="card">` below Hero
- [ ] `.card` has own `background-color: #f1f5f9`, `padding`, `color`
- [ ] Card text inherits from `.card`, not `.hero`

---

## Study questions
1. What is CSS inheritance — which properties are inherited and which are not?
2. What is the difference between `<head>` and `<header>`?
3. Why must every `<img>` have an `alt` attribute?
4. What is Box Model and why does padding/background NOT inherit?
5. How do you break inheritance with a more specific selector?
6. What is the three-step method for explaining CSS code?

## Key concepts
| Concept | Definition |
|---|---|
| **CSS Inheritance** | Text properties (color, font-family) pass from parent to child |
| **Box Model** | padding, border, margin stay on the element — do NOT inherit |
| **Semantic HTML** | Tags chosen by meaning, not appearance |
| **Specificity** | More specific selectors override inherited values |
| **Hero section** | Large welcome area at top of landing page |
