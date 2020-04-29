2020-04-15 14:00 - 17:30

14:00 Vorstellungsrunde Studierende

14:30 
Thema: Daten 
Semantisches Feld
Definition: Datum/Daten ->elektronisch gespeicherte Zeichen/Angaben/Information
Information alleine reicht aber nicht aus
Wir werden mit minutenwerte für 1 jahr arbeiten (Klimadaten)
Die Speichermedium die wir heute benutzen sind Flash und Cloud und wir werden sie anschauen.
Kategoriesierung der Daten: nach der Struktur (Unstrukturierte, Semistrukturierte Daten und Strukturierte Daten), Sonstige Kat.: Transiente(z.B. Datenlogger --> kurzgespeichert und übermittelt), Ein-/ Ausgabedaten, Stammdaten z.B. Kundendaten Geburtsdatum (können sich ändern aber normalerweise nicht)..., Realtime z.B. Aktuell Stand (Messung), Neartime z.B. BVG Anzeige (nicht ganz realtime), Historisch z.B Zensus, Originär (Messwerte), Abgeleitet (Berechnung von Originäre Daten z.B Durchnitt)
Der Begriff "Realdaten" sollte nicht verwendet werden, da dieser Datentyp nicht existiert. Der Grund: jede Messung ist fehlerbehaftet.
Strukturierte Daten werden durch die Definition der "Struktur" Spaltenbezeichnung geschafft, i.d.R. werden zuerst Spalten, Dateitypen, Key und Value definiert
Strukturierten Daten sind grundlegend für Datenbank
endogene und exogene Daten
endogene:liegen innerhalb des Models
exogene:kommen als Input-Daten

Metadaten: beschreiben die Elemente eines Datensatzes vollständig und geben Informationen über Datentypen und Einheiten der einzelnen Elemente.

Datenbearbeitgun in a "nut-shell"
Folie 9 im Skript zeigt den grundsätzlichen Ablauf der Datenbearbeitung, wie wir ihn gehen werden. Weiß-hinterlegte Felder sind Standard (Teil der PV-Modellierung), grau hinterlegte sind Teil der Wissenschaftlichen/Ingenieurtechnischen Arbeit. Das eigentliche Ziel der Forschung sollte sein, die Inhalte mundgerecht aufzuarbeiten (grau-hinterlegte Felder). Zum Beispiel mit geploteten Diagrammen und einer Ergebnisanalyse.

Fragen: Ab welchem Prozentwert spricht man von einer schlechten Verschattung?

Forschungsfrage - nachgeführte PV-Anlagen: Welchen Ertrag würde die Dachanlage auf der HTW bei verschiedenen nachgeführten Systemen (einachsig horizontal, einachsig vertikal) liefern?

Feststellung: der Einfluss des Breitengrades auf das nachgeführte System ist gravierender als der Längengrad.
Frage: Grafik für nachgeführte PV-Anlagen in Abhängigkeit der geografischen Höhe.

Forschungsfragen auf Seite 12 - Zielstellungen für dieses Modul… Die obersten vier werden zu beantworten sein (Auszug):

    Betriebs- und Ertragsverhalten der Modultechnologien

    Wechselrichter-Performance und Wikrunsgrad bei Betrieb mit unterschiedlichen Modultechnologien

    Einfluss der Verwendung von verscheidenen Wetterdatensätze (wir werden diverse verwenden; HTW-Wetter 2015, open_FRED, synthetische Wetterdaten)

    Vergleich von unterschiedlichen Berechnungsmodellen.


Zu Wetterdaten und PV-Messung/Simualtion: Was habe ich? Macht es Sinn das zu vergleichen? Das ist eigentlich das, was ihr draufhaben sollt.

Lücken in Daten sind behutsam zu behandeln. Das Auffüllen solcher insbesondere für den Erhalt der Jahreslänge notwendig. Wie aufgefüllt wird (Lineare Näherung, Verwendung des Vortages, etc.), muss im Einzelfall entschieden werden.



    ☐ Softwareinstallationen vorbereiten [ALL] 

ACHTUNG: Installiert nicht einfach alles! Bei einigen Installationen müssen bestimmte Feinheiten beachtet werden. Diese werden wir gemeinsam durchgehen. Was beduetet "vorbereiten"? -> Benutzt GoogleSuchmaschine um möglichst viel über das Programm zu erfahren: Wie kann das Programm klassifiziert werden? Welche Lizenz hat das Programm? Welche Version(en) gibt es? Auf welchen OS läuft es? Wo kann ich es downloaden? Wie groß ist das Programm? Warum werde ich es verwenden? .... 

    PostgreSQL

    QGIS

    Notepad++ (oder ähnlicher Editor)

    git / gitSCM

    Anaconda (Python)

    Pycharm (Community)

    GitHub (Trickfrage)


Aufgabe #1: Recherchieren, Dokumentieren und Klassifizieren der verwendeten Software @22.04.2020 um 14:00

Erstellen Sie für jedes Programm einen BibTeX-Eintrag. 
Entscheiden Sie welche Einträge notwendig sind und füllen Sie diese aus.

(Hinweis: BibTeX kann mit jedem Texteditor erstellt werden, aber praktischerweise endet es mit .bib)

Beispiel:

        @Software{YEd,

      title           = {yEd},

      version         = {3.18.2},

      author          = {{yWorks GmbH}},

      url             = {https://www.yworks.com/products/yed},

      urldate         = {2019-03-05},

      platform        = {unabhängig},

      kategorie       = {Visualisierungsprogramm},

      comment         = {https://de.wikipedia.org/wiki/YEd},

      copyright_owner = {© 2019 yWorks},

      file            = {:DATA/Software/yEd/yEd-3.18.2_with-JRE10_64-bit_setup.exe:exe},

      license         = {yEd Software License Agreement},

      license_url     = {https://www.yworks.com/company/legal/terms-of-use},

      openess         = {Freeware},

      owner           = {Ludwig Hülk},

      tag             = {software;},

      timestamp       = {2019-03-05},

    }


    PostgreSQL

    QGIS -> Netzwerk oder Standalone?

    Notepad++ (oder ähnlicher Editor)

    git / gitSCM

    Anaconda (Python)

    PyCharm (Community)

    JabRef﻿

    GitHub -> Account anlegen