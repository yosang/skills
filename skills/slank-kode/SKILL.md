---
name: slank-kode
description: "Hold kodebasen og konteksten slank under utvikling og kodegjennomgang. Bruk ved arkitekturvalg, refaktorering, ny funksjonalitet og vedlikehold."
---

# slank-kode

Språkmodeller har en tendens til å skrive mer kode enn nødvendig, legge til ekstra abstraksjonslag for fremtidige behov som aldri dukker opp, og spre samme informasjon utover mange filer. Denne ferdigheten holder kodebasen enkel å lese, enkel å vedlikeholde og billig i kontekst.

## 1. Rammer før kode, bygg og stram inn

1. **Lås rammene først:** Før du skriver kode, definer tekniske begrensninger, datamodell og faste regler i en kort `AGENTS.md`.
2. **Spike and Stabilize:** Bygg først den enkleste fungerende linjen fra datalag til brukergrensesnitt for å bekrefte at løsningen fungerer i praksis. Gå deretter over i opprydding: fjern midlertidig støy, sjekk edge cases og lås oppførselen med tester.

## 2. Samle data ett sted

Når samme informasjon (for eksempel prosjekter, ruter eller produkter) må oppdateres i tre eller fire ulike filer, oppstår det raskt feil når både mennesker og AI gjør endringer.

- **En sannhetskilde:** Legg datadefinisjoner i en felles fil med tydelig TypeScript-type, og la visningskomponenter, filtre, søkeord, metadata og AI-instrukser lese fra samme liste.
- **Trekk ut gjenbrukbare visningskomponenter først når de faktisk gjenbrukes:** Ikke lag abstrakte fabrikker eller wrapper-lag for en enkelt visning, men samle identisk kort- eller skjemamarkup i en ren komponent når den brukes flere steder.

## 3. Foretrekk sletting fremfor påbygging

Hver kodelinje som legges til, må leses og vedlikeholdes senere.

- **Slett ubrukt kode med en gang:** Utkommentert kode, ubrukte importer, utdaterte hjelpefunksjoner og ubrukte egenskaper slettes helt. Git tar vare på historikken.
- **Ingen selvfølgelige kommentarer:** Ikke skriv kommentarer som bare gjentar hva kodelinjen gjør eller hvilket steg i prompten den kom fra. Skriv kun kommentar når det ligger en ikke-åpenbar grunn eller teknisk begrensning bak valget (for eksempel hvorfor eldre TV-nettlesere krever animert WebP fremfor `<video>`).
- **Ingen skjulte feil:** Unngå tomme `try/catch`-blokker som svelger feil i stillhet, og unngå unødvendige null-sjekker på verdier som allerede er garantert av typesystemet. Håndter feil der du faktisk kan gjøre noe med dem.

## 4. Tester som sjekker reell oppførsel

- En test har kun verdi hvis den feiler når funksjonen slutter å virke.
- Test mot faktiske dataflyter, grenseverdier og samtidig belastning fremfor å bare teste at interne mocks kalles.
