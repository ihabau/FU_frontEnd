# 02 — Visuellt: arv och affischen

Samma dresscode- och affisch-metafor som i teoriguiden — nu som flöde. Ingen Flex/Grid-karta: förälder → barn + toppsektion räcker.

GitHub renderar diagrammen nedan automatiskt.

---

## Dresscoden rinner ner

```mermaid
flowchart TD
  P["Förälder: .hero<br/>color + font-family"] --> C1["h1 — ingen egen color"]
  P --> C2["p — ingen egen color"]
  P --> C3["p.undantag — egen color"]
```

**Vad diagrammet visar:** Barn utan egen regel får förälderns röst. Barnet med egen `color` bryter dresscoden medvetet.
**Kom ihåg / INTE:** `background` och `padding` på `.hero` stannar på affischen. De rinner inte in i barnen som textfärg gör.

**Målsvar (säg högt / skriv i README):** *"Color och font på föräldern syns hos barnen om barnen inte sätter egna värden."*

---

## Vad ärvs — och vad sitter på lådan?

```mermaid
flowchart LR
  subgraph arvs [Dresscode — ärvs]
    A["color"]
    B["font-family"]
  end
  subgraph lada [Affischen — sätts på .hero]
    D["background"]
    E["padding / margin"]
  end
```

Till vänster: policyn. Till höger: pappret. Blanda inte ihop — det är den vanligaste missen inför README-fråga 2.

---

## Affischen på tavlan

```mermaid
flowchart TB
  subgraph tavla [Anslagstavlan — sidan]
    H["Hero / löpsedeln<br/>namn · bild · datum · plats · intro"]
    R["Resten av sidan<br/>inte Hero"]
  end
```

**Kom ihåg / INTE:** Hero är *ett papper* högst upp, inte hela tavlan. Semantisk `header` eller `section` så du kan peka i HTML.

---

## Metodkortet — tre steg

```mermaid
flowchart TD
  A["1. Förälder med t.ex. color"] --> B["2. Barn utan egen color"]
  B --> C["3. Det syns hos barnet = arv<br/>= README-exemplet"]
```

Utan steg 3 har du en definition. Examinationen vill ha *din* selektor.

---

## Checkpoint (privat)

Utan att titta på teoriguiden: säg vad som ärvs vs vad som sitter på affischen. Nämn Hero:s fem bitar. Jämför sen med diagrammen.

När kartan sitter: [03 — Övningar](./03-ovningar.md).
