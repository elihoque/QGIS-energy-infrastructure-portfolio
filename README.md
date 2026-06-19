# GIS-Portfolio: Energie- und Infrastrukturanalysen (Bremen)

Dieses Repository dokumentiert meine technischen Projekte im Bereich Geoinformationssysteme (GIS), kombiniert mit meinen Kompetenzen als Master of Science in Elektrotechnik.

## Projekt 1: Optimierung von E-Ladestationen in Bremen
* **Ziel:** Identifikation von Versorgungslücken im städtischen Ladenetz für Elektrofahrzeuge.
* **Methodik:** Daten-Extraktion via OpenStreetMap (QuickOSM), Puffer-Analysen (500m Radius) und räumliche Cluster-Erkennung in QGIS.
* **Ergebnis:** Eine detaillierte Karte der prioritären Ausbauzonen für die lokale Netzinfrastruktur.

### Projektergebnisse
* Siehe die finale PDF-Karte: [Bremen_EV_Optimization.pdf](./Bremen_EV_Optimization.pdf)
* # Projekt 2: PV-Einspeisepotenzial vs. Ortsnetztransformator-Kapazität

## Projektübersicht
In diesem Projekt wurde das theoretische maximale solare Einspeisepotenzial eines Wohnquartiers im Raum Bremen auf Basis von offiziellen Liegenschaftsdaten (ALKIS) berechnet und einer elektrotechnischen Netzverträglichkeitsprüfung unterzogen.

## Technische Parameter & Formeln
Die geometrische Auswertung der Dachflächenpolygone erfolgte in QGIS. Die finale Peak-Leistung ($P_{\text{peak}}$) wurde über den Feldrechner mit folgender ingenieurmäßiger Restriktion berechnet:

$$P_{\text{peak}} = \text{Dachfläche} \times 0{,}40 \ (\text{Nutzungsgrad}) \times 0{,}20 \ (\text{Modulwirkungsgrad})$$

### Kennzahlen der Analyse:
* **Datenquelle:** Landesamt GeoInformation Bremen (ALKIS-Liegenschaftskarte)
* **Berechnete Gesamtleistung:** **1680,01 kWp**
* **Referenz-Betriebsmittel:** 630 kVA Ortsnetztransformator (Typischer Standard der swb Regional GmbH)
* **Überlastungsfaktor:** **> 260%** im ungesteuerten Worst-Case-Szenario.

## Ergebnisse und Dokumentation
Die vollständige ingenieurtechnische Netzengpassanalyse sowie die graduierte Potentialkarte finden Sie in der ausführlichen Projektdokumentation:
👉 **[Hier klicken für den vollständigen PDF-Bericht](././bremen_solar_transformer_analysis.pdf)**

## Erworbenes GIS-Know-how:
* Verarbeitung von offiziellen Katasterdaten im Shapefile-Format (ALKIS).
* Geometrische Berechnungen mit nativen QGIS-Funktionen (`$area`).
* Attributdaten-Slicing und statistische Aggregationsanalysen via Statistical Summary Panel.
* Erweiterte layerbasierte Theme-Symbolisierung (Graduierte Darstellung).
