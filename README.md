# MU26 — Frontend Grundkurs

Folkuniversitetet MU26: Basic Frontend Programming exercises.

Course book: https://github.com/linuszocom/mu26-frontend-grundkurs

---

## 🛑 Don't clone the source repo

The source repo is a **read-only digital textbook**. Browse it in the browser. Code your own work locally in VS Code and version it in your own repos (this one).

---

## 📚 Material structure (`01`–`05`)

Each lesson folder contains five files with fixed roles:

| File | Role | What you do |
|:---|:---|:---|
| **`01-teoriguide.md`** | **Textbook** | Explains principles, metaphors, and *target answers* for examination. |
| **`02-visuell.md`** | **Diagrams** | Mental models, flows, and structure maps (Mermaid). |
| **`03-ovningar.md`** | **Exercises** | Hands-on coding from scratch with clear *Done* checkmarks. |
| **`04-ai-traning.md`** | **AI review** | Spot weaknesses in AI-generated code and adapt it so you own it. |
| **`05-sjalvtest.md`** | **Self-test** | Short questions with hidden answers under clickable tabs. |

### Study tracks
- 🟢 **Attended the lesson:** Do **`03`** (exercises) + **`05`** (self-test). Use `01` as reference when stuck.
- 🟡 **Missed the lesson:** Do the full chain: **`01` → `02` → `03` → `04` → `05`**.

---

## 🌐 HTML in this course

HTML is covered in **Vecka 35 — Lesson 01: HTML-semantik** (`completed/w35-first-page` branch).

**What you learn:**
- HTML document skeleton (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`)
- Semantic tags: `<header>`, `<main>`, `<footer>`, `<section>`, `<article>`, `<nav>`
- Why semantics matter for accessibility and SEO
- Adding text, images, links, and lists
- Image attributes: `src`, `alt`, `width`, `height`

**Target answers for examination:**
- *"Varför använder vi semantiska taggar istället för div?"* — Screen readers and search engines understand page structure. Semantic tags convey meaning; `<div>` conveys nothing.
- *"Vad gör `<!DOCTYPE html>`?"* — Tells the browser to render in standards mode (HTML5).
- *"Vad krävs för att ett `img`-element ska vara tillgängligt?"* — A descriptive `alt` attribute that conveys the image's purpose.

**Branch:** `completed/w35-first-page` — contains full 01–05 course material + weekly roadmap.

---

## 🗺️ Branch overview

### Completed ✅
| Branch | Topic | Week | Material |
|---|---|---|---|
| `completed/w35-first-page` | HTML semantics & first page | W35 | 01-html-semantik (01–05) |
| `completed/w35-git-exercise` | Git & GitHub fundamentals | W35 | 02-git-github (01–05) |
| `completed/w35-css-syntax` | CSS syntax & Box Model | W35 | 03-css-box-model (01–05) |

### In progress 🔵
| Branch | Topic | Week |
|---|---|---|
| `w36-04-css-arv-hero` | CSS inheritance & Hero section | W36 |
| `w36-05-flexbox` | Flexbox layout | W36 |
| `w36-06-css-grid` | CSS Grid | W36 |
| `w36-07-nav-mq-exam1` | Nav, media queries & Exam 1 | W36 |

---

## ⏰ Weekly schedule
- **Mon / Wed / Fri (13:00–16:00):** Live lesson in Teams
- **Tue / Thu:** Self-study, exercises, AI review, repetition

---

## How to use
```bash
git checkout <branch-name>
```
Each branch has its own `README.md` with checklists, study questions, and links to the course material.
