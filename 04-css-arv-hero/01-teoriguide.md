# 01 — Teoriguide: CSS-ärv & Hero

> **Så använder du denna guide:** Här slipar du **målsvar** du ska kunna säga högt / skriva i README. Tar du paketet från noll — läs klart, gör sen [03 — Övningar](./03-ovningar.md) och [04 — AI-träning](./04-ai-traning.md). Se också [mappens README](./README.md).

Vi börjar med **vad som går sönder** när du upprepar samma färg på varenda barn — och när sidan saknar en tydlig topp. Sedan bygger vi upp arv och Hero. Det är inte magi. Det är en metod.

Ingen Flexbox, ingen Grid, ingen nav-meny här. Bara arv, typografi, bakgrund, spacing — och en pekbar toppsektion.

---

## Problemet först — fem ställen att jaga

Många tänker nu: "Jag sätter `color` på varje rubrik och varje stycke. Då har jag kontroll." Andas.

**Dåligt läge:** Du vill att *all* text i toppen ska vara mörkgrå. Du skriver samma rad tre, fyra, fem gånger.

```css
.hero h1 { color: #222; }
.hero p { color: #222; }
.hero .datum { color: #222; }
.hero .plats { color: #222; }
```

Det *fungerar* — tills någon byter tema. Då jagar du fem ställen och missar det sjätte. Det är behovet **arv** löser: ett ställe att styra "klädseln", så barnen följer med.

Andra problemet, samtidigt: sidan *har* en `h1` och lite text högst upp, men det går inte att peka: "här är välkomstaffischen". Exam 1 kräver en **Hero** du kan peka ut — namn, bild, datum, plats, kort intro — inte "lite innehåll som råkade hamna först".

Två jobb i det här paketet:

1. **Arv** — vissa egenskaper rinner från förälder till barn.
2. **Hero** — en semantisk, stylad toppsektion med rätt innehåll.

---

## Arv — dresscode på kontoret

**Metafor:** Tänk en **kontorspolicy / dresscode**. Kontoret säger: "Vi kör marin text och det här typsnittet." Alla på våningen följer det — *om* de inte har ett eget undantag (en egen `color`). Du målar inte om varje persons tröja för hand. Du sätter policyn en gång.

Samma sak, annan bild om dresscode känns luddigt: en **recept-bas**. Basen (olja, salt, `font-family`) går in i rätterna. En rätt kan överskrida ("den här såsen ska vara röd"). Du skriver inte om basen i varje rätt.

**Vad det är:** Arv = vissa CSS-egenskaper på en **förälder** (t.ex. `body` eller en Hero-`header`) förs vidare till **barnen** om barnen inte sätter egna värden. Klassiskt: `color`, `font-family`, ofta `font-size` / typografi.
**Varför det finns:** Så du slipper upprepa samma röst på varje barn. Ett ställe att styra, många barn som följer.
**Om det saknas / vad det INTE är:** Allt CSS ärvs *inte*. `margin`, `padding`, `border` och `background` ärvs inte på samma sätt. Dresscoden färgar inte om kontorets väggar. Väggfärg (`background`) och avstånd mellan skrivbord (`margin`/`padding`) sätter du på *lådan*, inte via arv. Arv ≠ "hela Box Model kopieras till barnen".

```css
body {
  font-family: system-ui, sans-serif;
  color: #222;
}

.hero {
  background: #f4f1ea; /* INTE ärvt av barnen — sitter på affischen */
  padding: 2rem;       /* luft i affischen — Box Model, inte arv */
  color: #1a1a1a;      /* ÄRVS av texten inuti, om den inte har egen color */
}
```

I HTML: `h1` och `p` *inne i* `.hero` får `#1a1a1a` utan att du skriver `color` på dem. Det är exemplet du ska kunna peka på i README.

Sätter barnet egen färg vinner barnet:

```css
.hero p {
  color: #555; /* undantag från dresscoden — den här rätten får egen sås */
}
```

**Målsvar (säg högt / skriv i README):**
*"Arv betyder att vissa CSS-egenskaper (t.ex. `color`, `font-family`) på en förälder förs vidare till barnen om barnen inte sätter egna värden. Exempel: `color` på `body` eller Hero-föräldern syns på texten inuti."*

---

## Metod — hitta arv i koden (när README-frågan kommer)

Det är inte magi. Tre steg:

1. **Hitta en förälder** med t.ex. `color` eller `font-family`.
2. **Hitta barn** *utan* egen samma egenskap.
3. **Det som syns hos barnet** kommer via arv — skriv ner *din* regel + *ditt* barn. Det är README-fråga 2. Inte en Wikipedia-mening.

**Vad metoden är:** Ett sätt att *peka* i egen CSS, inte att citera definitionen.
**Varför den finns:** Exam 1 frågar efter exempel från *er* kod.
**Om den saknas:** Du har "arv är när barn ärver" utan selektor, utan barn, utan egenskap.

**Målsvar (säg högt / skriv i README) — metod:**
*"Hitta en förälder med t.ex. `color`. Hitta barn utan egen `color`. Det som syns hos barnet är arvet — det exemplet skriver jag i README."*

---

## Hero — löpsedeln högst upp på anslagstavlan

Många tänker: "Hero… är det en superhjälte?" Andas. Det är ett branschord för **toppsektionen**.

**Metafor:** Tänk en **löpsedel / affisch** högst upp på en anslagstavla. Affischen ska gå att peka på som *ett papper*: vad som händer, en bild, när, var, och två meningar så du vet om du ska stanna. Resten av tavlan (schema, smålappar) är *inte* affischen.

**Vad det är:** Hero = välkomnande topp. På Exam 1: **eventnamn**, **bild/logotyp**, **datum**, **plats**, **kort beskrivning**. I HTML: semantisk `header` eller `section` (gärna med en class så du kan styla just den lådan).
**Varför det finns:** Besökaren ska på en sekund förstå *vad, när, var*. Examinationen ska kunna peka: "där är Hero."
**Om det saknas / vad det INTE är:** Hero är INTE hela sidan. Inte schema. Inte en rad aktivitetskort. Inte `<head>` (det är dokumentets meta — osynligt). En naken `h1` högst upp utan sektion räcker inte som affisch: den saknar bild, datum, plats och en *avgränsad* yta att styla.

```html
<header class="hero">
  <img src="https://placehold.co/280x120" alt="Logotyp Källarloppis" width="280" height="120" />
  <h1>Källarloppis på Ringvägen</h1>
  <p>Lördag 12 september · Ringvägen 14</p>
  <p>Möbler, porslin och cyklar. Fika i trappan. Inget föranmälan.</p>
</header>
```

Fem bitar. En förälder. Sedan CSS: typografi och `color` på föräldern (arv), `background` och `padding` på affischen (lådan).

**Målsvar (säg högt / skriv i README):**
*"Hero är den välkomnande toppsektionen — namn, bild/logotyp, datum, plats och kort intro. Den ska gå att peka ut i HTML (t.ex. `header`/`section`) och vara stylad med typografi, bakgrund och spacing."*

---

## Semantik för toppen — vad ÄR det här pappret?

Metod du redan kan: fråga vad innehållet *betyder*, sen välj tagg.

| Fråga | Tagg | INTE |
|--------|------|------|
| Sidans välkomst / sidhuvud | `header` (eller `section` om du hellre tänker "en sektion") | En hög `div` "för att det syns ändå" |
| Namnet på evenemanget / stället | `h1` (en per sida) | Extra `h1` längre ner "för stor text" |
| Bild som *betyder* något | `img` med `alt` | Tom dekor utan alternativtext |
| Datum och plats | `p` (eller `p` + `span` om du vill styla en del) | Gömma i CSS-content |

Class på Hero (`class="hero"`) är till för CSS: *den här* affischen. Classen ersätter inte semantik.

---

## Styla affischen — tre rattar, inte en

Typografi och färg kan ärvas. **Bakgrund och spacing sitter på affischen.**

```css
.hero {
  font-family: Georgia, serif;
  color: #1a1a1a;
  background: #f4f1ea;
  padding: 2rem;
  margin-bottom: 2rem;
}

.hero img {
  display: block;
  margin-bottom: 1rem;
}
```

- **Typografi / `color`:** dresscode — barnen följer.
- **`background`:** papprets färg. Barnen blir inte beige inuti bokstäverna.
- **`padding` / `margin`:** luft *i* affischen vs avstånd *till nästa* block. Matlådan från CSS-paketet. Inte arv.

Ingen `display: flex` och inget Grid här. Affischen ska vara tydlig, inte ett kortgalleri.

---

## Vanliga missar

| Miss | Rättare tanke |
|------|----------------|
| `color` på varje barn "för kontroll" | Sätt på föräldern. Undantag bara där det behövs |
| "Allt CSS ärvs" | Typografi/färg ofta. Inte padding/background/border på samma sätt |
| Hero = hela `body` | Toppsektion. Resten av sidan kommer senare |
| `<head>` istället för `<header>` | `head` = meta. `header` = synligt sidhuvud |
| Bara en `h1`, ingen bild/datum/plats | Exam-listan: fem bitar, inte en rubrik |
| Flex/Grid "så Hero blir snygg" | Inte det här paketet. Typografi, bakgrund, spacing räcker |
| README-fråga 2 utan pekning | Förälder + egenskap + barn utan egen regel |

---

## Checkpoint (privat)

Skriv i Docs/anteckningar — för dig:

1. Vad betyder arv i CSS? (sikta på målsvaret)
2. Nämn två egenskaper som ofta ärvs — och en som du *inte* räknar som arv på samma sätt
3. Vad måste en Hero innehålla?
4. Metodens tre steg för att hitta ett README-exempel

När du kan säga svaren högt utan att titta: gå vidare.

---

## Nästa steg

Gå till [02 — Visuellt](./02-visuell.md), sedan övningarna.
