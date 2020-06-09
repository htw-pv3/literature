# Daten
__2020-04-15 14:00 - 17:30__

- 14:00 Vorstellungsrunde Studierende

- 14:30 Thema: Daten 

## Semantisches Feld
### Definition:

Datum/Daten -> elektronisch gespeicherte Zeichen/Angaben/Information

- Information alleine reicht aber nicht aus
- Wir werden mit minutenwerte für 1 jahr arbeiten (Klimadaten)
- Die Speichermedium die wir heute benutzen sind Flash und Cloud und wir werden sie anschauen.
### Kategoriesierung der Daten:
- nach der Struktur:
	- Unstrukturierte
	- Semistrukturierte Daten
	- Strukturierte Daten)
- Sonstige Kat.: 
	- Transiente(z.B. Datenlogger --> kurzgespeichert und übermittelt)
	- Ein-/ Ausgabedaten, Stammdaten z.B. Kundendaten Geburtsdatum (können sich ändern aber normalerweise nicht)....
	- Realtime z.B. Aktuell Stand (Messung)
	- Neartime z.B. BVG Anzeige (nicht ganz realtime)
	- Historisch z.B Zensus, Originär (Messwerte)
	- Abgeleitet (Berechnung von Originäre Daten z.B Durchnitt)
	
> Der Begriff "Realdaten" sollte nicht verwendet werden, da dieser Datentyp nicht existiert. Der Grund: jede Messung ist fehlerbehaftet.

Strukturierte Daten werden durch die Definition der "Struktur" Spaltenbezeichnung geschafft, i.d.R. werden zuerst __Spalten__, __Dateitypen__, __Key__ und __Value__ definiert.

- Strukturierten Daten sind grundlegend für Datenbank
- endogene und exogene Daten
	- endogene:liegen innerhalb des Models
	- exogene:kommen als Input-Daten

__Metadaten:__
Sie beschreiben die Elemente eines Datensatzes vollständig und geben Informationen über Datentypen und Einheiten der einzelnen Elemente.

### Datenbearbeitung in a "nut-shell"

- Folie 9 im Skript zeigt den grundsätzlichen Ablauf der Datenbearbeitung, wie wir ihn gehen werden.
- Weiß-hinterlegte Felder sind Standard (Teil der PV-Modellierung), grau hinterlegte sind Teil der Wissenschaftlichen/Ingenieurtechnischen Arbeit
- Das eigentliche Ziel der Forschung sollte sein, die Inhalte mundgerecht aufzuarbeiten (grau-hinterlegte Felder). Zum Beispiel mit geploteten Diagrammen und einer Ergebnisanalyse.

__Frage:__ Ab welchem Prozentwert spricht man von einer schlechten Verschattung?

Forschungsfrage - nachgeführte PV-Anlagen: Welchen Ertrag würde die Dachanlage auf der HTW bei verschiedenen nachgeführten Systemen (einachsig horizontal, einachsig vertikal) liefern?

Feststellung: der Einfluss des Breitengrades auf das nachgeführte System ist gravierender als der Längengrad.

__Frage:__ Grafik für nachgeführte PV-Anlagen in Abhängigkeit der geografischen Höhe.

Forschungsfragen auf Seite 12 - Zielstellungen für dieses Modul.
Die obersten vier werden zu beantworten sein (Auszug):

- Betriebs- und Ertragsverhalten der Modultechnologien

- Wechselrichter-Performance und Wikrunsgrad bei Betrieb mit unterschiedlichen Modultechnologien

- Einfluss der Verwendung von verscheidenen Wetterdatensätze (wir werden diverse verwenden; HTW-Wetter 2015, open_FRED, synthetische Wetterdaten)

- Vergleich von unterschiedlichen Berechnungsmodellen.


Zu Wetterdaten und PV-Messung/Simualtion: Was habe ich? Macht es Sinn das zu vergleichen? Das ist eigentlich das, was ihr draufhaben sollt.

__Lücken:__
Lücken in Daten sind behutsam zu behandeln. Das Auffüllen solcher insbesondere für den Erhalt der Jahreslänge notwendig. Wie aufgefüllt wird (Lineare Näherung, Verwendung des Vortages, etc.), muss im Einzelfall entschieden werden.

