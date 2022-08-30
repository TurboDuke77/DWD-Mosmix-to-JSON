coming soon...

# dwd-forecast-mosmix-json.php
## german DWD Weather Forecast MOSMIX to JSON

Dieses PHP Script lädt für den gewünschten Ort, entweder bei jedem Aufruf oder datensparend 4x am Tag, die Daten vom DWD Server und erzeugt eine JSON-Datei mit 16 Wettervariablen für die Weiterverarbeitung auf der eigenen Wetterseite.

This PHP script loads the data from the DWD server for the desired location, either at every call or data-saving 4 times a day, and generates a JSON file with 16 weather variables for further processing on your own weather page.

#### Wettervorhersage vom deutschen Wetterdienst
#### Weather forecast by the German Weather Service
- [Link DWD.de](https://www.dwd.de/)

---

#### Aufruf Beispiel / example call

- die dwd-forecast-mosmix-json.php muss manuell oder über einen cronjob mehrmals am Tag aufgerufen werden, dabei wird die MOSMIX_L_LATEST_station-id.kmz vom Server opendata.dwd.de geladen und gespeichert

- ein paar Parameter müssen im Script angegeben werden, wie die Station ID, der Download und Ausgabepfad auf dem Server
- andere Parameter können nach den eigenen Bedürfnissen angepasst werden

- als Ausgabe wird eine aufbereitete JSON Datei mit den stündlichen Wetterparametern erstellt und gespeichert:


#### Ausgabe Beispiel für eine Stunde in der JSON Datei / output example for one hour

"Forecast": {
 "0": {
      "0": "Zeitstempel+UTC-Versatz",
      "1": "Datum",
      "2": "Zeitraum bis",
      "3": "min Temperatur letzte 12Std °C",
      "4": "max Temperatur letzte 12Std °C",
      "5": "Temperatur 2m °C",
      "6": "Taupunkt 2m °C",
      "7": "Windrichtung °",
      "8": "Windgeschwindigkeit km/h",
      "9": "Windböe km/h",
      "10": "Bedeckungsgrad %",
      "11": "Luftdruck hPa",
      "12": "Niederschlag Wahrscheinlichkeit %",
      "13": "Niederschlag mm",
      "14": "Niederschlag letzte 12Std mm",
      "15": "Sonnenschein Dauer min",
      "16": "Sichtweite km",
      "17": "Signifikantes Wetter",
      "18": "Luftfeuchtigkeit %",
      "19": "icon"
    },
"1": {
      "0": "2022-08-30T18:00:00+02:00",
      "1": "2022-08-30",
      "2": "18:00",
      "3": "-",
      "4": "-",
      "5": "22.5",
      "6": "11.8",
      "7": "22 NNO",
      "8": "9",
      "9": "19",
      "10": "85",
      "11": "1021",
      "12": "1",
      "13": "0",
      "14": "0",
      "15": "10",
      "16": "81.1",
      "17": "stark bewölkt",
      "18": "51",
      "19": "3d.svg"
 }


##### MOSMIX_L
- Der MOSMIX-Vorhersagedatensatz "MOSMIX_L" enthält ca. 115 Wettervariablen pro Vorhersage und die maximale Vorhersagezeit beträgt +240 Stunden (10 Tage Trend). Die Vorhersage wird 4 mal täglich um 03, 09, 15 und 21 Uhr UTC vom DWD aktualisiert. Die Download Größe einer MOSMIX_L_.kmz Datei einer DWD Station beträgt 16-20 kbyte, die erstellte JSON Datei ist ca. 60-80 kbyte groß.

- The MOSMIX forecast data set "MOSMIX_L" contains about 115 weather variables per forecast and the maximum forecast time is +240 hours (10 days trend). The forecast is updated 4 times a day at 03, 09, 15 and 21 UTC by DWD. The download size of a MOSMIX_L_.kmz file of a DWD station is 16-20 kbyte, the created JSON file is about 60-80 kbyte.


##### German INFOS und LINKS (some documents you can switch to english)
- [README opendata.dwd.de ](https://opendata.dwd.de/README.txt)
- [MOSMIX-L - DWD ](https://dwd-geoportal.de/products/G_FJM/)
- [MOSMIX-L Element Definition ](https://www.dwd.de/DE/leistungen/opendata/help/schluessel_datenformate/kml/mosmix_elemente_xls.xlsx?__blob=publicationFile&v=7)
- [Model Output Statistics-MIX (MOSMIX)](https://www.dwd.de/DE/leistungen/met_verfahren_mosmix/met_verfahren_mosmix.html)
- [MOSMIX-Vorhersagedaten FAQ](https://rcccm.dwd.de/DE/leistungen/met_verfahren_mosmix/faq/faq_mosmix_node.html)
- [DWD Stationskatalog (Vorhersagepunkte)](https://www.dwd.de/DE/leistungen/met_verfahren_mosmix/mosmix_stationskatalog.cfg?view=nasPublication&nn=16102)
- [ww-Code - Hashs mit deutschen Konditionen (Code/Description)](https://wetterkanal.kachelmannwetter.com/was-ist-der-ww-code-in-der-meteorologie/)

