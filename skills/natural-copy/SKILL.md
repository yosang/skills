---
name: natural-copy
description: "Write direct, natural human copy in English and Norwegian (Bokmål) without LLM clichés, em dashes, or stiff literal translations. Use whenever drafting or editing UI text, READMEs, commit messages, voice/chat prompts, portfolio intros, or job applications."
---

# natural-copy

Language models default to predictable punctuation, throat-clearing transitions, and marketing superlatives. When writing in Norwegian (`nb`), English-trained models also invent awkward word-for-word compound translations. This skill enforces direct, natural copy across English and Norwegian.

## 1. Universal Prose Rules (English & Norwegian)

- **Zero em dashes and no colons in sentences or headings:** Never use em dashes (`—`), en dashes as sentence separators (`–`), double hyphens (`--`), or colons (`:`) in the middle of a running sentence to join clauses (avoid *"Den erfaringen gjør at jeg trives når jeg får bidra med mer enn bare kode: engasjere meg i møte med kunden..."*). Never use colon-split headings (`Label: Subtitle` such as *"Utenfor skjermen: Fjell, telt og hunden"*, *"Målgruppe og innsikt: Hvem vi bygger for"*, or *"Uke 1: Normalisering"*); drop the prefix and write the direct heading (*"Fjell, telt og hunden"*). In running sentences, use commas, natural connecting words (*som å*, *både*, *fra ... til*, *der*, *men*, *such as*, *from ... to*), parentheses, or split into two sentences with a period.
- **Drop compound modifier hyphens:** Avoid hyphenating compound modifiers or tech terms in English and Norwegian (`full-stack`, `cross-clinic`, `real-time`, `AI-assisted`, `role-based`, `in-memory`, `server-side`, `speech-to-text`, `built-in`, `stress-tested`, `two-year`). Write single words or space-separated words instead (`fullstack`, `across clinics`, `real time`, `AI assisted`, `role based`, `in memory`, `server side`, `speech to text`, `built in`, `stress tested`, `two year`).
- **State what something is:** Avoid negative parallelisms such as *"It's not about X, it's about Y"* or *"less about X and more about Y"*. Say directly what the product or code does.
- **Cut openers and summaries:** Skip conversational filler (*"Great question!"*, *"Let's dive in"*) and dutiful closing summaries. Stop as soon as the last concrete point lands.
- **Drop empty buzzwords & stiff essay verbs:** Avoid *seamless*, *robust*, *cutting-edge*, *tailored*, *holistic*, *empower*, *thrive*, *delve*, *tapestry*, *showcase*, *demonstrate*, *accumulate*, *arose*, *endeavor*, *facilitate*, *utilize*, *consolidate*, *eliminate*, *cumbersome*, *purged*, *subsequently*, *following a bout of*, *targeted by trickery*, and their Norwegian equivalents (*sømløs*, *robust*, *banebrytende*, *skreddersydd*, *helhetlig*, *spennende reise*, *faktaforankring*, *strengt forankret*, *målrettede tiltak*). Use everyday spoken verbs (*like*, *enjoy*, *show*, *walk through*, *save/collect*, *came up*, *use*, *gather*, *clean up*, *heavy*, *cleared*, *after*).
- **Translate idioms by meaning, never word for word:** When translating between Norwegian and English, never calque idioms literally (translate *"utdannet meg"* as *"studied"*, never *"trained"*; translate *"trives"* as *"like"* or *"enjoy"*, never *"thrive"*; translate *"står og faller på"* as *"depends on"*, never *"stands and falls on"*; translate *"muntlig trening"* as *"speaking practice"*, never *"oral practice"*; keep *"AI version of me"*, never *"AI twin"*).
- **Straight quotes:** Use standard straight quotes (`"` and `'`).
- **No dangling plural apostrophes:** Avoid trailing apostrophes after plural words (`students'`, `users'`, `players'`) that look like stray marks in UI copy. Rephrase naturally (*"among students"*, *"for users"*, *"player points"*).

## 2. Natural Norwegian (`nb`) for Developers & Voice/TTS

When writing Norwegian UI copy, documentation, or spoken TTS persona notes, write the way a Norwegian developer actually talks over coffee:

### Never invent literal translations or bureaucratic terms

| Avoid (stiff, textbook, or bureaucratic) | Use instead (natural Norwegian or standard term) |
| :--- | :--- |
| *enkeltkilde-sannhet* | *en felles kilde*, *samlet på ett sted* |
| *myk sletting* | *soft delete* |
| *kanttilfeller* | *edge cases*, *uvanlige tilfeller* |
| *tilstandshåndtering* | *state* |
| *tilgjengelighet* | *accessibility* |
| *unike skranker* | *unike indekser*, *unique constraints* |
| *arbeidsminnet* | *minnet* |
| *informasjonskapsler* / *sporingscookies* | *cookies*, *cookies for sporing* |
| *stemmesyntese* / *syntetisk stemme* | *klonet stemme*, *stemme* |
| *skjermflate* / *applikasjonen* / *publikumssidene* | *side*, *visning*, *UI*, *løsningen*, *nettsiden*, *de åpne sidene* |
| *fjernarbeid* | *remote* |
| *faktaforankring* / *strengt forankret* | *holder seg til godkjente fakta*, *kun godkjente fakta* |
| *merkantil* / *merkantile* | *forretning*, *forretningsvirksomhet* |
| *målrettede tiltak* | *konkrete grep*, *endringer* |
| *medbygger* | *medgründer*, *driver sammen med* |
| *tosidig bekreftelse* | *begge bekrefter resultatet* |
| *ryggmargsrettferdig* | *rettferdig*, *uten juks* |
| *kjernen i oppsettet* | *tanken bak*, *slik det fungerer* |

### Retain standard English engineering terms and drop hyphen clutter

- Keep established terms untouched: `frontend`, `backend`, `fullstack`, `remote`, `hybrid`, `state`, `loading og error states`, `soft delete`, `edge cases`, `middleware`, `cookie`, `refresh token`, `deploy`, `repo`, `stack`, `UI`, `assets`, `accessibility`, `REST API`.
- **No suspended hyphens:** Never write list compounds like *turnerings-, bord- og aktivitetsplattform*, *loading- og error-states*, or *minutt- og dagskvoter*. Rephrase into normal spoken words (*et system for turneringer og poengtavle*, *loading og error states*, *kvoter per minutt og per dag*).
- **No hyphens between tech terms/abbreviations and Norwegian words:** Write single words or space-separated phrases (`frontendutvikling`, `backendutvikling`, `fullstackutvikler`, `programvareutvikling`, `QR kode`, `3D modell`, `3D skannet`, `AI versjon`, `AI assistert`, `WAL modus`, `ES5 støtte`, `Docker container`, `SQLite database`, `backend løsninger`).
- **Never glue Norwegian suffixes onto code identifiers with a hyphen:** Avoid `.Include()-kall`, `node:sqlite-modulen`, `<video>-tag`, or `SKILL.md-moduler`. Write *kall til `.Include()`*, *innebygd `node:sqlite`*, *`<video>`*, and *`SKILL.md` filer*.
- Use `programvareutvikling` or `utvikling` (never `koding`), prefer plain `regler` or `rammer` over stiff `kjøreregler`, and write `ide` and `en` without acute accents (`é`).
- **Source notes for TTS/chat models:** Write background notes in the exact everyday phrasing you want spoken aloud. If prompt notes contain dense English or stiff nouns, fast models will invent awkward translations mid-sentence.

## 3. Personal, Portfolio & Application Copy

When writing job applications, project intros, or bio text, models default to keyword-stuffing and mirroring the prompt. Follow these rules instead:

- **Motivation before tech stack:** Introduce a project with the human reason it exists (*"Started as an attempt to make something fun for students during recess"*), then add only the 2 to 3 technical details that prove how it works. Do not dump a checklist of frameworks, metrics, and edge cases in one paragraph.
- **Never parrot the job posting:** Do not repeat the employer's exact phrases (*"a small team of 12"*, *"automate voucher entry"*) back to them. Address their core needs in your own everyday words.
- **Group by real-world context:** Label projects by what role they play in real life (*AI in practice*, *Hobby project*, *Commercial*), and do not cram multiple unrelated projects into a single bullet point just to check off more keywords.
- **Peer-to-peer closing:** End applications at eye level by offering to walk through codebases and hear what they look for in a developer, rather than pleading for an interview.
