# 04 — AI-träning: Flexbox, feedback & ägarskap

AI kan lägga `display: flex` på *allt* och kalla det layout. Det betyder inte att *du* äger hyllan. Här tränar du: **se vad som är svagt, ändra, förklara** — plus samma sakliga feedback som kursplanen kräver.

Det är inte magi. Det är en riktning + pekning.

---

## Scenario — problem först

Du ber AI: *"Lägg korten i en snygg rad."*
Du får tillbaka något i stil med:

```html
<section style="display: grid; grid-template-columns: 1fr 1fr 1fr;">
  <div>Kort 1</div>
  <div>Kort 2</div>
  <div>Kort 3</div>
</section>
```

```css
div {
  display: flex;
  margin: 30px;
  justify-content: center;
}
```

Plus kommentaren: *"Ser bra ut! Modern layout."*

Det *kan* råka se ut som en rad. Det är svagt mot det här paketet:

- **Grid** (`grid-template-columns`) är nästa verktyg — inte det du ska gömma Flex bakom här.
- **`display: flex` på varje `div`** — hyllan sitter på barnen, inte på raden.
- **`margin: 30px` på alla `div`** istället för `gap` på containern.
- **Inga bilder, ingen `article`** — inte kortformen bild + text.
- **Feedbacken "ser bra ut"** är tom. Den pekar på noll egenskaper.

**Vad du tränar:** FEEDBACK-rader + en Flex-rad *du* äger.
**Varför:** Exam 1 Highlights ska vara Flex. README-fråga 3 (Flex-sidan) kräver att du kan säga *varför en riktning*.
**Vad det INTE är:** "Grid är tre kolumner, alltså är Flex löst."

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt (eller jobba mot snutten) där du ber om en rad **lunchkort** eller **passkort** (bild + kort text). Spara prompten. Be om Flex — inte Grid.

### Steg 2 — Granska (checklist)
Kryssa mot koden du fick:

- [ ] `display: flex` på *behållaren* runt korten — eller på varje kort / på `section` med Grid?
- [ ] `gap` — eller bara `margin`?
- [ ] `flex-wrap` om raden kan bli trång?
- [ ] Semantik: `article` per kort, `img` + text?
- [ ] Grid / float / `position` som du **inte** ska använda här?
- [ ] Kan du förklara `justify-content` och `align-items` om de finns?

Skriv **minst tre** rader:
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`
Minst en rad ska såga tomt beröm om det fanns ("ser bra ut" → peka på en egenskap istället).

### Steg 3 — Anpassa
Skriv om till `ovning-ai-flex/index.html` + `style.css`. Tre–fyra kort, Flex på raden, `gap`, `flex-wrap`. Tema: matsal eller gym — inte event-highlights. Ingen Grid.

### Steg 4 — Reflektion (3 meningar)

1. Vad var svagt i förslaget?
2. Vad ändrade du?
3. Varför är "en riktning / liknande kort" viktigt när eventsidans Highlights ska motiveras i README?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader
- [ ] Peka: containern med `display: flex` + `gap` — säg *varför*
- [ ] Peka på något du *tog bort* (t.ex. Grid eller flex på varje barn)
- [ ] Reflektion klar

---

## Facit-riktning (titta efter du granskat själv)

- `FEEDBACK: display grid + template-columns → Flex på en behållare; Grid är 06.`
- `FEEDBACK: display flex på varje div → flex på rad-behållaren.`
- `FEEDBACK: margin 30px på alla div → gap på containern.`
- `FEEDBACK: div-kort utan bild → article + img + kort text.`
- `FEEDBACK: "ser bra ut" → peka t.ex. saknad gap / fel tagg.`

**Målsvar (säg högt / skriv i README) — ägarskap:**
*"Jag tar emot AI-layout som utkast, granskar vilken element som är hyllan och vilka rattar som sitter där, och behåller bara det jag kan peka ut."*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
