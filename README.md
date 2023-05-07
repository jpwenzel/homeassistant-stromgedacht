_(See English description below)_

## StromGedacht API Sensor für Home Assistant

In der Datei [sensor.yml](sensor.yml) wird ein Sensor definiert, der die Status-Daten von der StromGedacht API (Netzauslastung bei TransnetBW) abfragt.

Diese Information kannst Du nutzen, um z.B. temporär das Laden Deines Elektroautos an der Wallbox während einer Hochlastphase zu pausieren. Damit ermöglichst Du dem Netzbetreiber einen einfacherern Lastausgleich.

Mögliche Werte des Sensors sind:

- `1` = grün
- `2` = gelb
- `3` = orange
- `4` = rot

Zur Konfiguration Deines Standorts ersetze die PLZ in der Sensorkonfiguration (`zip`) durch Deine eigene: `zip=76131`

Eine Beispiel-Karte für Das Lovelace-Dashboard findest Du in der Datei [simple_lovelace_gauge.yml](simple_lovelace_gauge.yml).

Ideen oder Bug Reports kannst Du [hier](issues/) eintragen.

Weitere Infos findest Du hier:

- StromGedacht (TransnetBW): <https://www.stromgedacht.de/>
- StromGedacht API Dokumentation: <https://api.stromgedacht.de/>
- Home Assistant Sensor Konfiguration: <https://www.home-assistant.io/integrations/sensor/>


## StromGedacht API sensor for Home Assistant

Use the sensor defined in [sensor.yml](sensor.yml) to provide information about TransNet electrical grid load.

Based on this load, you can decide to temporarily turn of energy consuming devices, e.g., your EV car charger, to allow for easier grid balancing for the provider.

Available states are:

- `1` = green
- `2` = yellow
- `3` = amber/orange
- `4` = red

To configure the location for which data is requested, replace the `zip` parameter with your own ZIP code: `zip=76131`

You can find a simple gauge to be used with the Lovelace dashboard in [simple_lovelace_gauge.yml](simple_lovelace_gauge.yml).

Ideas or bugs can be reported [here](issues/).

More info:

- StromGedacht (TransnetBW): <https://www.stromgedacht.de/>
- StromGedacht API documentation: <https://api.stromgedacht.de/>
- Home Assistant Sensor configuration: <https://www.home-assistant.io/integrations/sensor/>
