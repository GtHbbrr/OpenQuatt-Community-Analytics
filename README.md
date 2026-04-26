# OpenQuatt Community Analytics 📊

Dit project heeft als doel om de prestaties van Quatt-warmtepompen binnen de community inzichtelijk en vergelijkbaar te maken. Of je nu een **OpenQuatt (ESP32)** gebruikt of de **Home Assistant Quatt-integratie**, jouw data helpt ons om de "Black Box" van onze warmtepompen te openen.

## 🎯 Waarom meedoen aan de Nulmeting?

De meeste van onze installaties draaien op de standaardinstellingen van de Quatt CiC. Maar hoe presteert die standaard nu echt in verschillende woningen?

- **Objectief Benchmarken:** Vergelijk temperaturen, drukken en verbruik met de 'gemiddelde' Quatt van de community onder vergelijkbare weersomstandigheden.
- **Vermeende Afwijkingen Checken:** Zie je vreemd pendelgedrag of een onverklaarbare defrost? In het dashboard zie je direct of dit een bekend fenomeen is of dat jouw systeem afwijkt van de norm.
- **De APK-check (Carnot-score):** We gebruiken een technische score die de invloed van het weer wegfiltert. Zo zie je puur de technische conditie van je machine (vervuilde verdamper? koudemiddel ok?).
- **Huis-efficiëntie:** Dankzij de metric 'kWh per Dynamische Graaddag' (gecorrigeerd op jouw thermostaat-setpoint) zie je eindelijk hoe efficiënt jouw woning met de geleverde warmte omgaat.

## 🔒 Privacy-by-Design

Deelname is veilig en drempelloos (gebaseerd op het OpenAmber-model):
1. **Anonimiteit:** Identificatie vindt plaats op basis van een hash van je Device ID of MAC-adres. Geen accounts, geen namen.
2. **Geografische vervaging:** We gebruiken alleen de eerste cijfers van je postcode voor de koppeling met lokale KNMI-weerdata.
3. **Transparantie:** Alle code die data verstuurt is open-source en vooraf door jou in te zien in deze repository.

# ⚠️ STATUS: INFRASTRUCTUUR IN OPBOUW (HULP GEZOCHT!)

**Welkom bij OpenHeatPumps!** De visie voor dit analytics platform staat, de metrics (zoals de Carnot-score) zijn gedefinieerd en het domein **openheatpumps.nl** is vastgelegd.

### 🛠️ Gezocht: Server & Dashboard Experts
Omdat de focus van dit project momenteel ligt op de thermodynamica en de Quatt-data, zoeken we hulp vanuit de community voor de technische fundering:
- **Hosting:** Wie kan/wil een centrale MQTT-broker en InfluxDB hosten?
- **Dashboarding:** Wie helpt mee met het bouwen van de Grafana-dashboards?
- **Automatisering:** Wie wil de backend-scripts voor data-verwerking verfijnen?

**Heb je de skills?** Open een Issue of laat van je horen in de Quatt topics op Tweakers. De YAML-snippets in deze repo zijn momenteel 'placeholders' tot de broker-URL actief is.

## 🛠️ Hoe doe ik mee?

Het platform ondersteunt twee manieren van aanleveren via **openheatpumps.nl**:

### Methode A: OpenQuatt (Modbus / ESP32)
Voor gebruikers met een eigen ESP32 controller. Voeg de snippet uit `/esphome/analytics.yaml` toe aan je configuratie voor high-res data.

### Methode B: Home Assistant Quatt-integratie
Voor gebruikers van de officiële hub. Gebruik de automatisering uit `/home-assistant/quatt_sync_automation.yaml` om de belangrijkste parameters door te sturen.

## 🤝 Bijdragen
Heb je verstand van Grafana-dashboards, InfluxDB of wil je meehelpen de metrics te verfijnen? Kijk in de `CONTRIBUTING.md` of open een Issue!

*Laten we stoppen met gissen en de krachten van de community bundelen op [openheatpumps.nl](http://openheatpumps.nl).*
