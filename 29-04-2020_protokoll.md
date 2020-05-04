# 2020-04-29 14:00 - 15:30 Wetterdatenaufbereitung mit PostgreSQL

## Feedback zur Übung / Generell:

    * Relativ wenig Antworten  

    * Werden die nächsten Tage bewertet  

    

## Fragen zu git und GitHub:
    
    *Wie kann ich einen Pull Request über git scm in den Master starten?* Hab das jetzt über GitHub gemacht. [Link](https://github.com/htw-pv3/literature/pull/9) 
	
    ->Die Pull Requests (PR) sollten über GitHub erstellt werden. Das geht auch über die GitBash, aber Ziel des PR ist eine Dokumentation und Kommunikation (Review mit 4-Augen-Prinzip)  
    
	
    *Wie sieht der "git workflow" genau aus?*
	
    -> Habe dazu ein kurzes Video-Tutorial gemacht.  
    
	
    *Was ist eine "gute Commit-Message"?*
	
    -> Verb - Nomen - #Ticketnummer
	
	
    *Was ist eine "schlechte Commit-Message"?*
    -> 
    
	
    *Darf ich jemals direkt auf den Master-Branch pushen?*
	
    -> Nein!


## Quick-Walkthrough: Protokolle aufbereiten 

	* issue erstellen lohnt sich ab einer Bearbeungsdauer von 1 bis 2 Stunden
	
	* Hot-Fixes direkt drauf (Rechtschreibfehler, keine substanziellen Veränderungen, selbsterklärende Commit-Messages verwenden!)




# 15:00 Datenbanken

## Vortrag: Wetterdatenaufbereitung


0. Grundlagen Datenbanken und PostgreSQL

    * Database System (DBS) beinhaltet erstens eine Datenbank (DB - Daten auf Platte) und zweitens das Datanbank-Management System (DBMS-Kontroll Software) und den Bearbeiter (DMS)

    * robuster und sicherer Datenspeicher

    * Grundlage und kollaboratives Arbeiten

    * PostgreSQL ist eine Datenbank, sie wird mit einem DBMS (pgAdmin) bearbeitet

    * DB ist verknüpft mit einem Frontend (F) und einem Backend (B). Frontend ist eine Webdarstellung, Backends verwalten die Datenbank (administrieren, Code schreiben mit Python etc.).
	
	  * Das Hin- und Her zwischen F und B sollen wir üben.

    * gutes Passwort anlegen, Benutzer, Gruppen und neue Datenbank erstellen (oedb)

1. Vorhandene Wetterdaten

    * Daten von der Wetterstation der HTW Berlin (1/min)

    * Sonja-Messdaten (5x WR), minütig aufgelöst für das Jahr 2015

    * Zusätzlich vollständige Zeitreihe (525.600), weil in den Daten der HTW Berlin einige Lücken drinne sind. Und: Sonnenauf- und -untergangszeiten für die Aufbereitung

    * erste Untersuchung von Daten / wissenschaftliches Standardverfahren:

      * entpacken

      * Metadaten prüfen (Format: Sommerzeit&Winterzeit, Vollständigkeit)

      * zunächst csv-Dateien in einem Texteditor öffnen (csv: comma separated values)

      * Kopie erstellen! (Datenschutz bsp. Excel versucht autmatisch Datumsformate zu erkennen und ändert diese)

      * Öffnen in MS-Excel zum Explorieren (bspw. mit plot, mittelwert, prüfsumme)

      * Erstellen / Ergänzen der Metadaten (Aufbereitung esseziell wichtig!) und vorbereiten der DB (Tabellenblätter zusammenfassen o.ä.)

         * LH forscht and an öffentlichen Energiedatenbank z.B. OEMetaData: [Link](https://github.com/OpenEnergyPlatform/metadata)

         * Standards und Best-PractiseDatenbanken: frictionlessdata.io, "Tidy Data", FAIR

             * FAIR- findability, accessability, interoperability and reusability 

2. import in Datenbank (Fettgedrucktes sind SQL-Befehle)

    1. Tabellenstruktur erstellen: **CREATE TABLE** SCHEMA.DATEINAME 'Dateipfad/Datei.Endung'.... (Folie 10)

    2. Metadaten editieren (aus dem Standard "OEMetaData v1.4 bspw.: General (Name und Beschreibung, Context (Zusammenhang) und Spatial (örtlich), längere Liste siehe Folie 12)

    3. Einfügen der Zeilen: **COPY ... TO** SCHEMA.DATEINAME....

    *  semistrukturierte Daten im JSON-Format (Folie 13) --> *Prüfungsfragen: Welche Datenstruktur ist das? Welches Datenformat haben wir?*

    *  **COMMENT ON TABLE** SCHEMA.TABELLE - hängt die Metadaten an eine Tabelle

3. Verknüpfen von Tabellen (JOIN)

    * Fragestellungen: Welche Informationen sind in einer Tabelle enthalten und in der anderen nicht?

    * Verknüpfungsmuster: INNER-, LEFT-, FULL-JOIN sind die wichtigsten und RIGHT, NATURAL und CROSS gibt es auch

    * Aufgabe: die richtigen Datenbankbefehle für die Fehler -> Lücken finden und Lücken schließen

    * Programmier-Code siehe Folie 16

    * Beispiel für einen LEFT-JOIN: Zeitreihe mit Wetter verknüpfen

4. Arbeitsschritte

    * siehe Folie 21 und weitere

    * SELECT (welche Spalten) FROM (SCHEMA.TABELLE)  WHERE (Bedingung)
 


# 16:30 Datenbanken II

## pg-Admin4:

	* Web-GUI, die SQL-code ausführt
	
	* Man verbindet sich immer mit einem Datenbank-Server und nicht direkt mit einer Datenbank
    

    * Servergruppe erstellen: Servers -> create -> Server Group bspw. HTW-PV3

    * Server erstellen: HTW-PV3 -> create -> Server

      * Reiter General: Name = PostgresSQL 12

      * Reiter Connection: Host name/address=localhost

      * save

    * Server wählen: PostgresSQL 12

      * postgres-Datenbank nicht anfassen außer die ersten beiden Skripte?!


    * Ein Befehl der ausgeführt wird, wird immer nur auf einer Datenbank ausgeführt

      * Fehlerquelle: Falsche DB ausgewählt und code somit auf falscher DB ausgeführt (Vorsicht!)

    * *Wie führe ich auch einer Datenbank code aus?*

      1. * Server auswählen

      2. * Datenbank auswählen 

      3. * Rechtskick: Querry-tool:

         * Code einfügen und ausführen (F5)

         * Querry wird immer mit Ausgabe "Query returned successfully in XXX msec." abgeschlossen

         * Falls nicht, wurde nichts ausgeführt (All or nothing)

         * **!Wichtig!** In der Regel muss ausgeführter CODE (rechts) im Browser (links) per Rechtsklick>Refresh neugeladen werden.

      4. * Disconnected vom Server
	      
      5. * PostgresSQL 12: Properties ändern

         * user == sonnja

      6. * reconnecten mit Passwort : sonnja


    * *FRAGE: Wie wurde die Datenbank "sonnja_db" hinzugefügt? Steht das in dem Skript 2?*

    * -> Ja (Aber Prinzipiell Rechtsklick auf die Datenbank und neue Datenbank erzeugen)



	* User Management mit Skript (von LH) erstellen:

      * user Rolle erstellen

      * admin Rolle erstellen


# 17:00 Daten-Session

    Welche Daten haben wir?

    METADATEN erstellen

    Datenbankimport versuchen


 [LINK](https://next.rl-institut.de/s/LJXYzBDyC5aDJtz) zu Rohdaten


# Aufgaben
☐ ☑ ☒
   ☐ Metadaten zu den CSV-Dateien "HTW-Wetter" und "Sonja-Messdaten" generieren [ALL]
   ☐ die richtigen Datenbankbefehle für die Fehler -> Lücken finden und Lücken schließen [ALL]
   
   ## 1. SQL-Script
   -- Groups
DROP ROLE IF EXISTS role_read; 
CREATE ROLE role_read WITH NOLOGIN NOSUPERUSER NOCREATEDB NOCREATEROLE INHERIT NOREPLICATION; -- Read only

DROP ROLE IF EXISTS role_user; 
CREATE ROLE role_user WITH NOLOGIN NOSUPERUSER NOCREATEDB NOCREATEROLE INHERIT NOREPLICATION; 
GRANT role_read TO role_user; -- Insert, Update, Delete and Read

DROP ROLE IF EXISTS role_admin; 
CREATE ROLE role_admin WITH NOLOGIN SUPERUSER CREATEDB CREATEROLE REPLICATION; 
GRANT role_user TO role_admin; -- Admin, can create user and databases

-- User
DROP USER IF EXISTS user_read; 
CREATE USER user_read LOGIN PASSWORD 'read' NOSUPERUSER INHERIT NOCREATEDB CREATEROLE REPLICATION;
GRANT role_read TO user_read; -- 2017-04-17 LH

DROP USER IF EXISTS user_write; 
CREATE USER user_write LOGIN PASSWORD 'write' NOSUPERUSER INHERIT NOCREATEDB CREATEROLE REPLICATION; 
GRANT role_user TO user_write; -- 2017-04-17 LH

DROP USER IF EXISTS user_admin; 
CREATE USER user_admin LOGIN PASSWORD 'admin' SUPERUSER INHERIT CREATEDB CREATEROLE REPLICATION; 
GRANT role_admin TO user_admin; -- 2017-04-17 LH

DROP USER IF EXISTS sonnja; 
CREATE USER sonnja LOGIN PASSWORD 'sonnja' SUPERUSER INHERIT CREATEDB CREATEROLE REPLICATION; 
GRANT role_admin TO sonnja; -- 2018-04-25 LH


   


	* Fragen zu Git:

      * -commit auf falschen branch a

      * -wurde außerdem auf anderem branch b überholt

      * -branch a ist aber noch nicht abgeschlossen

      * -[Link](https://github.com/htw-pv3/literature/issues/11)

	  * -guter Lösungsweg?

        
	* Sobald bei git nicht trivale Unterschiede auftauchen (z.B. eine Bearbeitung in der gleichen Zeit), tritt ein sognannter "Merge Conflict" auf.
	* Das sieht zunächst schlimmer aus als es wirklich ist.
	* Das macht kurz Angst, kann aber relativ einfach behoben werden.
	* Ich schau es mir mal in Ruhe an und zeige eine einfache Lösung.
	* Ich verwende das Programm Meld (http://meldmerge.org/) zum vergleichen von Dokumenten (Dif-Tool). Damit ist ein "manuelles Beheben" sehr einfach.

