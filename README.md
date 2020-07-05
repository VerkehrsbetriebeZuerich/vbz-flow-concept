# Fahrgastzahlen VBZ interaktiv visualisiert

## Projekt

Die Verkehrsbetriebe Zürich erheben die Nutzung ihrer Fahrzeuge auf dem gesamten Verkehrsnetz und publizieren diese Daten als Open Data. Es handelt sich dabei um Extrapolationen, welche auf Zähleinrichtungen in den VBZ-Fahrzeugen und manuellen Zählungen basieren und seit 2015 publiziert werden. Ein Datensatz repräsentiert die Fahrt eines Fahrzeugs zwischen jeweils zwei Haltestellen einer Linie zu einer fahrplangemässen Abfahrtszeit. Er enthält jeweils die Anzahl ein- und aussteigender Personen an der Starthaltestelle und die Anzahl Reisender auf dem Streckenabschnitt. Es entsteht so ein vollständiger Überblick über das (extrapolierte) Verhalten aller Fahrgäste der VBZ innerhalb eines Tages. 

## Umsetzung

Die Netzstatistik der VBZ wird mithilfe der Koordinatenangaben im offenen Dienststellendokumentation der SBB "DiDok" georeferenziert und über das Python-Modul Geopandas als Geodatensatz nutzbar gemacht. Auf Grundlage der Informationen der VBZ über Fahrzeugmodelle und ihren Einsatz werden Kapazitätsgrenzen der einzelnen Linien errechnet. Die Fahrgastzahlen werden zusammengefasst, um Aussagen über den Gesamtpersonenfluss jeweils einzelner Abschnitte (die Strecke zwischen zwei Haltestellen als atomare Einheit) über den Zeitraum zwischen zwei vollen Stunden an einem Werktag (Mo-Fr) bzw. Wochenendtag machen zu können. Die Daten werden im GeoJSON-Format ausgegeben, um sie in Form einer interaktiven Webkarte darstellen zu können; eine solche wird mit Mapbox GL erstellt. 

Der gesamte [Arbeitsprozess mit Rohdaten](https://github.com/bountan/vbz-dataprep) ist abrufbar auf Github. 

Die [vollständige Webseite](https://github.com/bountan/vbz-flow-concept) ist ebenfalls verfügbar.


## Datenquellen
Alle verwendeten Daten werden sind öffentlich zugänglich 
[Open Data Zürich: Fahrgastzahlen VBZ](https://data.stadt-zuerich.ch/dataset/vbz_fahrgastzahlen_ogd)	
[Fahrzeugkenndaten VBZ](https://www.stadt-zuerich.ch/vbz/de/index/die_vbz/fahrzeuge.html) 

[Haltestellen gemäss opentransportdata.swiss](https://data.sbb.ch/explore/dataset/dienststellen-gemass-opentransportdataswiss/table/)

## Autoren

Ueli Isenschmid

Anian Pleisch

Janik Sievert

Severin Spörri

## Lizenz

[GNU](https://choosealicense.com/licenses/gpl-3.0/) 
