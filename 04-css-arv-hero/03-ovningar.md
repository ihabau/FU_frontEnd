# 03 — Övningar

**Omfång det här paketet:** CSS-ärv (`color` / `font-family` från förälder till barn), Hero som semantisk topp (`header` eller `section`) med namn, bild, datum, plats och kort beskrivning, plus typografi / bakgrund / spacing på den ytan. Ingen Flexbox, Grid eller nav-meny. Box Model och selektorer från CSS-paketet får användas.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje regel du behåller — särskilt *ett* arv-exempel.

---

## Uppgift 1 — Upprepad dresscode (loppis-lapp)

**Mål:** Se problemet när samma `color` sitter på varje barn. Rätta med arv från en förälder.

**Problem först:** Du har den här sidan. Den *har* innehåll. CSS:en upprepar samma röst överallt. Det är läget du ska ta dig ur — först lämna det trasigt så du *ser* jakten, sedan en förälder.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Loppis i garaget</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header class="skylt">
    <h1>Loppis i garaget</h1>
    <p>Söndag 6 september</p>
    <p>Industrigatan 9, bakom ICA</p>
    <p>Cyklar, verktyg och överblivna burkar. Kontant och swish.</p>
  </header>
</body>
</html>
```

**Start-CSS (medvetet svag):**

```css
.skylt h1 { color: #1a1a1a; font-family: Georgia, serif; }
.skylt p { color: #1a1a1a; font-family: Georgia, serif; }
```

**Krav:**
1. Mapp `ovning-loppis` → Open Folder → `index.html` + `style.css` som ovan.
2. Ladda i webbläsaren. Säg högt: *var måste jag ändra om jag vill byta färg på all text?*
3. Skriv om CSS: `color` och `font-family` **en gång** på `.skylt` (eller `body`). Ta bort dubbletterna på barnen.
4. Ge `.skylt` en `background` och `padding` (lådan — inte arv).
5. I anteckningar: en mening "Föräldern är …, barnen är …, ärvd egenskap är …"

**Klart-check (peka i DIN kod):**
- [ ] Peka på *en* `color`-rad på föräldern — och ett barn **utan** egen `color`
- [ ] Säg *varför* du flyttade typografin uppåt
- [ ] Peka: `background`/`padding` sitter på lådan, inte på varje `p`
- [ ] Ingen Flex/Grid

**Ägarskap:** AI ok som bollplank — spara prompt + en mening om vad du ändrade. Du ska kunna förklara arv-raden utan att titta.

---

## Uppgift 2 — Affischen (simhallens öppet hus)

**Mål:** Bygga en Hero du kan peka ut. Fem bitar. Semantik. Styling. Ett arv-exempel redo för README-fråga 2.

**Scenario:** Simhallen Åkanten har öppet hus. Besökaren ska på en sekund få namn, bild, datum, plats och en kort pitch. Inte en festival-sida — en **simhallsaffisch**.

**Krav:**
1. Ny mapp `ovning-akanten` (eller fortsätt i en egen mapp — inte loppisen som enda fil om du vill hålla isär). Semantisk `header` eller `section` med class t.ex. `hero`.
2. Innehåll, alla fem:
   - namn (`h1`)
   - bild/logotyp (`img` + `alt`)
   - datum
   - plats
   - kort beskrivning
3. CSS: typografi + `color` på Hero-föräldern (arv). `background` + `padding` (och gärna `margin`) på affischen. Ingen Flex/Grid.
4. Bild: `https://placehold.co/320x140` eller en egen fil i mappen.
5. Skriv tre meningar i en `README.md` i mappen: (a) vad arv är, (b) *ditt* exempel (selektor + barn), (c) vad Hero är på den här sidan.

**Klart-check (peka i DIN kod):**
- [ ] Peka i HTML: de fem bitarna
- [ ] Peka: `header` eller `section` — *varför* den taggen, inte bara `div`
- [ ] Peka arv: förälder-regel + barn utan egen samma egenskap
- [ ] README-meningarna är *dina* ord
- [ ] Ingen Flex/Grid, ingen nav

**Ägarskap:** Samma regel som uppgift 1. Om AI slänger in `display: flex` — ta bort det innan du räknar uppgiften som klar.

---

## Uppgift 3 — Stretch (valfritt)

Bygg en **andra** affisch i samma anda: bakluckeloppis på en industriparkering. Samma fem bitar. Byt `background`. Öppna Inspect, välj ett `p` inuti Hero, och kolla Computed: var `color` kommer ifrån (föräldern, inte en egen regel).

**Klart-check:** En mening i anteckningar: "Inspect visade att color kommer från … för att …"

---

## När du kört fast

1. Spara + hård-ladda om. `link` till `style.css` i `head`?
2. Kör arv-metoden högt: förälder? barn utan egen regel? syns det?
3. Fem bitar i Hero — räkna dem på skärmen.
4. Jämför med [01-teoriguide](./01-teoriguide.md).
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
