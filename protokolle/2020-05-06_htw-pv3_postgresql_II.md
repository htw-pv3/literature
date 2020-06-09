# 2020-05-06 14:00 - 15:30 Wetterdatenverarbeitung mit PostgreSQL II -----#5

# Auswertung Abgaben Aufgaben #1 und #2

## Bewertungen
* Kriterien
* Veröffentlichung der Bewertungen? 
* Zeigen von Best- and Worst-Practices?

## Dokumentation
* Beispiel Aufgabe 1:
* Beschreiben und Dokumentieren Sie kurz ihr Vorgehen.
* Wie kann das Programm klassifiziert werden? Welche Lizenz hat das Programm? Welche Version(en) gibt es? Auf welchen OS läuft es? Wo kann ich es downloaden? Wie groß ist das Programm? Warum werde ich es verwenden? 
* Was bedeutet "Dokumentation des Vorgehens"

## Abgaben Datei
* Geeignete Dateiformate: PDF, + .bib + .sql + .py
* Dateibenennung: 2020-05-06_HTW-PV3_Aufgabe1_Hulk.pdf
* Datum ISO 8601 https://xkcd.com/1179/
* Wie sieht eine perfekte Abgabe aus? 
* Wie werden verschiedene Formate abgegeben?
* Wie Dokumentiere ich Zusammenarbeit?


## Kommentare aus den den Abgaben 1:
* {GitHub: warum das zusätzlich zu gitSCM?}, Client!
* Lizenz: Online Plattform, kürzlich gekauft von Microsoft
* Warum werde ich es verwenden: zur Erstellung und Verwendung eines gemeinsamen Git Repositories, ggf. zur Veröffentlichung der Arbeit
* .tex vs. .bib
* Validierung von Dateien
* Programmgröße={ 563MB},
* file_size={} Installer
* progamm_size={} Installiert


## Kommentare aus den den Abgaben 2:
* Alles wurde erfolgreich installiert
* __MACOSX in ZIP
* Folie 5 "merge.tool" nicht nachvollziehbar
* PUTTY für SSH Key nicht erfolgreich (!) - ssh-key angelegt, aber konnte nicht zu GitHub hinzugefügt werden, weil nicht im OpenSSH-Format(!)
* Folie 28 nicht nachvollziehbar (conda install jupyter)
* Git - Keine Probleme bei der Installation. Schritte aus den Folien durchgeführt
* Anaconda - Keine Probleme bei der Installation. Installation erfolgte in das Verzeichnis „C:\Anaconda“ ohne Leerstellen, so dass hoffentlich keine Fehler beim Ausführen enstehen. Schritte aus den Folien ausprobiert. 
* Polysun und PVsol hab ich noch nicht installiert, da mir noch die Lizenzschlüssel fehlen 
* Ist bei mir schon Installiert und bin damit sehr zufrieden. Installation wahr damals auch sehr einfach.
* Leider konnte ich aufgrund meines Speicherplatzes meine Installationen nicht vollenden. Ich habe mein Speicher angepasst und Sachen die ich nicht mehr brauche gelöscht und es hat leider immer noch nicht gereicht. Als beweis habe ich ihnen Screenshots oben beigefügt. Ich hoffe ich bekomme wegen diesem Problem keine Minus Punkte.
* Internetexplorer in der Taskleiste, kann ich mir das erlauben ;)
* PVSol - benötigt Windoof bzw. eine VM. Wurde deshalb nicht installiert.
* DIE ANWENDUNGEN.pdf - genau mein Humor
* Python/Conda activate BASE
* Postgresql - Ich habe das Programm installiert. Das Programm mochte volle Zugriff auf meiner Festplatte. Das sehe ich sehr skeptisch an. Ich lese mich noch ein und entscheide im Laufe der Woche darüber, ansonsten installiere ich es auf einem anderen Rechner. LH wird uns keine Schadsoftware empfehlen
* Alle Screenshots vs. "kurze Dokumentation"
* Kann ich Hardware voraussetzen? -> Augabe 1 Recherche und Vorbereitung?
* Remodesktop auf die HTW
* Kann ich ein OS voraussetzen? -> Win und/oder Linux ... Sorry Macboys
* Remodesktop auf die HTW
* Spracheinstellungen des OS -> Auf eigene Gefahr


# Finalisierung PV-Software:

* Polysun 11.3
	* 1 pro Person - jeweils nur auf einem Endgerät installieren / gültig bis 30.09.2020
* PVsol Premium 2020-7
	* 1 pro Person - jeweils nur auf einem Endgerät installieren / gültig bis 30.09.2020
* PVsyst 6-8-6
	* 1 für alle - nur auf Dozenten-PC installieren / gültig bis 30.09.2020
	*  Monat Testversion für jeden (3.6.2020 - 3.7.2020)!!!


# Ausführen der Datenbank-Skripte
1. Setup
2. Iport
3. Berechnungen (JOIN)
4. Export


# Wetterdatenvisualisierung mit Python in Jupyter Notebook (Jupy)
* Anlegen einer Python-Environment
* Starten von Jupy
* Ausführen und Datenanalysen


# Protokoll:

## SQL-Querries:
    
* Alle Skripte funkionieren auch ohne korrigierte Metadaten
* .csv - Dateien nicht öffnen
    
    1.  Servergruppe erstellen: 
		1. Servers -> create -> Server Group bspw. HTW-PV3
		2. Server erstellen: HTW-PV3 -> create -> Server
             - Reiter General: Name == PostgresSQL 12
		    - Reiter Connection: Host name/address == localhost
	    	- save
	2. Skript 1 ausführen: User anlegen
		1. postgres Datenbank auswählen
		2. rechtsklick postgres (Datenbank) -> Querry Tool -> Skript einfügen -> run
		3. rechtsklick Databases  -> refresh
		4. rechtsklick PostgresSQL 12 (server) -> diconnect database
		5. rechtsklick postgres (Datenbank) -> properties -> Reiter Connection -> Username = sonnja -> safe
		6. rechtsklick PostgresSQL 12 (server) -> connect Server -> password == sonnja
	2. Skript 2 ausführen: Datenbank "sonnja_db" erstellen
		1. rechtsklick Databases -> create  -> Database>Create und Einstellugen gem. Skript 2 (Body) vornehmen
	3. Skript 3: erstellen von Schema Pv3: 
		1. rechtsklick sonnja_db (Datenbank) -> Query Tool -> Skript einfügen -> run
		2. Skript 3 reinkopieren>Run
		3. Refresh mit Rechtsklick auf SChemas
	4. Skript 4: erstellen der DB_log (Logging option)
        - Achtung: Skript 4 müssen die Metadaten noch angepasst werden
			- von Kilian geupdated https://github.com/htw-pv3/weather-data/blob/MyMetaData/helfenbein_kilian/postgresql/htw_pv3_postgresql_04_function_db_log.sql
	5. rechtsklick sonnja_db (Datenbank) -> Query Tool ->Skript einfügen -> run
	6. Skript 4:
	    - einfach ausführen (was muss ausgewählt sein?) -> 
        - Erstellt eine Funktion, die in verschiedenen nachfolgenden Skripten verwendet wird, um Datenbank-Veränderungen verpflegen zu können.

### Datenabschnitt ansehen: Rechtsklick auf einleuchtend_wrdata_2015_wr1>ViewData
* die Abschnitte werden nur angezeigt und nicht verändert. Keine Ansgst bei Abfragen.
* Im Query Editor kann anschließedn die Vorschirft angepasst werden, welche Datenabschnitte man sich ansieht.
* Beispiel: zeigt 500 Einträge wo u_pv und i_pv "Null" ist
    - SELECT*
     FROM pv3.einleuchtend_wrdata_2015_wr1
	WHERE u_pv = 0 AND i_pv = 0ORDER BY "Timestamp"
	ASC LIMIT 500
* Für weitere Abfragen siehe: SQL_cheat_sheats und Abschnitt "timestamp-Abfragen im yopad-2
		
### Fragestellung: Wo sind die Lücken in den Wechselrichter-Daten?
* siehe: Skript 5_data_join
	
### Fehlernachrichten in pgAdimn 4 können sich auf die vorherige oder darauffolgende Zeile beziehen.

# Ziel für heute: alle Skripte bis Skript 5 ausgeführt haben(!)
* db_log (Logbuch) exportieren um nachzuweisen, dass wir eine Aufgabe erledigt haben
	
	
##### Falls eine Aufgabenstellung unklar ist und mehr als eine Stunde dauert, Email an LH schreiben
##### Fragen zu Aufgaben in das zweite pad: https://yopad.eu/p/HTW-PV3-2020-2

