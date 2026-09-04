# 04 — AI-träning: nav, MQ & ägarskap

AI kan spotta ur sig en "modern meny" på sekunder. Det betyder inte att *du* äger hoppen. Här tränar du samma färdighet som Examination 1 kräver: **se vad som är svagt, ändra, förklara**.

Det är inte magi att "granska AI". Det är hiss-matchen + en query du testat.

---

## Scenario — problem först

Du ber AI: *"Lägg till navigation och gör sidan responsiv."*
Du får tillbaka något i stil med:

```html
<div class="menu">
  <button onclick="location.href='hero.html'">Hem</button>
  <a href="/schema">Schema</a>
  <a href="#Highlights">Höjdpunkter</a>
</div>
<div class="bottom">Maila oss kanske</div>
```

```css
@media screen {
  .menu { display: grid; }
}
.nav {
  position: sticky;
  /* hamburger + 40 rader JS utelämnade */
}
```

Det *kan* se ut som en meny. Det är svagt mot det här paketet:

- **Andra filer / `onclick`** — Exam vill ha ankare på **samma sida**.
- **`#Highlights` vs `id="highlights"`** — versaler = död knapp.
- **Footer saknas** eller är en `div` utan kontakt + sponsorer.
- **`@media screen` utan `max-width`** = nästan alltid sann — du har inte "andra regler när det är smalt".
- Extra **JS / hamburger** du inte kan försvara i den här kursdelen.

**Vad du tränar:** Feedback + en meny och query *du* äger.
**Varför:** Muntligt och Exam kräver att *du* pekar: `href` ↔ `id`, vad queryn gör, vad footern innehåller.
**Vad det INTE är:** "AI sa hamburger, alltså är det proffsigt."

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt (eller jobba mot snutten) där du ber om nav + footer + responsivitet för en **loppmarknad** eller **simklubb**. Spara prompten.

### Steg 2 — Granska (checklist)
Kryssa mot koden du fick:

- [ ] `nav` + `href="#…"` + matchande `id` — eller knappar/JS/andra sidor?
- [ ] Versaler / stavning som skulle döda hoppet?
- [ ] `footer` med kontakt **och** fiktiva sponsorer?
- [ ] `@media` med en **bredd** du kan testa — eller en query som alltid gäller?
- [ ] Layoutverktyg du inte kan förklara (sticky, grid-på-meny-som-tavla, JS)?

Skriv **minst tre** rader:
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till `ovning-ai-nav/index.html` + `style.css`. Tre ankare som fungerar, footer med båda kraven, en `@media` du har testat i smal viewport. Inget JS. Spara filerna.

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller `NAV-MQ.md`:

1. Vad var svagt i förslaget?
2. Vad ändrade du?
3. Varför spelar ägarskap roll när gruppen lämnar eventsidan (kod du inte kan peka i)?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader
- [ ] Peka på `href` + `id` + `@media` — säg *varför*
- [ ] Peka på något du *tog bort* från AI
- [ ] Reflektion klar

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: href='hero.html' / onclick → a href="#hero" + id="hero" på samma sida.`
- `FEEDBACK: #Highlights → samma versaler som id, t.ex. highlights.`
- `FEEDBACK: div.bottom utan sponsorer → footer med kontakt + fiktiva namn.`
- `FEEDBACK: @media screen utan max-width → t.ex. max-width: 600px och testa smalt.`
- `FEEDBACK: hamburger-JS → stryk; ankare räcker här.`

**Målsvar (säg högt / skriv i README) — ägarskap:**
*"Jag tar emot AI-meny som utkast, granskar ankare och query, och behåller bara det jag kan peka ut."*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
