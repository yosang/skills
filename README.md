# yosmel-skills

Norske ferdigheter (`SKILL.md`) og kjøreregler for AI-assistert programvareutvikling. Laget for å løse tre konkrete utfordringer når språkmodeller skriver norsk tekst, bygger grensesnitt og endrer kode:

1. **[`norsk-tone`](./skills/norsk-tone/SKILL.md):** Får språkmodeller til å skrive naturlig, muntlig norsk bokmål uten stive direkteoversettelser fra engelsk, oppkonstruerte sammensatte ord, tankestreker eller klisjeer.
2. **[`rolig-design`](./skills/rolig-design/SKILL.md):** Fjerner typiske AI-trekk fra webgrensesnitt (flerfargede bakgrunnsgløder, kald blågrå mørkmodus, fete overskrifter overalt og hoppende kort) til fordel for matte flater, varme kulltoner og redaksjonell typografi.
3. **[`slank-kode`](./skills/slank-kode/SKILL.md):** Holder kodebasen og konteksten slank gjennom planlegging før kode, en enkelt sannhetskilde for data, aktiv sletting av unødvendige lag og tester som sjekker reell oppførsel.

## Struktur

```text
yosmel-skills/
├── AGENTS.md
├── LICENSE
├── README.md
└── skills/
    ├── norsk-tone/
    │   └── SKILL.md
    ├── rolig-design/
    │   └── SKILL.md
    └── slank-kode/
        └── SKILL.md
```

## Bruk i prosjekter

Du kan enten legge mappen `skills/` inn i `.agents/skills/` (støttes av verktøy som følger Agent Skills-standarden, som Claude Code, Cursor, Antigravity og Gemini CLI), eller kopiere [`AGENTS.md`](./AGENTS.md) rett inn i roten av prosjektet ditt.

## Videreutvikling og nye ferdigheter

Dette repoet er bygget for å vokse i takt med nye erfaringer i prosjekter. Både jeg og andre utviklere kan utvide eksisterende ferdigheter eller legge til nye.

### 1. Utvide en eksisterende ferdighet

Når en språkmodell gjentar en ny uvane i et prosjekt, legg til et konkret punkt i den ferdigheten det gjelder:

- **Nytt kunstig norsk ord eller stiv oversettelse:** Legg ordet og det naturlige alternativet inn i tabellen i [`skills/norsk-tone/SKILL.md`](./skills/norsk-tone/SKILL.md).
- **Nytt visuelt mal-trekk i CSS eller UI:** Beskriv mønsteret som skal unngås og hvilken konkret verdi som skal brukes i stedet i [`skills/rolig-design/SKILL.md`](./skills/rolig-design/SKILL.md).
- **Ny kodeuvane eller arkitekturregel:** Legg inn regelen med et kort praktisk eksempel i [`skills/slank-kode/SKILL.md`](./skills/slank-kode/SKILL.md).

### 2. Legge til en ny ferdighet fra bunnen av

Hver ferdighet bor i sin egen mappe under `skills/<navn>/SKILL.md` og følger dette oppsettet:

```markdown
---
name: <kort-navn-med-bindestrek>
description: "Kort beskrivelse av hva ferdigheten gjør og når modellen skal bruke den."
---

# <kort-navn-med-bindestrek>

Kort forklaring (2 til 3 setninger) på hvilket konkret problem ferdigheten løser.

## 1. <Første hovedregel>

- Konkret instruks med eksempel på hva som skal unngås og hva som skal gjøres i stedet.
```

### 3. Prinsipper for bidrag

For at ferdighetene skal være raske for en språkmodell å lese uten å spise opp kontekstvinduet:

1. **Kun regler som endrer atferd:** Ikke legg inn generelle lærebokråd som modellen allerede kan fra før. Hver regel skal rette opp en konkret feil modellen faktisk gjør uten styring.
2. **Konkrete eksempler fremfor vage adjektiver:** Vis heller *"Unngå X, skriv Y"* eller eksakte verdier (`font-weight: 400`, `#141211`) enn å be modellen om å *"skrive godt"* eller *"lage et fint design"*.
3. **Hold filene korte:** En `SKILL.md` bør være under 100 linjer. Hvis en ferdighet trenger lengre oppslagsverk eller hjelpescript, legg dem i undermapper (`references/` eller `scripts/`) inne i ferdighetens mappe.
4. **Følg reglene selv:** Alle tekster i dette repoet skal følge [`norsk-tone`](./skills/norsk-tone/SKILL.md) (naturlig norsk bokmål og null tankestrek).

Når en ny ferdighet er lagt til under `skills/`, legg også inn en kort linje om den i [`AGENTS.md`](./AGENTS.md) og i oversikten øverst i denne filen.

## Lisens

MIT © Yosmel Chiang
