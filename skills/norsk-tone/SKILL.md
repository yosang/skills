---
name: norsk-tone
description: "Sørg for at norsk tekst i brukergrensesnitt, dokumentasjon, chattesvar og systeminstrukser leses som naturlig norsk bokmål skrevet av en norsk utvikler. Bruk alltid når du skriver eller redigerer norsk tekst."
---

# norsk-tone

Språkmodeller er i hovedsak trent på engelsk. Når de skriver norsk uten tydelige rammer, oversetter de engelske uttrykk ord for ord, finner på unaturlige sammensatte ord og strør om seg med tankestreker og reklamespråk. Denne ferdigheten setter faste regler for naturlig norsk bokmål i tekniske prosjekter.

## 1. Ingen oppkonstruerte oversettelser fra engelsk

Det tydeligste tegnet på maskinskrevet norsk er hjemmesnekrede sammensetninger som forsøker å oversette et engelsk uttrykk direkte. Hvis en vanlig norsk utvikler ikke ville sagt ordet høyt over en kaffekopp, skal det ikke brukes.

| Unngå (direkteoversatt / oppkonstruert) | Skriv heller (naturlig norsk eller etablert fagord) |
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

## 2. Behold engelske faguttrykk som faktisk brukes i bransjen

Norske utviklere blander inn faste engelske faguttrykk når de snakker norsk. Ikke tving gjennom stive lærebokoversettelser for ord som allerede er standard på norske arbeidsplasser:

- Behold: `frontend`, `backend`, `fullstack`, `remote`, `hybrid`, `state`, `loading og error states`, `soft delete`, `edge cases`, `middleware`, `cookie`, `refresh token`, `deploy`, `repo`, `stack`, `UI`, `assets`, `accessibility`, `REST API`.
- Skriv sammensetninger uten unødvendig bindestrek: `frontendutvikling`, `backendutvikling`, `fullstackutvikler`, `programvareutvikling`, `QR kode`, `3D figur`, `AI versjon`.
- Bruk `programvareutvikling` eller `utvikling`, aldri `koding`.
- Skriv `ide` og `en` uten akutt aksent (`é`).

## 3. Tegnsetting og setningsbygning

- **Null tankestrek:** Bruk aldri lang tankestrek (`—`), kort tankestrek (`–`) eller dobbel bindestrek (`--`) som innskudd i setninger. Del heller opp med komma, punktum, kolon eller parentes.
- **Si hva noe er:** Unngå den typiske språkmodell-vendingen *"Det handler ikke om X, men om Y"* eller *"mindre om X og mer om Y"*. Gå rett på hva løsningen faktisk gjør.
- **Kutt fyllet i starten og slutten:** Hopp over åpninger som *"Godt spørsmål!"*, *"Absolutt!"* og *"La oss dykke ned i..."*. Avslutt når det siste konkrete poenget er sagt, uten et oppsummerende sluttavsnitt.
- **Unngå tomme superlativer:** Stryk ord som *sømløs*, *robust*, *banebrytende*, *skreddersydd*, *helhetlig*, *i dagens digitale landskap*, *spennende reise* og *lidenskapelig*. Beskriv heller konkret hva som er bygget.
- **Rette anførselstegn:** Bruk vanlige rette anførselstegn (`"` og `'`).

## 4. Muntlig flyt i samtaler og lyd (TTS)

Når teksten skal leses høyt av en stemmemodell (tekst-til-tale) eller vises i en chat:

- Skriv kildesetningene og bakgrunnsnotatene i like enkelt og muntlig språk som du ønsker ut igjen. Hvis notatene inneholder tunge substantiver eller engelske setninger, vil modellen begynne å oversette på egen hånd midt i samtalen.
- Hold hvert avsnitt eller hver meldingsboble til 1 til 2 korte setninger med variert lengde.
- Unngå å lese opp filstier, pakkeversjoner eller epostadresser bokstav for bokstav i muntlige svar med mindre brukeren ber direkte om det.
