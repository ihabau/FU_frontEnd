# 03 — Övningar

**Omfång det här paketet:** `display: flex`, `justify-content`, `align-items`, `gap`, `flex-wrap`. Tre–fyra kort med bild + kort text i **en** riktning. Konkret feedback (tagg eller egenskap — inte "ser bra ut"). Ingen Grid. Ingen nav. Ingen media query. Hero från förra paketet får ligga kvar om du bygger i samma mapp — rör den inte med Flex om du inte måste.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje flex-rad du behåller.

Tema här: **lunchbrickor** och **träningspass** — inte event-kort. Samma form som Exam 1-Highlights (bild + text, liknande bitar i rad).

---

## Uppgift 1 — Traven i matsalen

**Mål:** Se stapeln. Slå på hyllan. Styra luft med `gap`.

**Problem först:** Tre lunchkort som block. De *finns*, men de är en hög. Det är läget du ska ta dig ur.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Matsalen Loftet</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <section class="meny">
    <h2>Veckan på Loftet</h2>
    <div class="kort-rad">
      <article class="kort">
        <img src="https://placehold.co/200x120" alt="Ärtsoppa i bunke" width="200" height="120" />
        <h3>Ärtsoppa</h3>
        <p>Torsdag. Pannkaka till.</p>
      </article>
      <article class="kort">
        <img src="https://placehold.co/200x120" alt="Fiskgratäng" width="200" height="120" />
        <h3>Fiskgratäng</h3>
        <p>Onsdag. Sallad ingår.</p>
      </article>
      <article class="kort">
        <img src="https://placehold.co/200x120" alt="Vegetarisk pasta" width="200" height="120" />
        <h3>Pasta pesto</h3>
        <p>Fredag. Nötter i såsen.</p>
      </article>
    </div>
  </section>
</body>
</html>
```

**Krav:**
1. Mapp `ovning-matsal` → `index.html` (ovan) + `style.css`.
2. Först: **ingen** Flex. Ladda. Säg högt vad som är fel mot "en hylla".
3. På `.kort-rad`: `display: flex`, `gap`, och minst en av `justify-content` / `align-items`.
4. `flex-wrap: wrap` så korten får byta rad om fönstret är smalt.
5. Lätt Box Model på `.kort` (t.ex. padding + border) — `gap` sköter mellanrummet, inte `margin` på alla barn.
6. Ingen Grid.

**Klart-check (peka i DIN kod):**
- [ ] Peka: vilken selector är *hyllan* — och *varför* inte `.kort`
- [ ] Peka `gap` och säg vad som hade hänt utan den
- [ ] Peka `flex-wrap` och säg *varför*
- [ ] Ingen Grid, inga floats

**Ägarskap:** AI ok som bollplank — spara prompt + en mening om vad du ändrade. Du ska kunna förklara varje flex-egenskap.

---

## Uppgift 2 — Passkort + feedback på "en kompis kod"

**Mål:** Bygga tre–fyra likadana kort till. Öva **konkret** feedback på någon annans (här: given) kod.

**Scenario:** Gymmet Loftet vill visa dagens pass: bild + namn + en mening. Samma form som Highlights — men det är **träningspass**, inte artister.

**Del A — bygg:**
1. Mapp `ovning-pass` (eller ny sektion i matsal-mappen). `section` + behållare + **minst tre** `article.kort` (bild, `h3`, `p`).
2. Flex på behållaren: `display: flex`, `gap`, `flex-wrap`. Välj `justify-content` medvetet (inte bara för att AI la dit `center`).
3. I anteckningar: en mening varför Flex passar *här* (liknande bitar, en riktning).

**Del B — feedback på den här snutten** (hitta på att det är en klasskamrat):

```html
<section>
  <div style="display: flex;">
    <div class="card">Yoga</div>
    <div class="card">Spinning</div>
    <div class="card">Cirkelfys</div>
  </div>
</section>
```

```css
.card {
  margin: 20px;
}
```

Skriv **minst tre** rader:
`FEEDBACK: [vad jag ser] → [vad som måste ändras]`
Krav: peka på **tagg eller egenskap**. Förbjudet som enda kommentar: "ser bra ut", "snyggt", "nice".

**Klart-check (peka i DIN kod + dina rader):**
- [ ] Tre–fyra passkort i en riktning med `gap`
- [ ] Meningen "varför Flex" är din, inte copy-paste
- [ ] Tre FEEDBACK-rader utan tomt beröm
- [ ] Minst en rad om saknad `gap` *eller* `div` vs `article` *eller* inline `style`

**Ägarskap:** Om AI skriver feedbacken åt dig: skriv om så *du* kan stå för varje pil.

---

## Uppgift 3 — Stretch (valfritt)

Samma kort, men **kolumn** (`flex-direction: column`) i en variant — t.ex. en class `.kort-rad--kolumn`. Två skärmdumpar i huvudet: rad vs kolumn. En mening: fortfarande en dimension, bara andra hållet.

**Klart-check:** Peka `flex-direction` och säg varför det *inte* plötsligt är Grid.

---

## När du kört fast

1. Sitter `display: flex` på behållaren runt korten?
2. Kör de tre frågorna: liknande bitar? en riktning? (annars Grid i 06 — inte här)
3. Feedback: tvinga meningen att innehålla ett CSS-ord eller en tagg.
4. Jämför med [01-teoriguide](./01-teoriguide.md).
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
