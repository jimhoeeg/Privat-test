# HOMAG Produktions-Kompasset

Interaktiv, videnbaseret lead generator og konfigurator til HOMAG Danmark A/S.

Værktøjet fører brugeren gennem seks trin, kortlægger produktionens modenhed og beregner
et vejledende investerings- og ROI-estimat med konkrete produktanbefalinger.

## Kom i gang

Åbn `index.html` direkte i en browser. Applikationen er en enkelt selvstændig fil
uden byggetrin, afhængigheder eller eksterne kald — HTML, CSS, vanilla JavaScript
og skrifttypen er indlejret i filen, så den også fungerer offline.

## Logo

`logo.svg` er kildefilen til HOMAG-logoet. Den er indlejret direkte i `index.html`,
så applikationen forbliver én selvstændig fil. Udskiftes logoet, skal SVG-stierne
opdateres begge steder — markuppen i sidehovedet bruger `fill="currentColor"`,
så farven styres fra CSS-variablen `--navy-deep`.

## Designlinje

Layout, typografi og farver følger homag.com (DA): Barlow som skrifttype (latin-subset
indlejret som data-URI), hvidt sidehoved med logo-lockup og hovedmenu, blå brand-hero,
brødkrummelinje, firkantede kort, pill-formede knapper i HOMAG-cyan `#009EE0`,
fyldte formularfelter og mørk sidefod. Primærfarverne er HOMAG-blå `#005080` og
mørkeblå `#003D66`.

## Indhold

| Trin | Emne |
|------|------|
| 1 | Profilering og segmentering (snedkeri, industri, træbyggeri, bygningskomponenter) |
| 2 | Maskinsundhed og risikoprofil (maskinalder, uplanlagt nedetid) |
| 3 | Flaskehalse og automation (ilægning/aflæsning ved hovedmaskiner) |
| 4 | Digital workflow og materialeudnyttelse (dataoverførsel, spildprocent) |
| 5 | Fremtidssikring og skalering (primært forretningsmål) |
| 6 | Resultat-dashboard, anbefalinger og lead capture |

## Beregningsmotor

- **Produktions-Index (0–100)** — vægtet score på tværs af maskinsundhed, automationsgrad,
  digital modenhed og materialeudnyttelse.
- **Investeringsramme** — segmentbaseret grundinterval justeret additivt ud fra svarene.
  Referencescenarierne rammer 180.000–450.000 DKK (snedkeri), 650.000–1.800.000 DKK
  (serieproduktion med ældre park) og 1.200.000–4.500.000 DKK (træbyggeri/elementer).
- **Tilbagebetalingstid** — beregnet ud fra frigjorte mandetimer, reduceret nedetid,
  lavere materialespild, mindre administration og øget kapacitet. Vises i intervallet
  11–22 måneder med en konservativ realiseringsgrad på 55 %.

## Lead capture

Formularen valideres i browseren (navn, virksomhed, e-mail, telefon, samtykke) og
simulerer indsendelse. Payload til CRM/marketing automation samles i `submitLead()` og
logges til konsollen — her indsættes det reelle endpoint ved idriftsættelse.
Efter indsendelse kan rapporten udskrives eller gemmes som PDF via browserens
udskriftsdialog (dedikeret print-stylesheet).
