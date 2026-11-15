---
name: rolig-design
description: "Fjern typiske AI- og mal-trekk ('vibe-code') fra nettsider og apper. Bruk ved design, CSS-oppsett og visuell gjennomgang for å gi grensesnittet matte flater, varme fargetoner og redaksjonell typografi."
---

# rolig-design

Når kodeverktøy og språkmodeller genererer CSS og komponenter uten stram styring, havner de nesten alltid på de samme visuelle standardvalgene: flerfargede bakgrunnsgløder, kald blågrå mørkmodus, tykke avrundede kort som spretter ved hover, og fete overskrifter overalt. Denne ferdigheten erstatter disse standardvalgene med et rolig, redaksjonelt uttrykk.

## 1. Matte flater fremfor flerfargede bakgrunnsgløder

Det tydeligste visuelle tegnet på en AI-generert side er to eller tre store `radial-gradient`-flekker (ofte i lilla, lyseblå, rosa eller oransje) lagt oppå bakgrunnen i `body` eller rundt kort.

- **Regel:** Bakgrunnen på siden (`body`) og i seksjoner skal være en ren, matt flate uten flerfargede `radial-gradient`-gløder.
- **Bildebakgrunner:** Forhåndsvisningsbilder og prosjektkort skal ligge på en ensfarget, matt bakgrunn (for eksempel `#1d1a18`), uten innebygde neonrammer eller fargede lysflekker i hjørnene.

## 2. Varme kull- og sandtoner fremfor kald tech-blågrå

Standard mørkmodus i mange maler bruker kald, blålig grå (`#0d0e10`, `#15171a`, `#64748b`). Når det blandes med varme aksentfarger, ser grensesnittet oppstykket ut.

- **Lys modus:** Bruk varm, matt papir- eller linfarge som grunnflate (`#f7f4ee`), ren hvit på løftede flater (`#ffffff`), varm sand på sekundære flater (`#ede8df`) og dyp varm sort på tekst (`#161312`).
- **Mørk modus:** Bruk varm kull og espresso (`#141211` som bakgrunn, `#1d1a18` og `#262220` på kort) med varm dempet grå på sekundærtekst (`#a39c95`).
- **Stram aksentbruk:** Hold deg til en gjennomført aksentfarge (for eksempel varm terrakotta `#e05633` / `#ed6e48`) på tvers av hele siden, fremfor å gi hvert kort sin egen neonfarge.

## 3. Redaksjonell typografi: La størrelsen gjøre jobben

Når alle overskrifter (`h1`, `h2`, `h3`) står i `font-semibold` (`600`) eller `font-bold` (`700`), ser siden ut som en generisk mal.

- **Store overskrifter (`h1` og `h2`):** Bruk vanlig vekt (`font-normal` / `400`) med litt strammere negativ bokstavavstand (`letter-spacing: -0.025em` til `-0.03em`). Når vekten er `400`, gir selve størrelsen et rolig og gjennomarbeidet uttrykk.
- **Korttitler og underoverskrifter (`h3`):** Bruk `font-medium` (`500`) med `-0.015em` bokstavavstand.
- **Lesero:** Ikke legg inn unødvendige intro-avsnitt eller forklaringsbokser mellom overskrifter og innhold når selve kortene eller oversikten taler for seg selv.

## 4. Strammere kort og rolig bevegelse

Unngå kombinasjonen av store boblehjørner (`24px`+), tunge skygger, kort som hopper opp ved hover (`translateY(-3px)`) og bilder som zoomer inn (`scale(1.02)`).

- **Hjørner og kanter:** Bruk strammere avrunding (`12px` til `16px`) med en tynn, diskret kantlinje (`1px solid var(--line)`) og lav skygge.
- **Rolig hover:** La bildene ligge helt i ro. Marker heller hover ved å gjøre kantlinjen et hakk tydeligere (`border-color: var(--line-strong)`).
- **Skille mellom forslag og fritekst i skjema/chat:** Hold tekstfelt rene med en fast, åpen plassholdertekst (som `"Skriv ditt eget spørsmål…"`). Ikke la ferdige spørsmål rulle inne i selve skrivefeltet.
