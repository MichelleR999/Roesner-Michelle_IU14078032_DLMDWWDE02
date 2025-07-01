# Roesner-Michelle_IU14078032_DLMDWWDE02
Roesner-Michelle_IU14078032_DLMDWWDE02_P2
# Echtzeit-Datenpipeline mit Azure Databricks

## Projektübersicht

In diesem Projekt wurde eine cloudbasierte Streaming-Datenpipeline in Microsoft Azure Databricks umgesetzt. Ziel ist die Simulation, Aggregation und Auswertung von Sensordaten in Echtzeit inklusive Filterung, Klassifikation und Visualisierung.

## Umgesetzte Verarbeitungsschritte

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

6. **Persistente Speicherung (nicht umgesetzt)**  
   Aufgrund fehlender Schreibrechte in der Azure-Umgebung konnte die Ausgabe in Parquet-Dateien nur konzeptionell vorbereitet werden.

7. **Aggregation für Trend**
   Der Temperaturverlauf der Senoren werden als Trend-Diagramm abgebildet.

## Tools & Technologien

- Microsoft Azure Databricks 
- PySpark / Structured Streaming
- SQL (Spark)
- In-Memory-Views
- GitHub für Versionierung

## Hinweis

Ursprünglich war geplant das Projekt lokal umzusetzten. Aufgrund meiner begrenzten Systemressourcen (nur 4 GB RAM) war das jedoch nicht umsetzbar. Stattdessen habe ich das Projekt in Azure Databricks realisiert. Über meinen Arbeitgeber habe ich einen Databricks-Zugang. Dort war die Umsetzung technisch möglich, allerdings mit Einschränkungen. Schreibrechte auf persistente Speicherorte sind nicht vorhanden und der Zugriff auf externe Containerlösungen sind ebenfalls limitiert.
Deshalb wurde die Pipeline vollständig innerhaln von Databricks modular aufgebaut. Dabei sind alle Schritte logisch getrennt und inerhalb eines Notebooks über In-Memory-View hinterlegt.
