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

## Lisens

MIT © Yosmel Chiang
