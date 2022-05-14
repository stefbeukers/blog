---
title: Raspberry Pi instellen en gebruiken met enkel een Chromebook
---

Zelf gebruik ik privé een Chromebook en een iPad als mijn computer. Zakelijk heb ik een Windows laptop, maar die gebruik ik - zoals bedoeld - zakelijk. 

Om een Raspberry Pi werkend te krijgen kan dat best een uitdaging zijn met een Chromebook en/of iPad. Toch is het wel mogelijk. Het is zelfs mogelijk zonder een monitor, toetsenbord en muis. Wat je wel nodig hebt?

## Benodigdheden
- Een WiFi-verbinding waar je toegang toe hebt
- Een Chromebook
- Een SD of MicroSD kaartlezer (kan standaard in je Chromebook zitten)
- Een Raspberry Pi die geschikt is voor een WiFi-verbinding
- Een image van [Raspbian OS](https://www.raspberrypi.org/downloads/raspbian/), gedownload op je Chromebook
- De [Chromebook Herstel applicatie](https://chrome.google.com/webstore/detail/chromebook-recovery-utili/jndclpdbaamdhonoechobihbbiimdgai)
- Een tekst editor, [Text](https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkjmjhdgbg) bijvoorbeeld

## Micro-SD kaart voorbereiden
Zoals gezegd moet je de image van Raspbian OS vooraf naar je Chromebook downloaden. Die heb je in de volgende stap nodig. Zorg ook dat je de micro-SD kaart in je Chromebook hebt zitten en dat deze leeg en geformatteerd is.

Start de Chromebook Herstel applicatie en klik rechtsboven op het tandwiel om een lokale image te selecteren. Selecteer vervolgens de image van Raspbian OS (als .zip, de Chromebook Herstel applicatie kan hiermee overweg).

De image wordt naar de micro-SD kaart geschreven en als dit gedaan is zie je twee mappen op je micro-SD kaart. We moeten nog twee bestanden toevoegen aan de map ‘Boot’, zodat je Raspberry Pi direct verbinding kan maken met je netwerk.

## Netwerkverbinding en SSH inschakelen
Open twee nieuwe documenten in de tekst editor en sla deze op je Chromebook op. Deze kopiëren we straks naar de micro-SD kaart.

1. Het eerste bestand krijgt de naam ‘ssh’ (zonder bestandsformaat). Dit bestand mag verder helemaal leeg blijven. Dit zorgt ervoor dat SSH ingeschakeld wordt op je Raspberry Pi.
2. Het tweede bestand krijgt de naam ‘wpa_supplicant.conf’ (.conf is het bestandsformaat). Hieronder zie je wat in dit bestand moet komen te staan. De velden achter ‘country’, ‘ssid’ en ‘psk’ moet je aanpassen naar je eigen situatie. Dit zorgt ervoor dat je Raspberry Pi verbinding kan maken met je netwerk.

`country=US`  
`ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev`  
`update_config=1`  

`network={`  
`ssid="jouw WiFi-verbinding"`  
`psk="jouw Wifi-wachtwoord"`  

Kopieer vervolgens beide bestanden naar de map ‘Boot’ op de micro-SD kaart. 

## Raspberry Pi aanzetten
Dan is het tijd om de micro-SD kaart in je Raspberry Pi te stoppen en deze aan te sluiten op netstroom. 

Je Raspberry Pi is nu verbonden met je netwerk en kan via SSH benaderd worden. Hierover is een andere blogpost meer.