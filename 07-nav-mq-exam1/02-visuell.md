# 02 — Visuellt: hissknappar, sidfot och ihopvikt karta

Samma hiss- och kart-metaforer som i teoriguiden — nu som bild. Ingen Grid-genomgång: bara hopp, fot och när CSS byter regler.

GitHub renderar diagrammen nedan automatiskt.

---

## Knapp och skylt

```mermaid
flowchart LR
  N["nav: href='#schema'"] -->|"samma namn"| S["section id='schema'"]
```

**Vad diagrammet visar:** Hissknappen och våningsskylten.
**Kom ihåg / INTE:** Utan `#` eller med stavfel = död knapp. Det är INTE en ny HTML-fil.

**Målsvar (säg högt / skriv i README):** *"`href="#schema"` kräver `id="schema"` på samma sida."*

---

## Sidans våningar (Exam-sektioner)

```mermaid
flowchart TD
  NAV[nav — knapparna]
  H["#hero — intro"]
  SC["#schema — Grid-tavla"]
  HI["#highlights — Flex-kort"]
  F[footer — kontakt + sponsorer]
  NAV --> H
  NAV --> SC
  NAV --> HI
  H --> SC --> HI --> F
```

**Kom ihåg:** Schema-layouten är Grid (syskonpaketet). Highlights är Flex. Nav *pekar* — den byter inte verktyg på sektionerna.

---

## Media query — skrivbord vs ryggsäck

```mermaid
flowchart TD
  T["Testa smal viewport"] --> Q{"Kläms layouten?"}
  Q -->|Nej| OK[Bra — du har bevis]
  Q -->|Ja| M["@media max-width …"]
  M --> E["Ändra EN ratt<br/>t.ex. 1 kolumn i grid<br/>eller meny i kolumn"]
```

**Metafor:** Utslagen karta på skrivbordet vs ihopvikt i ryggsäcken. Samma innehåll, andra vik.
**INTE:** En extra "mobilfil". Inte gissa utan att smalna fönstret.

**Målsvar (säg högt / skriv i README):** *"Media query = CSS som bara gäller vid vissa bredder. Testa viewport först, skriv sen andra reglerna."*

---

## Checkpoint (privat)

Utan att titta: säg hiss-matchen högt, vad footern måste innehålla, och metoden smalt → query → en ratt. Jämför sen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
