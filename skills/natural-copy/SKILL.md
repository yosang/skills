---
name: natural-copy
description: "Write direct, natural human copy in English and Norwegian (Bokmål) without LLM clichés, em dashes, or stiff literal translations. Use whenever drafting or editing UI text, READMEs, commit messages, voice/chat prompts, portfolio intros, or job applications."
---

# natural-copy

Language models default to predictable punctuation, throat-clearing transitions, and marketing superlatives. When writing in Norwegian (`nb`), English-trained models also invent awkward word-for-word compound translations. This skill enforces direct, natural copy across English and Norwegian.

## 1. Universal Prose Rules (English & Norwegian)

- **Zero em dashes:** Never use em dashes (`—`), en dashes as sentence separators (`–`), or double hyphens (`--`). Use commas, periods, colons, or parentheses instead.
- **State what something is:** Avoid negative parallelisms such as *"It's not about X, it's about Y"* or *"less about X and more about Y"*. Say directly what the product or code does.
- **Cut openers and summaries:** Skip conversational filler (*"Great question!"*, *"Let's dive in"*) and dutiful closing summaries. Stop as soon as the last concrete point lands.
- **Drop empty buzzwords:** Avoid *seamless*, *robust*, *cutting-edge*, *tailored*, *holistic*, *empower*, *delve*, *tapestry*, and their Norwegian equivalents (*sømløs*, *robust*, *banebrytende*, *skreddersydd*, *helhetlig*, *spennende reise*).
- **Straight quotes:** Use standard straight quotes (`"` and `'`).

## 2. Natural Norwegian (`nb`) for Developers & Voice/TTS

When writing Norwegian UI copy, documentation, or spoken TTS persona notes, write the way a Norwegian developer actually talks over coffee:

### Never invent literal translations of English tech terms

| Avoid (stiff or invented literal translation) | Use instead (natural Norwegian or standard term) |
| :--- | :--- |
| *enkeltkilde-sannhet* | *en felles kilde*, *samlet på ett sted* |
| *myk sletting* | *soft delete* |
| *kanttilfeller* | *edge cases*, *uvanlige tilfeller* |
| *tilstandshåndtering* | *state* |
| *skjermflate* | *side*, *visning*, *UI* |
| *fjernarbeid* | *remote* |
| *tosidig bekreftelse* | *begge bekrefter resultatet* |
| *ryggmargsrettferdig* | *rettferdig*, *uten juks* |
| *kjernen i oppsettet* | *tanken bak*, *slik det fungerer* |

### Retain standard English engineering terms used in Norway

- Keep established terms untouched: `frontend`, `backend`, `fullstack`, `remote`, `hybrid`, `state`, `loading og error states`, `soft delete`, `edge cases`, `middleware`, `cookie`, `refresh token`, `deploy`, `repo`, `stack`, `UI`, `assets`, `accessibility`, `REST API`.
- Avoid unnecessary hyphens in Norwegian compounds: write `frontendutvikling`, `backendutvikling`, `fullstackutvikler`, `programvareutvikling`, `QR kode`, `3D figur`, `AI versjon`.
- Use `programvareutvikling` or `utvikling` (never `koding`), and write `ide` and `en` without acute accents (`é`).
- **Source notes for TTS/chat models:** Write background notes in the exact everyday phrasing you want spoken aloud. If prompt notes contain dense English or stiff nouns, fast models will invent awkward translations mid-sentence.

## 3. Personal, Portfolio & Application Copy

When writing job applications, project intros, or bio text, models default to keyword-stuffing and mirroring the prompt. Follow these rules instead:

- **Motivation before tech stack:** Introduce a project with the human reason it exists (*"Started as an attempt to make something fun for students during recess"*), then add only the 2 to 3 technical details that prove how it works. Do not dump a checklist of frameworks, metrics, and edge cases in one paragraph.
- **Never parrot the job posting:** Do not repeat the employer's exact phrases (*"a small team of 12"*, *"automate voucher entry"*) back to them. Address their core needs in your own everyday words.
- **Group by real-world context:** Label projects by what role they play in real life (*AI in practice*, *Hobby project*, *Commercial*), and do not cram multiple unrelated projects into a single bullet point just to check off more keywords.
- **Peer-to-peer closing:** End applications at eye level by offering to walk through codebases and hear what they look for in a developer, rather than pleading for an interview.
