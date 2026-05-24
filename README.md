_(Find the [English project description](#stromgedacht-api-sensor-for-home-assistant) below)_

## StromGedacht API-Sensor für Home Assistant

In der Datei [sensor.yml](sensor.yml) wird ein Sensor definiert, der die Status-Daten von der StromGedacht API (Netzauslastung bei TransnetBW) abfragt.

Diese Information kannst Du nutzen, um z.B. temporär das Laden Deines Elektroautos an der Wallbox während einer Hochlastphase zu pausieren. Damit ermöglichst Du dem Netzbetreiber einen einfacherern Lastausgleich. Beim Wert "supergrün" wird ein hoher Anteil der Stromerzeugung durch CO2-neutrale Energiequellen wie Wind und Sonne gedeckt, daher ist es sinnvoll, planbaren Verbrauch in diese Zeiten zu verschieben.

Mögliche Werte des Sensors sind:

- `-1`= supergrün
- `1` = grün
- `3` = orange
- `4` = rot

### Einrichtung

1. Füge den Inhalt von [helpers.yml](helpers.yml) in Deine `configuration.yaml` ein (oder binde die Datei per `homeassistant: packages:` ein). Dieser Helper speichert die PLZ als konfigurierbaren Wert in Home Assistant.
2. Füge den Inhalt von [sensor.yml](sensor.yml) entsprechend in Deine Konfiguration ein.
3. Starte Home Assistant neu.
4. Ändere die PLZ über **Einstellungen → Geräte & Dienste → Helfer → StromGedacht ZIP code** – oder direkt im Dashboard über die Entity `input_text.stromgedacht_zip_code`.

Eine Beispiel-Karte für das Lovelace-Dashboard findest Du in der Datei [simple_lovelace_gauge.yml](simple_lovelace_gauge.yml).

![Lovelace Dashboard Karte](lovelace_gauge.png)

Ideen oder Bug Reports kannst Du [hier](issues/) eintragen.

Copyright (c) 2023–2025 by [Jean Pierre Wenzel](https://github.com/jpwenzel/).

Weitere Infos findest Du hier:

- StromGedacht (TransnetBW): <https://www.stromgedacht.de/>
- StromGedacht API-Dokumentation: <https://api.stromgedacht.de/>
- Home Assistant Sensor-Konfiguration: <https://www.home-assistant.io/integrations/sensor/>

## StromGedacht API sensor for Home Assistant

Use the sensor defined in [sensor.yml](sensor.yml) to provide information about TransNet electrical grid load.

Based on this load, you can decide to temporarily turn of energy consuming devices, e.g., your EV car charger, to allow for easier grid balancing for the provider. The value "supergreen" indicates an increased share of CO2-neutral sources in power production, e.g., by solar panels and wind turbines, and power consumption should probably be expedited/postponed to this time frame.

Available states are:

- `-1` = supergreen
- `1` = green
- `3` = amber/orange
- `4` = red

### Setup

1. Add the contents of [helpers.yml](helpers.yml) to your `configuration.yaml` (or include the file via `homeassistant: packages:`). This helper stores the ZIP code as a configurable value in Home Assistant.
2. Add the contents of [sensor.yml](sensor.yml) to your configuration accordingly.
3. Restart Home Assistant.
4. Change the ZIP code via **Settings → Devices & Services → Helpers → StromGedacht ZIP code** — or directly on the dashboard via the entity `input_text.stromgedacht_zip_code`.

You can find a simple gauge to be used with the Lovelace dashboard in [simple_lovelace_gauge.yml](simple_lovelace_gauge.yml).

![Lovelace Dashboard card](lovelace_gauge.png)

Ideas or bugs can be reported [here](issues/).

Copyright (c) 2023–2026 by [Jean Pierre Wenzel](https://github.com/jpwenzel/).

More info:

- StromGedacht (TransnetBW): <https://www.stromgedacht.de/>
- StromGedacht API documentation: <https://api.stromgedacht.de/>
- Home Assistant sensor configuration: <https://www.home-assistant.io/integrations/sensor/>
