# Roesner-Michelle_IU14078032_DLMDWWDE02
Roesner-Michelle_IU14078032_DLMDWWDE02_P2
# Echtzeit-Datenpipeline mit Azure Databricks

## 🔍 Projektübersicht

In diesem Projekt wurde eine cloudbasierte Streaming-Datenpipeline in Microsoft Azure Databricks umgesetzt. Ziel ist die Simulation, Aggregation und Auswertung von Sensordaten in Echtzeit – inklusive Filterung, Klassifikation und Visualisierung.

## 🎯 Zielsetzung

Die Anwendung bildet eine modulare Echtzeit-Architektur ab, um kontinuierlich erzeugte Temperaturdaten von simulierten Sensoren zu analysieren. Die Datenpipeline wurde in mehreren, klar abgegrenzten Schritten implementiert.

## ⚙️ Umgesetzte Verarbeitungsschritte

1. **Datengenerierung**  
   Erzeugung eines kontinuierlichen Datenstroms mit Zeitstempel, Sensor-ID und Temperaturwert.

2. **Aggregation**  
   Berechnung der durchschnittlichen Temperatur pro Sensor in 1-Minuten-Zeitfenstern.

3. **Filterung kritischer Werte**  
   Herausfiltern aller Temperaturwerte über 28 °C zur Anomalieerkennung.

4. **Klassifikation**  
   Einteilung der Messwerte in Statusklassen: „niedrig“, „normal“ und „kritisch“.

5. **Visualisierung**  
   Tabellarische Auswertung (Anzahl, Durchschnitt, Maximaltemperatur je Status)  
   + Trendanalyse über Temperaturverläufe pro Sensor.

6. **Persistente Speicherung (nicht umgesetzt)**  
   Aufgrund fehlender Schreibrechte in der Azure-Umgebung konnte die Ausgabe in Parquet-Dateien nur konzeptionell vorbereitet werden.

## Tools & Technologien

- Databricks (Azure)
- PySpark / Structured Streaming
- SQL (Spark)
- In-Memory-Views
- GitHub für Versionierung

## Walkthrough-Video

➡️ [Hier klicken, um das Projektvideo anzusehen](#) *(Link bitte hier einfügen)*

## Architekturdiagramm

Das konzeptionelle Architekturdiagramm befindet sich im Ordner `images/`.

---

## Ordnerstruktur
notebooks/ # Exportiertes Databricks-Notebook
images/ # PNG-Dateien (Architektur, Screenshots)
video/ # Walkthrough-Video oder Link
README.md # Dieses Dokument

## Hinweis

Die Umsetzung erfolgt im Rahmen des Moduls „Data Engineering“ an der IU. Aufgrund von Systemeinschränkungen / fehlender Speicherzugriff in der Cloud-Umgebung wurden Teile der Architektur angepasst.
