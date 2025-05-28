# Pumpenanalyse – Projekt im Rahmen der Vorlesung Strömungsmaschinen (DHBW Karlsruhe)
# Code:53350

## Projektbeschreibung

Im Rahmen des Projekts zur Vorlesung *Strömungsmaschinen* an der DHBW Karlsruhe wurde das Betriebsverhalten einer Wasserpumpe mithilfe realer Messdaten und technischer Herstellerangaben analysiert. Ziel war es, die Energieeffizienz der Pumpe zu untersuchen und Rückschlüsse auf mögliche Energieverluste zu ziehen.

Die Analyse wurde mit Python durchgeführt und in einer strukturierten Umgebung umgesetzt. Alle Berechnungen und Visualisierungen wurden in einem Jupyter Notebook dokumentiert.

## Projektkontext

- Es handelt sich um eine Wasserpumpe, die in einer industriellen Umgebung eingesetzt wird.
- Der Hersteller stellt ein technisches Datenblatt mit Leistungs- und Förderkennlinien zur Verfügung.
- Der Volumenstrom wurde nach der Pumpe über einen bestimmten Zeitraum gemessen und in einer CSV-Datei gespeichert (`volume_flow_data.csv`).
- Der Laufraddurchmesser der Pumpe beträgt 264 mm.

## Bearbeitete Aufgaben

### 1. Berechnung des Energieverbrauchs
Auf Basis des gemessenen Volumenstroms (in m³/h) und der aus dem Datenblatt interpolierten Eingangsleistung wurde die gesamte elektrische Energie berechnet, die die Pumpe über den Messzeitraum aufgenommen hat.

### 2. Ermittlung des durchschnittlichen Wirkungsgrads
Die hydraulische Leistung der Pumpe wurde mithilfe der Förderhöhe (aus der Kennlinie), der Dichte des Mediums und der Erdbeschleunigung berechnet. Anschließend wurde der Wirkungsgrad als Verhältnis der hydraulisch umgesetzten Energie zur zugeführten elektrischen Energie bestimmt.

### 3. Berechnung der nicht genutzten Energie
Die Differenz zwischen zugeführter und nutzbarer Energie wurde als Leistungsverlust (z. B. durch Wärme, Reibung etc.) betrachtet und separat ausgewertet.

### 4. Zusätzliche Analysen
Zur besseren Interpretation wurden verschiedene Visualisierungen erstellt:
- Zeitverläufe von Volumenstrom, hydraulischer Leistung, Eingangsleistung und Leistungsverlust
- Histogramme und Boxplots zur statistischen Verteilung wichtiger Parameter wie Volumenstrom, Förderhöhe und Eingangsleistung
- Gleitender Mittelwert zur Glättung der Zeitreihen für eine übersichtliche Darstellung

## Verwendete Ressourcen

- **Messdaten:** `volume_flow_data.csv` (CSV-Datei mit Zeitstempeln und Volumenstrom in m³/h)  
- **Datenblatt:** `datenblatt.xls` (Excel-Datei mit Pumpenkennlinien: Förderhöhe und Leistungsbedarf in Abhängigkeit des Volumenstroms)

## Genutzte Werkzeuge und Bibliotheken

Die Programmierung erfolgte vollständig in Python mit folgenden Bibliotheken:
- `pandas` – für Datenverarbeitung und Zeitreihenanalyse  
- `numpy` – für mathematische Operationen  
- `matplotlib` & `seaborn` – für die Erstellung von Diagrammen und statistischen Plots  
- `scipy.interpolate` – für die Interpolation der Pumpenkennlinien

## Ergebnisse

- **Gesamter Energieeinsatz der Pumpe** wurde in kWh berechnet  
- **Durchschnittlicher Wirkungsgrad** der Pumpe wurde in Prozent ermittelt  
- **Verlustleistung** (nicht in hydraulische Arbeit umgesetzte Energie) wurde quantifiziert  
- **Visualisierungen** ermöglichten eine anschauliche Bewertung des Systemverhaltens

## Fazit

Die durchgeführte Analyse zeigt, wie durch Kombination realer Betriebsdaten mit Herstellerangaben ein fundiertes Verständnis für das energetische Verhalten einer technischen Anlage gewonnen werden kann. Insbesondere der Wirkungsgrad und die Leistungsverluste geben Hinweise auf mögliche Optimierungspotenziale im Betrieb der Pumpe.

