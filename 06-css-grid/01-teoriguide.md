# 01 — Teoriguide: CSS Grid

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när du bara staplar rutor — sedan bygger vi upp hur du lägger dem i rader *och* kolumner samtidigt. Det är inte magi. Det är en metod.

Ingen meny, inga media queries här. Ett `id` på sektionen (t.ex. `id="tavla"`) behövs senare för ett hopp från menyn — det är adress, inte Grid.

---

## Problemet först — "det är ju en lista"

Många tänker nu: "Jag har ju sex rutor. Det *är* ju ett schema." Andas.

**Dåligt läge:** Öppettider, banor eller programposter ligger **under varandra**. Du kan läsa dem. Du kan *inte* se "samma klockslag, två spår" som celler i ett plan. Det är en stapel — en riktning.

Examination 1 kräver att **schema/tidtabell** layoutas med **CSS Grid**: tider och spår i **rader och kolumner**. Flexbox (en riktning) räcker inte där. README-fråga 3 vill ha skillnaden med *ert* exempel.

Grid löser stapeln. Flex löser raden av liknande kort. Olika verktyg, olika sektioner.

---

## Två dimensioner — schackbräde, inte kö

**Metafor:** Tänk ett **schackbräde** eller ett **kalkylark**. Varje ruta har *både* en rad och en kolumn. Pjäsen står i en cell — inte i en kö vid ett enda disk. En **lägenhetsplan** är samma idé: rum bredvid varandra *och* ovanför/under varandra.

**Vad det är:** **CSS Grid** = tvådimensionell layout. Föräldern slår på rutnätet med `display: grid`. Du sätter kolumner med `grid-template-columns`. Barnen fyller celler; **rader** uppstår när det blir fler barn än kolumner (eller när du sätter rader explicit). `gap` = luft mellan cellerna.
**Varför det finns:** Vissa ytor *är* två axlar — tid × spår, dag × öppettid, bana × pass. En riktning räcker inte.
**Om det saknas / vad det INTE är:** Utan Grid (eller utan kolumnmall) får du en stapel även om du "tänkte rutnät". Grid är INTE Flexbox. Det är INTE "nyare och därför bättre på allt". Det är INTE magi i varje barn — rutnätet sitter på **föräldern**.

```css
.tavla {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 1rem;
}
```

`1fr 1fr 1fr` = tre kolumner, lika andelar av ledig bredd. `1fr` låter tekniskt — betyder "en rättvis bit". Färre `1fr` = färre kolumner, samma verktyg.

**Målsvar (säg högt / skriv i README):**
*"Grid är tvådimensionell layout — rader och kolumner samtidigt. Föräldern får `display: grid`, kolumnerna sätts med `grid-template-columns`, luft mellan cellerna med `gap`."*

---

## Tre rattar — display, kolumner, gap

Många tänker: "Jag skrev `display: grid` men det ser likadant ut." Stopp. Rutnät utan mall är ofta **en** kolumn.

| Ratt | Vad det är (+ bild) | Varför | Om saknas / INTE |
|------|---------------------|--------|------------------|
| `display: grid` | Slå på brädet på **föräldern** | Barnen blir celler | På varje barn = du rutade cellen, inte planet |
| `grid-template-columns` | Hur många kolumner, hur breda | Utan mall: en kolumn | INTE samma sak som Flex `flex-wrap` |
| Rader | Fylls när barnen tar slut på kolumnerna | Andra axeln | Du *kan* sätta `grid-template-rows` — behövs sällan först |
| `gap` | Springor mellan rummen | Celler ska inte kuddra | INTE padding inuti en cell (det är Box Model) |

**Problem först:** Bara `display: grid` → ofta en smal stapel. `grid` på varje `.ruta` → varje lapp är sitt eget bräde med ett rum. Kolumner på fel element = "Grid funkar inte".

**Målsvar (säg högt / skriv i README) — rattarna:**
*"Minst `display: grid` och `grid-template-columns` på föräldern, plus celler som innehåll. `gap` så rummen inte kuddra."*

---

## Flex vs Grid — README-fråga 3

**Metafor:** Flexbox är **en kö** — brickor på ett band, en riktning (rad *eller* kolumn). Grid är **planen** — rum i rader *och* kolumner.

**Vad skillnaden är:** Flex = en huvudriktning. Grid = två axlar samtidigt.
**Varför båda finns:** Highlights på eventsidan är liknande kort i rad → Flex. Schema där tid och scen ska sitta i celler → Grid.
**Om du blandar / INTE:** Att slänga Grid på korten "för att det är Exam-vecka" är fel verktyg. Att göra schemat i Flex och kalla det Grid i README är samma sak. Det är INTE "vilket ser snyggast ut".

På Examination 1: **Highlights = Flexbox. Schema = Grid.** Fråga 3 i README ska motiveras från *er* kod — inte en googlad definition.

**Målsvar (säg högt / skriv i README) — Flex vs Grid:**
*"Flexbox ordnar i en riktning (t.ex. liknande kort i rad). Grid styr både rader och kolumner (t.ex. en tavla där tider och spår ska ligga i celler). På eventsidan: Highlights = Flex, schema = Grid."*

---

## Metod — när du tvekar "Flex eller Grid?"

Det är inte magi. Tre frågor:

1. **Liknande saker i en riktning?** (kort i rad, länkar i rad) → **Flex**.
2. **Behöver jag rader och kolumner samtidigt?** (tavla, tid × spår) → **Grid**.
3. **Osäker?** Är det en kö — eller ett schackbräde / kalkylark?

Sätt `display: grid` på **behållaren**. Sätt kolumnmallen. Lägg innehållet som barn. Peka och säg *varför* den sektionen fick Grid.

**Vad metoden är:** Ett val, inte en tävling mellan verktyg.
**Varför den finns:** Exam 1 bedömer att rätt sektion har rätt layoutverktyg, plus att ni kan förklara det.
**Om den saknas:** Allt blir Flex, eller allt blir Grid, och fråga 3 blir luddig.

**Målsvar (säg högt / skriv i README) — metod:**
*"Liknande saker i en riktning → Flex. Behöver jag rader och kolumner samtidigt → Grid. Osäker? Är det en kö, eller ett schackbräde?"*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `display: grid` på varje ruta | Grid på **föräldern** — brädet, inte pjäsen |
| Bara `display: grid`, ingen `grid-template-columns` | Utan mall blir det ofta en kolumn |
| Byter Highlights till Grid "så det matchar" | Highlights = Flex enligt Exam. Schema = Grid |
| `1fr` är "pixlar jag inte förstår" | Andel av ledig yta — tre `1fr` = tre lika bitar |
| `gap` vs padding | `gap` mellan celler. Padding *inuti* cellen |
| Grid = "gör sidan snygg" | Grid = två axlar. Utseende är fortfarande Box Model / färg |
| Glömmer `id` på sektionen | Adress för senare hopp — inte en Grid-ratt |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad är tvådimensionell layout? (schackbräde / kalkylark)
2. Vilka rattar sitter på föräldern?
3. Varför schema → Grid och highlights → Flex? (en mening vardera)
4. Metodens tre frågor

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
