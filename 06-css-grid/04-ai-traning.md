# 04 — AI-träning: Grid & ägarskap

AI kan spotta ur sig `display: grid` på sekunder. Det betyder inte att *du* äger tavlan. Här tränar du samma färdighet som Examination 1 kräver: **se vad som är svagt, ändra, förklara**.

Det är inte magi att "granska AI". Det är metoden: kö eller schackbräde — och rattarna på föräldern.

---

## Scenario — problem först

Du ber AI: *"Gör en snygg layout med Grid."*
Du får tillbaka något i stil med:

```html
<section style="display: grid;">
  <div style="display: grid; grid-template-columns: 200px;">Öppet</div>
  <div style="display: grid;">Stängt</div>
  <div class="card" style="display: flex;">Kort 1</div>
</section>
```

```css
div {
  display: grid;
  grid-template-columns: 1fr;
}
.cards {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

Det *kan* råka se ut som rutor. Det är svagt mot det här paketet:

- **Inline** `style=` blandar utseende in i HTML.
- **`display: grid` på varje barn** = många mini-bräden, inte en tavla.
- **`1fr` ensam** = en kolumn — du har ordet Grid men ingen andra axel.
- **`.cards` i Grid** när korten är liknande saker i en riktning = fel verktyg (det är Flex-jobb på eventsidan).

**Vad du tränar:** Feedback på AI-CSS + en tavla *du* äger.
**Varför:** Muntligt och README-fråga 3 kräver att *du* kan peka: förälder vs cell, Flex vs Grid.
**Vad det INTE är:** "AI skrev grid, alltså är schemat klart."

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt till AI (eller jobba bara mot snutten ovan) där du ber om en **öppettider-tavla** eller **simhallsbanor** i Grid. Spara prompten.

### Steg 2 — Granska (checklist)
Gå igenom svaret (AI:ns eller snutten) och kryssa:

- [ ] Sitter `display: grid` på **föräldern** — eller på varje ruta?
- [ ] Finns `grid-template-columns` med **mer än en** kolumn?
- [ ] Inline `style=` / extra layout du inte kan försvara?
- [ ] Har AI lagt Grid på en **kortsrad** som borde vara Flex?
- [ ] Kan du förklara `1fr` och `gap` muntligt?

Skriv **minst tre** konkreta feedback-punkter i formen:
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till `ovning-ai-grid/index.html` + `style.css`. Grid på föräldern, minst fyra celler, `gap`, extern CSS. Inga media queries, ingen meny. Spara filerna.

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller en `GRID-VAL.md` i mappen:

1. Vad var fel eller svagt i AI-förslaget (eller snutten)?
2. Vad ändrade du?
3. Varför spelar valet Flex vs Grid roll i Examination 1 (fråga 3 / rätt sektion)?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader sparade
- [ ] Peka på förälderns `display: grid` + kolumnmall — säg *varför*
- [ ] Peka på något du *tog bort* från AI — varför behövdes det inte?
- [ ] Reflektionens tre meningar klara

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: display:grid på varje div → flytta till föräldern, barnen är celler.`
- `FEEDBACK: grid-template-columns: 1fr ensam → minst två kolumner, t.ex. 1fr 1fr.`
- `FEEDBACK: style= på elementen → style.css + link.`
- `FEEDBACK: .cards i Grid → Flex; liknande kort i en riktning.`

**Målsvar (säg högt / skriv i README) — ägarskap:**
*"Jag tar emot AI-Grid som utkast, granskar förälder vs cell och Flex vs Grid, och behåller bara det jag kan peka ut."*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
