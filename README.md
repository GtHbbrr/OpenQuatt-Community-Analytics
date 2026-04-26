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

