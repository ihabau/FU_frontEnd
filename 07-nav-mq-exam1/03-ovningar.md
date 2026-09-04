# 03 — Övningar

**Omfång det här paketet:** `nav` med ankare (`#hero` `#schema` `#highlights`), matchande `id`, `footer` med kontakt + fiktiva sponsorer, minst en `@media`, testa viewport. Exam-checklistan i elevspråk. Ingen JavaScript-meny. Grid-rattarna för schemat övar du i [06-css-grid](../06-css-grid/) — här ska sektionen *finnas* och gå att hoppa till.

AI får hjälpa dig skriva. Du måste kunna **peka och förklara** varje länk, id och query du behåller.

---

## Uppgift 1 — Döda knappar på bakluckeloppis

**Mål:** Förstå problemet när menyn inte landar. Koppla hissknapp till skylt. Sätt sidfot enligt Exam.

**Problem först:** Sidan har sektioner. En "meny" med länkar som **inte** matchar några `id` — eller saknar `#`. Klick gör ingenting användbart. Det är läget du ska ta dig ur.

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8" />
  <title>Bakluckeloppis Hamnen</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav>
    <a href="hero">Hem</a>
    <a href="schema">Tider</a>
    <a href="highlights">Fynd</a>
  </nav>
  <header>
    <h1>Bakluckeloppis Hamnen</h1>
    <p>Lördag 10–14 · Kajen</p>
  </header>
  <main>
    <section>
      <h2>Tider</h2>
      <p>Insläpp 10. Uppackning 9.</p>
    </section>
    <section>
      <h2>Fynd</h2>
      <p>Vinyl, verktyg, bakluckor med kaffe.</p>
    </section>
  </main>
</body>
</html>
```

**Krav:**
1. Mapp `ovning-baklucka` → Open Folder → utgångspunkten ovan (eller eget loppmarknadstema).
2. Fixa **först** de döda länkarna: `href="#hero"` osv. + `id` på `header`/`section` som stämmer.
3. `nav` runt länkarna. Gärna Flex på menyn (en rad länkar).
4. `footer` med **kontakt** (påhittad mejl/adress) och **minst två fiktiva sponsorer**.
5. Ingen `onclick`, inga extra HTML-sidor. Samma dokument.

**Klart-check (peka i DIN kod):**
- [ ] Klick på "Tider" scrollar till tider-sektionen
- [ ] Peka på ett `href` och dess `id` — säg *varför* namnen är lika och var `#` sitter
- [ ] Peka i footern: kontakt *och* sponsorer
- [ ] Säg högt: varför `nav` och `footer` inte är samma sak

**Ägarskap:** AI ok som bollplank — spara prompt + en mening om vad du ändrade. Du ska kunna förklara varje ankare.

---

## Uppgift 2 — Simklubben på smal skärm

**Mål:** Se klämd layout. Skriv `@media`. Testa viewport. Koppla till Exam-listan.

Många tänker nu: "Den ser bra ut på min laptop." Just därför: **smalna**.

**Brief:** Enkel sida för **Simklubb Ådran** (eller annat föreningstema). Hero + två sektioner med `id` + nav + footer från uppgift 1-mönstret. På bred vy får menyn vara i rad. På smal vy ska något **faktiskt ändras** (t.ex. meny i kolumn, eller schema-tavlan i en kolumn om du kopplat Grid från 06).

**Krav:**
1. Mapp `ovning-adran` (eller bygg vidare på bakluckan med nytt tema).
2. DevTools: smal viewport **först** — notera vad som kläms (en mening i anteckningar).
3. Minst en `@media (max-width: …)` som förbättrar just det. En ratt, inte tio.
4. Testa igen: smalt *och* brett. Queryn ska gå att peka ut.
5. I anteckningar, checklista mot Exam 1 — kryssa vad *den här* övningssidan har vs vad eventsidan fortfarande saknar (Hero-innehåll, Grid-schema, Flex-kort, nav, footer, MQ, README, grupprepo). Ingen tidsplan — bara innehåll.
6. **Gruppstart (om ni är flera):** skapa eller öppna det **gemensamma** GitHub-repot, fördela sektioner i en kort lista, gör minst en commit där det syns vem som jobbat (namn i meddelandet om samma dator).

**Klart-check (peka i DIN kod):**
- [ ] Peka på `@media` — vad den gör och *varför* du skrev den efter testet
- [ ] Peka: ankarlänk + matchande `id`
- [ ] Anteckningens Exam-check är din, inte copy-paste av hela briefen
- [ ] (Om grupp) repo-URL + minst en synlig commit som går att förklara

**Ägarskap:** Samma regel som uppgift 1. Om AI slänger in hamburger-JS eller `position: fixed` du inte kan försvara — ta bort det.

---

## Uppgift 3 — Stretch (valfritt)

Skriv tre rubriker i gruppens `README.md`: **Semantik**, **Arv**, **Flex vs Grid**. En mening under varje — utkast, egna exempel från sidan. Push.

**Klart-check:** Kan tre personer i gruppen läsa meningarna högt och stå för dem? Om ja: ni har README-frågorna i mini-format.

---

## När du kört fast

1. Död länk: jämför stavning, `#`, versaler.
2. MQ "händer inget": spara, hårdladda, kolla att viewport faktiskt är under `max-width`, kolla klassnamnet i queryn.
3. Schema ser ut som en lista: Grid-rattarna i [06-css-grid](../06-css-grid/).
4. Jämför med [01-teoriguide](./01-teoriguide.md).
5. Gå vidare till [04 — AI-träning](./04-ai-traning.md).
