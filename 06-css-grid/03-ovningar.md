# 03 — Övningar

**Omfång det här paketet:** `display: grid`, `grid-template-columns`, rader som fylls, `gap`. Skillnad Flex vs Grid (Highlights förblir Flex om du har dem). Ingen nav-meny, inga media queries. Semantisk HTML på grundnivå. Ett `id` på tavle-sektionen räcker som adress för senare hopp.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje regel du behåller.

---

## Uppgift 1 — Öppettider i en hög

**Mål:** Se stapeln. Slå på Grid på föräldern. Få en tavla med kolumner.

**Problem först:** Biblioteket har öppettider per dag. Just nu är det **sex lappar under varandra**. Det *finns* information. Det är **ingen** tavla — du ser inte "förmiddag / eftermiddag" som rum bredvid varandra.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Biblioteket Kajen — öppettider</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1>Biblioteket Kajen</h1>
  </header>
  <main>
    <section id="tavla">
      <h2>Öppettider</h2>
      <div class="tavla">
        <article>
          <h3>Tisdag</h3>
          <p>11–18</p>
        </article>
        <article>
          <h3>Onsdag</h3>
          <p>11–18</p>
        </article>
        <article>
          <h3>Torsdag</h3>
          <p>11–20</p>
        </article>
        <article>
          <h3>Fredag</h3>
          <p>11–18</p>
        </article>
        <article>
          <h3>Lördag</h3>
          <p>11–15</p>
        </article>
        <article>
          <h3>Söndag</h3>
          <p>12–16</p>
        </article>
      </div>
    </section>
  </main>
</body>
</html>
```

**Krav:**
1. Mapp `ovning-kajen-tavla` → Open Folder → `index.html` (ovan eller eget bibliotekstema) + `style.css`.
2. Öppna sidan **innan** Grid: bekräfta stapeln.
3. På `.tavla`: `display: grid`, `grid-template-columns` (minst två kolumner, t.ex. `1fr 1fr 1fr`), `gap`.
4. Cellerna får gärna padding/border (Box Model) — men Grid-rattarna sitter på **föräldern**.
5. Ingen `display: flex` på `.tavla`. Ingen `@media`.

**Klart-check (peka i DIN kod):**
- [ ] Sidan visar kolumner, inte bara en hög
- [ ] Peka på `display: grid` — *varför* på föräldern, inte på varje `article`
- [ ] Peka på `grid-template-columns` och säg vad `1fr` gör
- [ ] Säg högt: var sitter raderna (när sex barn och tre kolumner)?
- [ ] `id="tavla"` finns — adress för senare hopp, inte styling

**Ägarskap:** AI ok som bollplank — spara prompt + en mening om vad du ändrade. Du ska kunna förklara varje Grid-rad.

---

## Uppgift 2 — Simhallens banor

**Mål:** Upprepa rutnätet i ett annat tema. Träna Flex vs Grid med egna ord (README-fråga 3).

Många tänker nu: "En gång Grid räcker." Nej. En ny yta med två axlar = samma rattar igen.

**Brief:** Simhallen visar **banor** (kolumner) och **klockslag** (rader). Minst **fyra** celler (t.ex. bana 1–2 × två tider).

**Krav:**
1. Ny mapp `ovning-simhall` eller samma repo med en extra sektion. Semantik: `section` + celler som `article` (eller `div` i grid-föräldern — men sektionen ska vara tematisk).
2. Grid på **behållaren**: kolumnmall + `gap`. Minst fyra poster med tid + bana + kort text (t.ex. "Tekniksim" / "Öppen bana").
3. Om du har Highlights-kort från tidigare: de ska **fortfarande** använda Flex. Byt inte dem till Grid.
4. I anteckningar, tre meningar med *dina* ord: (a) vad Grid är, (b) varför *den här* tavlan är Grid, (c) när du skulle valt Flex istället. Sikta på README-fråga 3.
5. Ändra kolumnmallen en gång (t.ex. tre `1fr` → två `1fr`) och titta: samma verktyg, annan plan.

**Klart-check (peka i DIN kod):**
- [ ] Minst fyra celler i Grid
- [ ] Peka: föräldern vs en cell — *varför* Grid inte sitter på cellen
- [ ] Anteckningarnas tre meningar är dina, inte copy-paste
- [ ] Highlights (om de finns) är fortfarande Flex

**Ägarskap:** Samma regel som uppgift 1. Om AI lägger `grid` på varje bana: ta bort det innan du räknar uppgiften som klar.

---

## Uppgift 3 — Stretch (valfritt)

Lägg till en kort `README.md` i övningsmappen med rubriken **Flex vs Grid**. Två meningar: ett exempel som är Flex (kö / kort), ett som är Grid (bräde / tavla). Commit om du versionshanterar.

**Klart-check:** Kan du läsa meningarna högt utan att skämmas för att de är luddiga? Om ja: du har Exam-fråga 3 i mini-format.

---

## När du kört fast

1. Inspektera föräldern: finns `display: grid` *där*?
2. Finns `grid-template-columns` med mer än en kolumn?
3. Kör metoden högt: kö eller schackbräde?
4. Jämför med [01-teoriguide](./01-teoriguide.md) — ratt-tabellen och målsvaren.
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
