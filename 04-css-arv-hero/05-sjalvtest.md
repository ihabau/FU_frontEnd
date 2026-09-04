# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad betyder **arv** i CSS?
2. Nämn två egenskaper som ofta ärvs — och en som *inte* ärvs på samma sätt.
3. Du har satt `color` på både `.hero` och varje `p` inuti. Vad är problemet när du byter tema?
4. Beskriv metoden: hur hittar du ett arv-exempel till README?
5. Vad är en **Hero** — och vilka fem bitar kräver Exam 1?
6. `head` eller `header` för den synliga toppen — vilken, och varför?
7. Varför sätter du `background` på Hero-lådan och inte "via arv" på barnen?
8. Peka i *din* kod (loppis, Åkanten eller AI-övning): en förälder-regel, ett barn, och **varför** det är arv — inte "det såg bra ut".

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. Vissa egenskaper (t.ex. `color`, `font-family`) på en förälder förs vidare till barnen om barnen inte sätter egna värden.
2. Ofta: `color`, `font-family` (typografi). Inte på samma sätt: `margin`, `padding`, `border`, `background`.
3. Du jagar samma ändring på många ställen och missar lätt någon. En förälder = en dresscode.
4. (1) Förälder med t.ex. `color`. (2) Barn utan egen `color`. (3) Det syns hos barnet = exemplet.
5. Välkomnande toppsektion. Exam 1: namn, bild/logotyp, datum, plats, kort beskrivning. Pekbar i HTML (`header`/`section`), stylad.
6. **`header`** (eller `section`) i `body`. **`head`** är meta om dokumentet — syns inte som affisch.
7. Bakgrund ärvs inte som textfärg. Du färgar pappret, inte barnens "kläder" med `background`.
8. Subjektivt — rimligt om du kopplar förälder → barn → egenskap. Fel om svaret bara är "AI skrev det" eller Flex som förklaring.

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen CSS:

- [ ] Målsvar arv — egna ord, högt
- [ ] Målsvar Hero — egna ord, högt
- [ ] Målsvar metod — egna ord, högt
- [ ] Ett konkret arv-exempel pekat i din kod

Då har du landat Hero- och arv-målet. Nästa paket: [05-flexbox](../05-flexbox/).
