# HOMAG Produktions-Kompasset

Interaktiv, videnbaseret lead generator og konfigurator til HOMAG Danmark A/S.

Værktøjet fører brugeren gennem seks trin, kortlægger produktionens modenhed og beregner
et vejledende investerings- og ROI-estimat med konkrete produktanbefalinger.

## Kom i gang

Åbn `index.html` direkte i en browser. Applikationen er en enkelt selvstændig fil
uden byggetrin, afhængigheder eller eksterne kald — HTML, CSS og vanilla JavaScript
er indlejret i filen.

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
