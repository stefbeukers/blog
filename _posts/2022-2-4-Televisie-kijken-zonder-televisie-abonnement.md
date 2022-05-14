---
title: Televisie kijken zonder televisie-abonnement
---

Cord-cutten is de Engelse term voor het niet meer hebben van een televisie-abonnement via de kabel. In praktijk knip je geen kabel door, maar zeg je gewoon je televisie-abonnement bij je provider op. 

Dat heb ik recent gedaan en daarom wil ik graag kort beschrijven waarom je prima zonder kabel kunt en hoe je dat kunt regelen.

## Waarom?
Waarom zou je cord-cutten? Waarschijnlijk wil je alleen betalen voor hetgeen waar je gebruik van maakt. En hoeveel gebruik maak je van alle zenders die je van je provider afneemt? En dan gaat het vooral om lineaire televisie. Je kunt heel veel programma’s namelijk via internet kijken of terugkijken (en soms zelfs vooruitkijken).

Het is financieel best interessant om te cord-cutten. Een televisie-abonnement via je provider kost je al gauw een paar tientjes per maand. Terwijl je online een stuk voordeliger uit bent.

## Hoe?
Wat heb je dan nodig om te cord-cutten? Nou eigenlijk vooral een internetverbinding. Op mijn adres is glasvezel beschikbaar en daar maak ik dus graag gebruik van. 

Eerder had ik een televisie- en internetabonnement van Ziggo voor €71,00 per maand. Voor dat geld had ik iets meer dan 80 televisiezenders en 300 Mbit/s download & 30 Mbit/s upload. Daarbij komt de kanttekening dat het netwerk van Ziggo 97% glasvezel is, maar het laatste stukje naar je woning toe alsnog over coax gaat.

### Internet
Inmiddels heb ik een glasvezelverbinding van T-Mobile (op mijn adres over het netwerk van KPN) voor €30 per maand. Voor dat bedrag krijg ik 100 Mbit/s download & 100 Mbit/s upload. Meer dan genoeg voor dit huishouden.

Het abonnement bij T-Mobile valt wat voordeliger uit omdat ik ook een Tele2 telefoonabonnement heb en dus wat klantvoordeel krijg op beide abonnementen.

### Televisie
Om toch wat televisiezenders te kunnen bekijken (en vooral terug- en vooruit te kijken) heb ik er een NLZIET-abonnement bij genomen, voor €7,95 per maand. Daarmee kijk je 34 Nederlandse zenders (NPO, RTL, SBS, et cetera) via een app op je smart-tv, telefoon of iPad. Casten naar een Chromecast kan ook.

Waar ik dus eerder €71,00 per maand kwijt was aan internet en televisie, betaal ik nu €37,95 per maand. Dat is een besparing van zo’n 46%.

Naast NLZIET heb ik nog wat streamingdiensten zoals Netflix en Disney+, maar die kosten maakte ik ook toen ik nog een televisie- en internetabonnement bij Ziggo had. 

## Hardware
Als je dan alles over internet gaat doen, wil je ook een stabiel en snel netwerk hebben. Elke situatie en woning is natuurlijk anders, maar in een nieuwbouw rijtjeshuis met in totaal drie verdiepingen is dat gelukt met de volgende hardware:

- Zyxel T50
- TP-Link Deco M5 (3x)
- TP-Link switch (2x)

### Setup
De Zyxel T50 van T-Mobile, fungeert in de meterkast als modem en router. Hierop zit een switch aangesloten, waar twee UTP-kabels uit komen: eentje naar de woonkamer en eentje naar de slaapkamer op de eerste verdieping. 

De UTP in de woonkamer heeft een switch waarop de televisie, PlayStation, Hue bridge en een Deco bekabeld zijn aangesloten. De UTP in de slaapkamer zorgt voor een bekabelde Deco op de eerste verdieping. De Deco op zolder is draadloos verbonden.

Met deze setup haal ik draadloos op de begane grond en de eerste verdieping de maximale snelheid van 100/100 Mbit/s. Op zolder is de snelheid iets lager - namelijk 80/80 Mbit/s - maar dat is ook niet gek aangezien die laatste Deco niet bekabeld is aangesloten. 

### Even opletten
Met deze setup zijn er nog drie puntjes die wat aandacht behoeven:
1. De Deco M5 moet in Access-Point modus staan, aangezien de Zyxel van T-Mobile niet in bridge-mode kan. Als de Deco in Router modus staat heb je eigenlijk twee apparaten in je netwerk die de routing willen regelen en dat zorgt voor problemen.

2. De switch tussen de Zyxel en de bekabelde Decos is nodig omdat de switch in de Zyxel de benodigde discovery packets blokkeert. Het rechtstreeks aansluiten van de Decos op de Zyxel werkt dus niet.


3. Aangezien de Decos een draadloos netwerk verzorgen is het handig om het draadloze netwerk van de Zyxel uit te zetten. Dit kan makkelijk door erop in te loggen, maar de Zyxel heeft hier ook een fysieke knop voor.