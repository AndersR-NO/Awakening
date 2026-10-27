# Awakening
A strategy survival game about how everything is connected.

## Spill prototype 0.1
Last ned `index.html` og åpne filen i en moderne nettleser. Ingen installasjon, server, eksterne ressurser eller byggetrinn er nødvendig. Dette er en lokal prototype, ikke en publisert spilltjeneste.

Fordel seks innbyggere mellom vann, mat, ved, stein og forskning. Frigjør en arbeider med minus før du legger vedkommende til en annen oppgave. Velg et bygg og klikk på ledig gress. Dra kartet for å panorere og rull for å zoome. Mellomrom pauser, Escape avbryter bygging. Lagre/last inn bruker nettleserens lokale lagring; tilgjengelighet ved file:// kan variere mellom nettlesere.

**Mål:** Overlev tre døgn, bygg et bål og to hytter, og utvikle bedre steinredskaper. Etterpå kan du fortsette i sandkassen.

## Status og avgrensning
- Skrått ovenfraperspektiv i Canvas 2D, med midlertidig kodebasert grafikk.
- Ressurser, arbeidsfordeling, byggekostnader, forskning, felles helsetilstand, dag/natt og fire sesonger.
- Ett døgn = 120 simulerte sekunder. Sesong skifter etter tre døgn. Dette er spillbalanse, ikke en historisk tidsmodell.
- Rovdyr er foreløpig en hendelse med konsekvens, ikke bevegelige fiender.
- Innbyggernes bevegelser er illustrasjoner; produksjon følger arbeidsfordelingen, ikke faktisk transport eller veifinning.
- Bygg fullføres straks. Ingen klær, befolkningsvekst, andre stammer, avanserte produksjonskjeder eller romfart ennå.
- Big Bang-filmen er ikke produsert. Ingen endelig spillmotor eller visuell stil er valgt.

## Utvikling
`node tests/simulation.cjs` tester simuleringsreglene uten avhengigheter.

For nettlesertest: `npm install --no-save playwright` og `npx playwright install chromium`, deretter `node tests/browser.cjs`. Testen skriver skjermbilder utenfor prosjektmappen. Se `docs/ROADMAP.md` for neste arbeid.
