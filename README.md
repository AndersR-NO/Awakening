# Awakening
A strategy survival game about how everything is connected.

## Spill prototype 0.2
Last ned `index.html` og åpne i en moderne nettleser. Ingen server, installasjon eller eksterne ressurser trengs.

Menneskeheten må utvikle seg fra steinalderen til en sivilisasjon som kan forlate jorda før planeten blir ubeboelig. Årsaken og den historiske tidshorisonten er foreløpig åpne designvalg. Ingen utenomjordisk hovedperson eller hjemreise til Alpha Centauri.

**Første mål er uendret:** Overlev tre døgn, bygg bål og to hytter, og utvikle bedre steinredskaper.

## RTS-kontroller
- Innbyggerne starter ledige. Klikk en person på kartet eller i listen for å velge.
- Dra med venstre museknapp for å velge flere; Shift legger til/fjerner ved personklikk og legger til ved rammevalg. «Velg alle» velger hele stammen.
- Med personer valgt: klikk på en ressurs for innsamling, eller ledig mark for flytting. Høyreklikk kan også gi ordre.
- Elvekanten gir vann, bærbusker gir mat, trær gir ved, steinblokker gir stein. Den lilla kunnskapsplassen gir forskning.
- Velg arbeidere, trykk på et bygg og klikk på ledig gress. Ressursene betales når byggeplassen opprettes. Arbeiderne går frem og bygger; flere arbeidere bygger raskere. Klikk på en uferdig byggeplass for å gjenoppta arbeidet.
- «Stopp» avbryter valgte personers ordre. De blir ledige når en flytte- eller byggeordre er ferdig. Innsamling fortsetter til ny ordre gis.
- Høyredra eller midtdra panorerer; rull zoomer. Mellomrom pauser og Escape avslutter byggemodus.
- Lagre/last inn bruker lokal nettleserlagring. Versjon 0.2 har et nytt lagringsformat; gamle 0.1-lagringer importeres ikke eller overskrives.

## Omfang og begrensninger
Canvas 2D med midlertidig grafikk. Innbyggere går langs beregnede ruter og produserer først ved ankomst. Vann og bygg blokkerer ruter, mens vegetasjon kan passeres. Innbyggerne kan overlappe hverandre. Ressursene er foreløpig ubegrensede, og legges direkte i felles beholdning uten bæring til lager.

Ett døgn er 120 simulerte sekunder; en sesong varer tre døgn. Felles helsetilstand og hendelsesbaserte rovdyr er enkle modeller. Klær, andre stammer, avanserte produksjonskjeder, epokesprang og romfart er ikke implementert. Filmsekvensen er ikke produsert.

## Tester
`node tests/simulation.cjs` tester idle-start, ordre, reisetid, bygging, kostnader, gjennomførbart oppdrag, tap og lagringsformat uten avhengigheter.

Nettlesertest: installer Playwright og Chromium, kjør `node tests/browser.cjs`. Nettlesertesten er oppdatert, men kunne ikke kjøres i utviklingsmiljøet fordi Chromium ikke var tilgjengelig. Visuell QA gjenstår.
