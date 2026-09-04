# 04 — AI-träning: arv, Hero & ägarskap

AI kan spotta ur sig en "snygg topp" på sekunder. Det betyder inte att *du* äger arvet. Här tränar du samma färdighet som Exam 1 README-fråga 2 kräver: **se vad som är svagt, ändra, peka**.

Det är inte magi att "granska AI". Det är dresscode-metoden + affischen.

---

## Scenario — problem först

Du ber AI: *"Gör en snygg Hero-sektion till min sida."*
Du får tillbaka något i stil med:

```html
<head>
  <style>
    h1 { color: navy; }
    p { color: navy; }
    span { color: navy; }
  </style>
</head>
<body>
  <div class="hero" style="display: flex; gap: 2rem; background: gold;">
    <div>Välkommen</div>
    <div>Ett event</div>
  </div>
</body>
```

Det *kan* se "designat" ut. Det är svagt mot det här paketet:

- **`color` på varje barn** — ingen dresscode, tre ställen att jaga.
- **`<style>` i HTML** + **inline `style=`** — utseende inne i strukturen.
- **`div` för toppen** — säger inget om betydelse (`header`/`section`).
- **Saknar bild, datum, plats, beskrivning** — inte en Hero du kan försvara mot Exam 1.
- **`display: flex`** — layout du inte ska gömma dig bakom här.

**Vad du tränar:** Feedback på AI-CSS + en Hero *du* äger, med ett pekbart arv.
**Varför:** Muntligt och README-fråga 2 kräver att *du* kan peka: förälder, barn, egenskap.
**Vad det INTE är:** "AI gjorde den snygg, alltså är arv löst."

---

## Din uppgift (ca 45–75 min)

### Steg 1 — Prompt
Skriv en egen prompt till AI (eller jobba bara mot snutten ovan utan ny AI) där du ber om en välkomst-topp för t.ex. en simhall, loppis eller bakluckeloppis. Spara prompten. Be *inte* om Flex/Grid.

### Steg 2 — Granska (checklist)
Gå igenom svaret (AI:ns eller snutten) och kryssa:

- [ ] Extern `style.css` + `link` — eller `<style>` / inline?
- [ ] `color`/`font` på föräldern — eller upprepat på varje barn?
- [ ] Semantisk `header`/`section` — eller `div`?
- [ ] Fem Hero-bitar: namn, bild, datum, plats, intro?
- [ ] Flex/Grid/`position` som du **inte** kan förklara i det här paketet?
- [ ] Kan du peka ett arv-exempel muntligt?

Skriv **minst tre** konkreta rader:
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`

### Steg 3 — Anpassa
Skriv om till `ovning-ai-hero/index.html` + `style.css`. Semantisk Hero, fem bitar, arv från förälder, bakgrund + padding på affischen. Inget Flex/Grid. Tema: **inte** festival — t.ex. kallbad eller loppislapp.

### Steg 4 — Reflektion (3 meningar)
Skriv i anteckningar eller en `ARV.md` i mappen:

1. Vad var svagt i förslaget?
2. Vad ändrade du?
3. Varför spelar pekningen (förälder + barn) roll för Exam 1 README-fråga 2?

---

## Klart-check (peka i DIN omskrivna kod)

- [ ] Tre FEEDBACK-rader sparade
- [ ] Peka på arv-raden + ett barn utan egen `color` — säg *varför*
- [ ] Peka på något du *tog bort* från AI (t.ex. flex eller `div`)
- [ ] Reflektionens tre meningar klara

---

## Facit-riktning (titta efter du granskat själv)

Exempel på giltig feedback (dina egna ord får skilja sig):

- `FEEDBACK: color på h1, p och span → en color på .hero, barnen ärver.`
- `FEEDBACK: div.hero → header eller section, det är sidans topp.`
- `FEEDBACK: display flex → ta bort; inte det här paketet.`
- `FEEDBACK: saknar bild/datum/plats → fem bitar, inte bara "Välkommen".`
- `FEEDBACK: style= och style-tagg → style.css + link.`

**Målsvar (säg högt / skriv i README) — ägarskap:**
*"Jag tar emot AI-CSS som utkast, granskar arv och Hero-innehåll, och behåller bara det jag kan peka ut."*

---

Nästa: [05 — Självtest](./05-sjalvtest.md).
