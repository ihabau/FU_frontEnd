# 02 — Visuellt: CSS Grid

Samma schackbräde / kalkylark som i teoriguiden — nu som bild. Ingen meny-karta: föräldern, kolumnerna och valet Flex vs Grid räcker.

GitHub renderar diagrammen nedan automatiskt.

---

## Stapel vs bräde

```mermaid
flowchart LR
  subgraph fel [Utan kolumnmall]
    A1[Ruta] --> A2[Ruta] --> A3[Ruta]
  end
  subgraph ratt [Med Grid på föräldern]
    B1[cell] --- B2[cell] --- B3[cell]
    B4[cell] --- B5[cell] --- B6[cell]
  end
```

Till vänster: en riktning — en kö. Till höger: rader *och* kolumner — ett kalkylark.

**Kom ihåg / INTE:** `display: grid` utan `grid-template-columns` ser ofta ut som vänster sida. Det är INTE att "Grid är trasigt".

---

## Rattarna på föräldern

```mermaid
flowchart TD
  P["Föräldern .tavla"] --> D["display: grid<br/>slå på brädet"]
  P --> C["grid-template-columns<br/>hur många rum i bredd"]
  P --> G["gap<br/>springor mellan rum"]
  D --> K["Barnen = celler"]
  C --> K
  K --> R["Rader fylls när kolumnerna tar slut"]
```

**Vad diagrammet visar:** Brädet är containern. Pjäsen är barnet.
**Målsvar (säg högt / skriv i README):** *"Grid på föräldern. Kolumnmall + celler. Rader kommer när det blir fler barn än kolumner."*

---

## Flex eller Grid?

```mermaid
flowchart TD
  Q["Vad ska ordnas?"] --> A{"En riktning — liknande saker?"}
  A -->|Ja, t.ex. kort i rad| F["Flexbox"]
  A -->|Nej — två axlar, t.ex. tid × spår| G["CSS Grid"]
```

**Kom ihåg / INTE:** Inte "vilket är bäst". Examination 1: Highlights → Flex. Schema → Grid. README-fråga 3 = *ert* exempel.

**Målsvar (säg högt / skriv i README):** *"Kö → Flex. Schackbräde / kalkylark → Grid."*

---

## Checkpoint (privat)

Utan att titta på teoriguiden: säg de tre rattarna högt och varför Highlights inte ska bytas till Grid. Jämför sen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
