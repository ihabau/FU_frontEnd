# 01 — Teoriguide: Flexbox & konkret feedback

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när liknande kort bara staplas som vanliga block — sedan slår vi på en riktning. Det är inte magi. Det är en metod.

Ingen Grid-layout här. En mening räcker: **Grid = när du behöver rader OCH kolumner samtidigt** — det tar [06-css-grid](../06-css-grid/). Idag: en hyllbräda.

---

## Problemet först — tre kort som en hög

Många tänker nu: "Jag har tre `article`. De ligger under varandra. Jag knuffar med `margin` tills det *ungefär* blir en rad." Andas.

**Dåligt läge:** Korten *finns*. De beter sig som tre tegelstenar i en trave. Olika höjd. Luckor som du gissar i pixlar. På smal skärm åker en bit utanför. Det är behovet Flexbox löser: **samma sorts bitar, i en riktning, med styrd luft**.

På Exam 1 heter den sektionen **Highlights** — aktivitetskort med bild + kort text. Formen är densamma även när du övar på lunchrätter eller träningspass: en behållare, flera likadana barn.

```html
<section class="meny">
  <h2>Dagens brickor</h2>
  <div class="kort-rad">
    <article class="kort">
      <img src="https://placehold.co/200x120" alt="Soppa" width="200" height="120" />
      <h3>Ärtsoppa</h3>
      <p>Torsdag. Med pannkaka.</p>
    </article>
    <!-- fler article ... -->
  </div>
</section>
```

Utan Flex på `.kort-rad` är det en stapel. Med Flex blir det en hylla.

---

## En riktning — böcker på EN hyllbräda

**Metafor:** Tänk **böcker på en hyllbräda**. En bräda. Böckerna (korten) står efter varandra. Du bestämmer hur de fördelas *längs* brädan, om de linjeras i höjd, och hur stor luft det är mellan ryggarna. Du ritar inte ett helt bokskåp med namngivna plan *och* fack samtidigt — det vore två riktningar.

Samma idé: **kläder på en stång**. Galgarna hänger i *en* linje. Du skjuter isär, samlar mot mitten, eller låter nästa plagg hoppa till en ny stång om den första tar slut (`flex-wrap`).

"En-dimensionell" låter akademiskt. Betyder egentligen: **en huvudriktning** — rad *eller* kolumn. Inte båda som ett schema.

**Vad det är:** Flexbox = layout i en riktning. Föräldern blir **flex-container** (`display: flex`). Barnen blir **flex-items** (dina kort).
**Varför det finns:** Så liknande bitar kan dela på en bräda utan margin-hack och gissningar.
**Om det saknas / vad det INTE är:** Flexbox är INTE "gör sidan snygg". Det är INTE Grid. Utan Flex (och utan annan layout) beter sig block som en trave. `display: flex` på fel element — t.ex. på *ett kort* istället för på raden — slår på hyllan på fel ställe.

**Målsvar (säg högt / skriv i README):**
*"Flexbox är en-dimensionell layout — vi ordnar barn i en rad eller en kolumn. Bra när liknande kort ska ligga i rad med jämna mellanrum (`gap`), och kunna wrappa."*

---

## Fem rattar — vad de faktiskt gör

Slå på hyllan på **behållaren** som *håller korten*, inte på `h2`:n ovanför och inte på varje kort "för säkerhets skull".

```css
.kort-rad {
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  gap: 1rem;
  flex-wrap: wrap;
}
```

| Egenskap | Vardagsbild (hyllan) | Vad den styr | Om den saknas |
|----------|----------------------|--------------|----------------|
| `display: flex` | Brädan är igång | Barnen blir items i en riktning | Vanlig block-stapel |
| `justify-content` | Fördelning *längs* brädan | Start, mitt, luft mellan (`space-between` …) | Default: packade mot start |
| `align-items` | Linje *tvärs* brädan | Olika höga böcker: stretch, center, start | Default: stretch (ofta ok på kort) |
| `gap` | Luft *mellan* ryggarna | Avstånd mellan items — en ratt | Du luras till `margin` på varje kort |
| `flex-wrap` | Får nästa bok byta rad? | `wrap` = ja när brädan tar slut; `nowrap` = allt på en linje | Default `nowrap` — kan trycka ut innehåll |

Riktning: default är **rad** (`flex-direction: row`). Kolumn = samma verktyg, andra hållet — fortfarande *en* dimension.

Du behöver inte memorera alla `justify-content`-värden idag. Du behöver kunna **peka**: den här rattet styr längs brädan, den här tvärs, `gap` är luften mellan.

---

## När Flex passar — tre frågor

Många tänker: "Ska jag alltid köra Flex nu när jag kan det?" Nej. Metod:

1. **Har jag liknande bitar** (kort) som ska ordnas?
2. **Räcker en riktning** (rad *eller* kolumn)? → Flexbox.
3. **Behöver jag rader och kolumner samtidigt** (ett schema)? → Grid — [06-css-grid](../06-css-grid/). Inte i det här paketet.

Highlights på eventsidan: tre–fyra kort, bild + text, i rad som kan wrappa. Det är hyllbrädan. Ett veckoschema med tider *och* scener är inte det — där tar Grid vid.

**Målsvar (säg högt / skriv i README) — metod:**
*"Har jag liknande bitar som ska ordnas? Räcker en riktning (rad eller kolumn)? Då Flexbox. Behöver jag rader och kolumner samtidigt — det är Grid, inte här."*

---

## Kortets inuti — fortfarande HTML-betydelse

Flex ordnar *lådorna*. Det ersätter inte semantik.

- Sektionen: `section` (t.ex. lunch, pass, senare Highlights).
- Varje kort: `article` om biten kan stå för sig (en rätt, ett pass, en höjdpunkt).
- Bild + kort text: `img` med `alt`, `h3`, `p`.
- Behållaren runt korten: en `div` med class är ok *här* — den *betyder* inte ett eget innehåll, den är hyllbrädan.

**Vad det INTE är:** En `div` per kort "för att Flex kräver div". Flex skiter i taggnamnet. Examinationen skiter inte i betydelsen.

Styling av *ett* kort (padding, border, bakgrund) är Box Model på barnet. `gap` på föräldern är luften *mellan* korten. Blanda inte: `gap` är inte padding inuti kortet.

---

## Feedback — peka på kod, inte på känsla

Kursen kräver att du kan ge **enklare feedback** på annans HTML/CSS. "Ser bra ut" räknas inte. Det är tomt. Det går inte att *göra* något med.

**Dåligt:** "Snyggt!" / "Bra jobbat."
**Bättre:** "Du har `display: flex` på `.kort-rad` men inget `gap` — korten kuddra; lägg `gap: 1rem`."
**Bättre:** "Korten är `div` utan betydelse — `article` vore tydligare för en självständig rätt."

**Vad det är:** En saklig mening: vad du *ser* (tagg eller egenskap) + vad som kan ändras.
**Varför det finns:** Nästa commit ska veta *vad*. Granskning i grupp och ägarskap kräver pekning, inte stämning.
**Om det saknas / INTE:** Feedback är INTE att betygsätta personen. INTE att lista tjugo saker. En konkret grej slår tre vaga.

Metod när du tvekar:

1. Titta på strukturen: vem är containern?
2. Välj **en** sak (saknar `gap`, Flex på fel element, fel tagg, ingen `flex-wrap`).
3. Skriv: `FEEDBACK: [vad jag ser] → [förslag]`.

**Målsvar (säg högt / skriv i README) — feedback:**
*"Bra feedback pekar på något konkret i koden (tagg, flex-egenskap, struktur) och säger vad som funkar eller vad som kan förbättras — inte bara 'snyggt'."*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `display: flex` på varje kort | Flex på *behållaren* som ska bli hyllan |
| `margin` på alla barn "som gap" | `gap` på containern |
| "Flex = Grid" | En riktning vs rader *och* kolumner. Grid = [06](../06-css-grid/) |
| `justify-content` när du menade höjdlinje | Längs brädan = justify. Tvärs = `align-items` |
| `nowrap` och kort som åker ur skärmen | `flex-wrap: wrap` när brädan tar slut |
| Feedback: "nice" | Tagg eller egenskap + förslag |
| Alla kort som `div` | `article` (eller annan betydelse) per bit |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad betyder en-dimensionell layout? (hyllbrädan)
2. Vilken selector får `display: flex` — containern eller korten?
3. `gap` vs padding — skillnad i en mening
4. En dålig vs en bra feedback-mening
5. När *inte* Flex — pekning mot Grid i en mening

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
