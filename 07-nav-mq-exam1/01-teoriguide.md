# 01 — Teoriguide: Nav, footer, Media Queries & Exam 1

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när sidan är en lång rulle utan knappar, utan sidfot och med desktop-regler på en smal skärm — sedan bygger vi hopp, fot och villkorad CSS. Det är inte magi. Det är matchande adresser och andra regler när ytan krymper.

Grid-rattarna (schema-tavlan) sitter i [06-css-grid](../06-css-grid/). Här: meny, footer, `@media` och vad Examination 1 faktiskt kräver.

---

## Problemet först — tre saker som saknas

Många tänker nu: "Sidan *finns*. Scrolla." Andas.

**Dåligt läge:**

1. Tre sektioner under varandra — men ingen väg att **hoppa** till Schema.
2. Ingen **sidfot** med kontakt eller sponsorer.
3. Tre kolumner (eller en bred Hero) som **krossas** när fönstret är smalt — du har inte testat.

Examination 1 kräver alla tre: **nav med ankare**, **footer (kontakt + fiktiva sponsorer)**, **responsivitet via Media Queries**. Plus Hero, schema i Grid, highlights i Flex, README ×3, gemensamt GitHub, synliga commits, ägarskap.

---

## Nav — hissknappar som måste matcha våningen

**Metafor:** Tänk **hissknappar** eller en **våningstavla** i entrén. Knappen "3" fungerar bara om våning 3 har samma nummer på skylten. `href="#schema"` är knappen. `id="schema"` är skylten. Utan match: klick i tomma intet.

**Vad det är:** `nav` = navigationsområde. Ankarlänk = länk till ett `id` **på samma sida** (`#` betyder "här", inte en ny fil). Examination 1: länkar till t.ex. `#hero`, `#schema`, `#highlights`.
**Varför det finns:** Besökaren ska hitta sektionerna utan att jaga i rullen.
**Om det saknas / vad det INTE är:** Utan matchande `id` är knappen död. Det är INTE en länk till `schema.html`. Det är INTE styling. Stavfel (`#Schema` vs `id="schema"`) räknas som miss.

```html
<nav class="nav">
  <a href="#hero">Hem</a>
  <a href="#schema">Schema</a>
  <a href="#highlights">Höjdpunkter</a>
</nav>

<header id="hero">…</header>
<section id="schema">…</section>
<section id="highlights">…</section>
```

Länkar i rad är **en riktning** — Flex på `.nav` är rimligt (samma Flex du redan kan). Det är INTE att göra menyn till Grid-tavla.

**Målsvar (säg högt / skriv i README):**
*"Länkar i `nav` pekar på `id` på samma sida (`href="#hero"` kräver `id="hero"`). Klick scrollar till sektionen — som hissknappar som måste matcha våningens skylt."*

---

## Footer — skylten längst ner

**Vad det är:** `footer` = sidfot. Examination 1: **kontaktinformation** + **fiktiva sponsorer**.
**Varför det finns:** Det är den semantiska platsen för "hur når ni oss / vem stöttar".
**Om det saknas / INTE:** En tom `div` längst ner räcker inte mot kravet. Det är INTE nav. Sponsorer får vara påhittade — de ska **synas**.

```html
<footer class="footer">
  <p>Kontakt: info@bakluckan.example</p>
  <p>Sponsorer: Fiktiv Cloud AB · Demo Drinks · Pixel Partner</p>
</footer>
```

**Målsvar (säg högt / skriv i README) — footer:**
*"Sidfoten har kontakt plus fiktiva sponsorer. `footer` är rätt tagg — inte en slump-div längst ner."*

---

## Media query — fäll ihop kartan

Många tänker: "Responsiv… det låter som en hel kurs." Andas.

**Metafor:** En **papperskarta** utslagen på skrivbordet får plats med tre kolumner. I **ryggsäcken** måste du **fälla ihop** den — samma karta, andra vik. Eller: på skrivbordet sprider du sakerna; i ryggsäcken packar du **en sak i bredd**. `@media` = de andra reglerna när ytan är smal.

**Vad det är:** En **media query** = CSS som bara gäller vid vissa skärmbredder, t.ex. `@media (max-width: 600px)`.
**Varför det finns:** Desktop-layout krossar ofta mobil. Examination 1: sidan ska anpassa sig så layouten inte går sönder.
**Om det saknas / INTE:** Utan query (eller utan **test**) gissar du. Det är INTE en magisk "mobilknapp". Det är INTE JavaScript. Du **ändrar en ratt** du redan har — t.ex. `grid-template-columns: 1fr` på schemat, eller `flex-direction: column` på menyn.

```css
@media (max-width: 600px) {
  .tavla {
    grid-template-columns: 1fr;
  }
}
```

**Testa viewport:** DevTools → enhetsverktyg / smalt fönster. Ser du klämt? Då skriver du query. Ser du inget fel för att du aldrig smalnade? Då har du inte testat.

**Metod — responsiv check:**

1. DevTools → smal viewport.
2. Ser något trasigt ut?
3. Skriv `@media (max-width: …)` och justera **en** sak.

**Målsvar (säg högt / skriv i README) — media query:**
*"En media query är CSS som bara gäller vid vissa skärmbredder. Jag anpassar t.ex. kolumner så smal vy inte krossar layouten — andra regler när kartan måste fällas ihop."*

---

## Examination 1 — vad du ska kunna peka på

Ingen ny teknik utöver det här paketet + Grid i 06. Kraven i elevspråk:

| Krav | Vad du gör | Vad du ser när det är klart |
|------|------------|-----------------------------|
| Hero | Toppsektion med namn, bild/logotyp, datum, plats, kort text | En tydlig intro högst upp |
| Schema | Program/tider i **CSS Grid** | Rader och kolumner — inte bara en lista |
| Highlights | Kort i **Flexbox** | Liknande kort i en riktning |
| Nav | Ankare till `#hero` `#schema` `#highlights` (eller era id) | Klick hoppar; id matchar |
| Footer | Kontakt + fiktiva sponsorer | Syns längst ner |
| MQ | Minst en `@media` + testa smal vy | Layouten går inte sönder på smalt |
| README | Tre frågor: semantik, arv, Flex vs Grid | Egna meningar från *er* kod |
| GitHub | Gemensamt repo | Alla syns i commits (eller namn i meddelandet vid samma dator) |
| Ägarskap | AI ok | Du kan förklara varje rad du behåller |

**Vad ägarskap är:** Du förstår, felsöker och försvarar koden.
**Varför det finns:** Genererad kod utan förklaring = inget ägarskap.
**Om det saknas / INTE:** Det är INTE "AI förbjudet". Det är INTE "det kompilerar så det är G".

**Målsvar (säg högt / skriv i README) — ägarskap:**
*"AI får användas, men jag måste förstå, felsöka och försvara koden. Annars saknas ägarskap — och det är IG-risk."*

---

## Metod — död länk eller klämd layout?

1. **Klick gör inget?** Jämför `href="#schema"` med `id="schema"` — samma namn, `#` bara i länken.
2. **Smal skärm ser trasig ut?** DevTools → smalt → en `@media` som ändrar *en* ratt.
3. **Exam-tvekan?** Gå listan ovan. Saknas Grid på schemat → [06-css-grid](../06-css-grid/). Saknas Flex på korten → Flex-paketet.

**Målsvar (säg högt / skriv i README) — metod nav:**
*"Knappen och skylten ska ha samma namn. Utan `id` är hissknappen död."*

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `href="schema"` utan `#` | `#` = hopp på samma sida |
| `id` med annat namn eller stor bokstav | Exakt match, versaler räknas |
| Nav-länkar till andra HTML-filer | Exam: sektioner på **samma** sida |
| Footer utan kontakt/sponsorer | Båda ska synas — fiktiva sponsorer ok |
| `@media` utan att smalna fönstret | Testa viewport, annars gissar du |
| Byter schema till Flex "så det får plats" | Schema förblir Grid; query ändrar *mallen* (t.ex. en kolumn) |
| En person pushar allas zip | Historiken ska visa gruppen |
| AI-meny med JavaScript | Inte i den här kursdelen — `a href="#…"` räcker |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad måste matcha mellan `href="#hero"` och HTML?
2. Vad ska footern innehålla enligt Exam 1?
3. Vad är en media query — och hur testar du den?
4. Lista funktionskraven ur minnet (Hero, Grid-schema, Flex-kort, nav, footer, MQ).
5. Ägarskap i en mening.

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
