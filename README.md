coming soon...

# dwd-forecast-mosmix-json.php
## german DWD Weather Forecast MOSMIX to JSON

#### Wettervorhersage vom deutschen Wetterdienst
#### Weather forecast by the German Weather Service
- [Link DWD.de](https://www.dwd.de/)

---

#### Aufruf Beispiel / example call

- 

- Der MOSMIX-Vorhersagedatensatz "MOSMIX_L" enthält ca. 115 Wettervariablen pro Vorhersage und die maximale Vorhersagezeit beträgt +240 Stunden (10 Tage Trend). Die Vorhersage wird 4 mal täglich um 03, 09, 15 und 21 Uhr UTC vom DWD aktualisiert. Dieses PHP Script lädt für den gewünschten Ort, entweder bei jedem Aufruf oder datensparend 4x am Tag, die Daten vom DWD Server und erzeugt eine JSON-Datei mit 16 Wettervariablen für die Weiterverarbeitung auf der eigenen Wetterseite.

- The MOSMIX forecast data set "MOSMIX_L" contains about 115 weather variables per forecast and the maximum forecast time is +240 hours (10 days trend). The forecast is updated 4 times a day at 03, 09, 15 and 21 UTC by DWD. This PHP script loads the data from the DWD server for the desired location, either at every call or data-saving 4 times a day, and generates a JSON file with 16 weather variables for further processing on your own weather page.


##### German INFOS und LINKS (some documents you can switch to english)
- [README opendata.dwd.de ](https://opendata.dwd.de/README.txt)
- [MOSMIX-L - DWD ](https://dwd-geoportal.de/products/G_FJM/)
- [MOSMIX-L Element Definition ](https://www.dwd.de/DE/leistungen/opendata/help/schluessel_datenformate/kml/mosmix_elemente_xls.xlsx?__blob=publicationFile&v=7)
- [Model Output Statistics-MIX (MOSMIX)](https://www.dwd.de/DE/leistungen/met_verfahren_mosmix/met_verfahren_mosmix.html)
- [Beschreibungen der einzelnen Parameter des Elementes Wetter (ww...)](https://www.dwd.de/DE/leistungen/opendata/help/schluessel_datenformate/kml/mosmix_element_weather_xls.html)
- [MOSMIX-Vorhersagedaten FAQ](https://rcccm.dwd.de/DE/leistungen/met_verfahren_mosmix/faq/faq_mosmix_node.html)
- [DWD Stationskatalog (Vorhersagepunkte)](https://www.dwd.de/DE/leistungen/met_verfahren_mosmix/mosmix_stationskatalog.cfg?view=nasPublication&nn=16102)
- [ww-Code - Hashs mit deutschen Konditionen (Code/Description)](https://wetterkanal.kachelmannwetter.com/was-ist-der-ww-code-in-der-meteorologie/)

