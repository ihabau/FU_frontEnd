# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad betyder **en-dimensionell** layout?
2. Vilket element ska ha `display: flex` — korten eller behållaren runt dem? Varför?
3. Vad gör `gap` som `margin` på varje barn *inte* gör lika rent?
4. `justify-content` vs `align-items` — längs eller tvärs hyllbrädan?
5. När använder du `flex-wrap`?
6. När ska du *inte* välja Flexbox — en mening (peka mot nästa verktyg utan att bygga det)?
7. Skriv en **dålig** och en **bra** feedback-mening om kod med Flex.
8. Peka i *din* kod (matsal, pass eller AI-övning): tre flex-egenskaper med **varför** — inte "det såg bra ut".

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. En huvudriktning: rad *eller* kolumn. Böcker på *en* bräda — inte ett helt skåp med plan och fack samtidigt.
2. **Behållaren** (hyllan). Korten är items. Flex på varje kort stylar kortets insida, inte raden.
3. `gap` sätter luft *mellan* items på containern. Margin på barnen blir lätt ojämnt och träffar ytterkanter du inte menade.
4. **Justify** = längs huvudaxeln. **Align-items** = tvärs (t.ex. höjd om korten är olika höga).
5. När brädan tar slut och nästa kort ska få byta rad (`wrap`) i stället för att tryckas ur.
6. När du behöver **rader och kolumner samtidigt** → Grid, se 06. Inte Highlights-raden.
7. Dålig: "Snyggt!" Bra: pekar t.ex. "saknar `gap` på `.kort-rad`" eller "`div` istället för `article`".
8. Subjektivt — rimligt om du kopplar egenskap → effekt på hyllan. Fel om "AI skrev Grid" eller bara "ser bra ut".

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen CSS:

- [ ] Målsvar Flexbox — egna ord, högt
- [ ] Målsvar feedback — egna ord, högt
- [ ] Målsvar metod (när Flex / inte) — egna ord, högt
- [ ] Tre FEEDBACK-rader någonstans i övning eller AI-träning

Då har du landat Flex-målet. Nästa: [06-css-grid](../06-css-grid/) och [07-nav-mq-exam1](../07-nav-mq-exam1/).
