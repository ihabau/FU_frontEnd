# 05 — Självtest

Svara **först** utan att titta på facit. Skriv i Docs/anteckningar — privat, för dig. Sikta på målsvar du kan *säga högt*.

Sedan: öppna facit och rätta dig.

---

## Frågor

1. Vad är **tvådimensionell layout** på en mening? (gärna schackbräde / kalkylark)
2. Vilka rattar måste sitta på **föräldern** för att du ska få ett rutnät?
3. Du skrev `display: grid` men allt ligger i en kolumn. Vad saknas oftast?
4. Varför sätter du **inte** `display: grid` på varje cell?
5. Vad gör `1fr`?
6. Skillnaden **Flexbox vs Grid** — och hur fördelar Examination 1 dem på eventsidan?
7. Beskriv **metoden** när du tvekar: Flex eller Grid?
8. Peka i *din* kod (Kajen-tavlan, simhallen eller AI-övningen): föräldern, kolumnmallen och **varför** — inte "AI sa åt mig".

---

## Facit

<details>
<summary>Visa facit (målsvar-nivå)</summary>

1. Rader **och** kolumner samtidigt — som ett schackbräde eller kalkylark, inte en kö.
2. Minst `display: grid` och `grid-template-columns` (plus innehållsceller). `gap` starkt rekommenderat.
3. `grid-template-columns` med mer än en kolumn — mall saknas.
4. Rutnätet är **brädet** (föräldern). Cellen är pjäsen. Grid på varje barn = många enrummare.
5. En **andel** av ledig bredd. Tre `1fr` = tre lika kolumner.
6. Flex = en riktning (Highlights/kort). Grid = två axlar (schema/tavla). Exam: Highlights Flex, schema Grid.
7. (1) Liknande saker i en riktning → Flex. (2) Rader + kolumner samtidigt → Grid. (3) Kö eller schackbräde?
8. Subjektivt — rimligt om du kopplar ratt → förälder och val → sektion. Fel om svaret bara är "AI skrev grid".

</details>

---

## Klart för paketet?

Om dina svar ligger nära facit, övningarna är gjorda, och du kan peka i egen CSS:

- [ ] Målsvar Grid — egna ord, högt
- [ ] Målsvar Flex vs Grid — egna ord, högt
- [ ] Målsvar metod — egna ord, högt
- [ ] Förälder / kolumner / gap pekade i din kod

Då har du landat Grid-målet. Nav, footer och Exam-start: [07-nav-mq-exam1](../07-nav-mq-exam1/).
