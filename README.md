# OpenQuatt Community Analytics 📊

Dit project heeft als doel om de prestaties van Quatt-warmtepompen binnen de community objectief vergelijkbaar te maken. Door technische data (anoniem) te poolen, halen we de machine uit de 'black box'.

## 🎯 Doelen
- **Technisch Benchmarking:** Vergelijk de gezondheid van je machine via de Carnot-score.
- **Afgifte Optimalisatie:** Inzicht in de effectiviteit van radiatoren vs. vloerverwarming.
- **Community Diagnostics:** Patronen herkennen in defecten of software-updates.

## 🔒 Privacy-by-Design
We gebruiken het OpenAmber-principe:
1. **Anonimiteit:** Identificatie op basis van een SHA-256 hash van je MAC-adres/Device ID.
2. **Geografische vervaging:** Alleen de eerste twee cijfers van je postcode (voor KNMI-data).
3. **Transparantie:** Alle code voor data-extractie is open-source en inzichtelijk.

🧠 Waarom Dynamische Graaddagen & Hydraulische Analyse?
De meeste dashboards vergelijken simpelweg verbruik met buitentemperatuur. Dat is onnauwkeurig. Wij gaan een stap verder:
1. kWh per Dynamische Graaddag (Huis-efficiëntie)
Standaard graaddagen gaan uit van een vaste binnentemperatuur van 18°C. Maar een warmtepomp-gebruiker stookt vaak op 19, 20 of 21 graden.
Onze methode: We berekenen de graaddagen live op basis van jouw werkelijke thermostaat-setpoint.
Het resultaat: Een eerlijke score die laat zien hoe efficiënt jouw woning met warmte omgaat, ongeacht hoe warm je het binnen wilt hebben. Zo ontdek je of die laatste graad extra stoken je COP onevenredig hard omlaag trekt.
2. Hydraulische Delta-T & Flow (Afgifte-efficiëntie)
Een warmtepomp presteert optimaal bij een specifieke balans tussen flow (liters per uur) en de 
 (het verschil tussen aanvoer- en retourwater).
Onze methode: We loggen niet alleen de temperaturen, maar koppelen deze direct aan de flow-data uit de Modbus.
Het resultaat: We kunnen analyseren of jouw systeem 'hydraulisch in balans' is. Zie je een extreem lage 
 bij een hoge flow? Dan stroomt het water misschien te snel door je radiatoren om effectief warmte af te geven. Door dit te vergelijken met anderen, vind je de ideale instelling voor jouw pomp.
3. De Carnot-score (Machine-gezondheid)
Dit is de "APK-keuring" van je warmtepomp.
Onze methode: We vergelijken je actuele COP met het theoretisch maximum onder jouw specifieke condities.
Het resultaat: Een percentage dat puur de technische staat van je systeem aangeeft. Een zakkende score over de tijd betekent: actie ondernemen (bijv. verdamper reinigen of koudemiddel checken), nog voordat je energierekening ontploft.

## 🛠️ Hoe doe ik mee?

### Methode A: OpenQuatt (Modbus/ESP32)
Voeg de snippet uit `/esphome/analytics.yaml` toe aan je configuratie.

### Methode B: Home Assistant Integratie
Installeer de automatisering uit `/home-assistant/sync.yaml` om de data van de officiële hub door te sturen.

## 📈 De Metrics
We kijken verder dan alleen de COP. We berekenen o.a.:
- **Carnot Efficiency (%):** Hoe dicht zit je bij het theoretisch maximum?
- **kWh per Dynamische Graaddag:** Verbruik gecorrigeerd op jouw unieke thermostaat-setpoint.
- **Hydraulische Delta-T:** De balans tussen flow en afgiftetemperatuur.

