# 2020-04-22 14:00 - 17:15

##14:00 Feedback zur Aufgabe #1


Was habt ihr gelernt?

- Gar nicht so einfach! Lizenzen und RechteinhaberInnen
- Was ist der unterschied zwischen url_date und timestamp?
	- timestamp: letzte bearbeitung
	- url-date: 
- Welche Daten notwendig sind, ist schwer einzuschätzen.
- Wie verwenden wir das jetzt?
	- für eine gemeinsame Literaturdatenbank
	- als Vorbereitung für das Zitieren in unserer Masterarbeit

- Bleibt das jetzt so einfach? (Spoiler: nein)

- Falls Textdateien im richtigen Format (als .txt erstellt, Dateiendung in .bib geändert) sind -> Einlesen in JabRef problemlos

- Bitte mehr Transparenz/Hinweise auf extra Anforderungen :)


Wir analisyeren heute git/GitHub, Anaconda (Phython) und PyCharm (zur bearbeitung von Python)

## 14:15 Software-Session

- Rundgang durch die Programme (git, Anaconda und PyCharm)
- Setup und Einstellungen
- Tests und MWE (Minimal Working Example)
- Let's encrypt! (verschlüsseln von privaten Dateien z.B. mit der Software "VeraCrypt")


### git

(Software - Link zu dem git-Programm (mit command line): siehe unten # Aufgabe 2)

git ist ein Versionsverwaltungssystem (source control management system) und wird dafür verwendet, verschiedene Versionen und Bearbeitungsstände von Software und Textdateien zuverwalten.

git sollte nur verwendet werden, um Textdateien zu verwalten, nicht für binäre Dateien. Grund: git erkennt gut Änderungen an Textdateien und muss nicht die gesamte Datei speichern/verwalten, sondern nur die Änderungen jeder Version. Sollte bei einem Bild oder Video ein Pixel verändert werden, so behandelt git diese Datei als neue Datei und muss diese in ihrer Gesamtheit verwalten.


#### github

(Webspace-Account) Konfiguration

- Konfiguration unserer Gruppe, Gruppenname: htw-pv3 
- neues Repository mit Namen "literature"
- erstellt mit Repository Eigenschaften: öffentlich, mit readme, add.gitignore: Python, License: cc 0
- vollständige URL: https://github.com/htw-pv3/literature
- repo clonen (https oder ssh)
- https fragt username und pw ab [kurzfristig einfacher]
- ssh benötigt ssh-key (public ssh-key muss im github account hinterlegt werden) [langfristig einfacher]
- github handles (Gruppenmitglieder - Einladung manuell annehmen unter: github.com/htw-pv3): 


Repository  in den lokalen Ordner "c:/git/github/htw-pv2" einbinden mit git bash (Admin) über den Befehl: git "clone https://github.com/htw-pv3/literature.git"


### Anaconda

Anaconda: Distribution management (Python, Python-IDEs, etc.)

- Anaconda mit Phython 3.7 herunterladen und unter C:/Anaconda3 installieren um die leerzeichnen von Folder von Windows (unter C:/Programme oder C:\Program Files (x86) ) zu verhindern.

- Leerzeichen in Programmpfaden verursachen Fehler in diversen Prgrammierumgebungen, daher tunlichst vermeiden und statt eines Lerrzeichens zum Beipsiel einen Unterstrich verwenden. Beispiel "d:\Programme_RE\Solar\"

- Falls anaconda nicht richtig installiert werden konnte (cmd: anaconda --version liefert einen Fehler), Umgebungsvariablen von Windows bearbeiten: Systemeigenschaften>Erweitert>Umgebungsvariablen>Systemvariablen>Path>bearbeiten>neu>C:\Anaconda3 und c:\Anaconda3\Scripts\

#### Environments

(ein virtueller Raum, der Python oder eine andere Sprache kann)

- Packages sind die kleinen spezialisierten Apps, die das Ganze interessant machen, bspw. PV-Simulation
- Namenskonventionen helfen dabei, diese wiederzuverwenden
- werden schnell sehr groß
- Beispiel für die Anwendung: Verschiedene Versionen und Pakete können in ihren Blasen (environment) unabhängig von den Versionen in den anderen Blasen funktionieren. Das Hilft dabei Kompatibiltätsprobleme zu reduzieren.

TIPP: Werden Environments hinzugefügt, dann muss das Fenster "Eingabeaufforderung" (in der Windows-Suche eingeben) vorerst als Administrator ausgeführt werden.

#### Conda
 
(bereits in anaconda integriert, muss nicht separat geladen werden): 

- Paketmanager für den Zugriff auf diverse Pakete, die einen ermächtigen mathematische Funktionen etc. zu benutzen .. bis hin zum "Fliegen" - neben Conda werden wir zwei weitere Paketmanager nutzen: conda-forge und pip
- Pakete: Conda enthält einige Pakete von Vornherein, zwei wichtige sind "pandas" und "jupyter"

pvlib für PV-Simulationen

Pakete installieren: In der Eingabeaufforderung wechselt man in den Pfad von Conda und tippt bspw. "conda install pandas" ein


### Pycharm IDE

integriertet Entwicklungsumgebung für Python (compiler und Editor)

Editor: Umgebung, zur Bearbeitung von Source Code, mit verschiedenen Zusatzfunktionen and Features

Compiler: Programme, die aus die die Programmiersprache (hier Python) in Maschinencode übersetzt

Empfehlung: drei "getting started" videos ansehen (Help in der Menüleiste)

GUI (Aussehen der Software): Darcula -> schwarz 

neues Projekt anlegen, checkbox: existing interpreter verwenden (gleichbedeutend mit zuvor angelegten python-Environment)

zur Ausführung des Codes ggf. vorher projekt-interpreter initialisieren (settings>project python>interpreter...)


--> Ziel: arbeiten mit dem Paket "Pvlib Python" https://github.com/pvlib/pvlib-python


Datei-Verschlüsselung mit VeraCrypt
VeraCrypt Software ist eine Verschlüsselungstechnologie um Daten zu Schützen
zur Verschlüsselung werden besondere Algorithmen verwendet, diese zeichnen sich dadurch aus, dass der Entschlüsselungs-Vorgang viel komplizierter ist, als der Verschlüsselung. 
Empfehlung zur Auswahl:

AES und Twofish

Hash Algorithmes SHA-512 hat heutzutage die Hochste Verschlüsselung


Passwortsicherheit  (wirklich sehenswerte Links):

How to choose a password https://www.youtube.com/watch?v=3NjQ9b3pgIg

How Password Managers work https://www.youtube.com/watch?v=w68BBPDAWr8

-> Empfehlung: Bitwarden / KeePass (Freeware/Open-source) / KeeWeb / Dashlane


### Aufgaben
☐ ☑ ☒

☑ Versionsnummern für PVSol und Polysun mitteilen [LH]

☑ alle ins Github-Team einladen [LH]

☑ Zugangsrechte für das repo überprüfen[LH]

Ups, hab nur Leserechte erteilt. Mein Fehler!

☑ Checkboxen checken



### Aufgabe #2: Installation und Setup @29.04.2020 um 14:00

Installieren Sie die benötigten Programme auf Ihrem Computer und machen sich mit dem Start und der Anwendung vertraut. Dokumentieren Sie die Installationen (Ein Screenshot pro Programm reicht, wenn daraus vorgeht, dass es funktioniert/richtig ist). Dokumentation als .pdf abgeben.

PostgreSQL 12.2 - https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

Ohne den "StackBuilder" (Der nervt)

Was habt ihr bei "Select the locale..." ausgewählt? [Default locale]? ja / German, Germany

Zusätzlich PostGIS - http://download.osgeo.org/postgis/windows/pg12/

über homebrew (macOS) - https://postgis.net/install/

bzw https://postgresapp.com/de/ PostgreSQL incl. PostGIS (macOS)

QGIS 3.10 (LTS) - https://qgis.org/de/site/forusers/download.html

nicht 3.12 geht auch, aber lieber LTS

Notepad++ 7.8.5 (oder ähnlicher Editor) - https://notepad-plus-plus.org/downloads/

textmate (macOS) - https://macromates.com/ 

git / gitSCM* 2.26  - https://git-scm.com/ sollte unter C:/ installiert werden?

notepad++ als editor einstellen oder im nachhinein umstellen (siehe Folien git)

optional (!): Putty Installieren https://www.putty.org/ und die SSH-Schlüssel einrichten (puttygen.exe, pageant.exe, plink.exe, putty.exe)

Hat hier jemand ne gute Erklärung zu? -> siehe Verschlüsselung.


Anaconda* Py37 (Python) - https://www.anaconda.com/distribution/

Windows: Installation mit Rechtsklick und "Als Administrator ausführen" beginnen

Windows: Installation unter C:/Anaconda3, da kein Leerzeichen im Dateipfad enthalten sein darf. Zuwiderhandlung kann mit schwerauffindbaren Fehlern bestraft werden. Daher nochmal:  Die Software NICHT unter C:/Programme/Anaconda3! installieren(!) --> Diese Information ist einen Bonus-Punkt wert.

PyCharm*  2020-1 (Community) - https://www.jetbrains.com/academy/ https://www.youtube.com/watch?v=5rSBPGGLkW0

https://www.jetbrains.com/pycharm/download/   pycharm-community-2020.1

Es gibt auch ne Version direkt für Anaconda https://www.jetbrains.com/pycharm/promo/anaconda/

JabRef﻿ 5.0- http://www.jabref.org/

für Custom Entry Types (z.B. "Software") https://docs.jabref.org/setup/customentrytypes

Optionen->Allgemeine Felder:

Allgemein:crossref;tag;keywords;file;doi;url;comment;owner;timestamp

Zusammenfassung:abstract

Überprüfung:download_url;review;license;license_url;copyright_owner;openness


Polysun 11.3 - https://www.velasolaris.com/downloads/

noch nicht runterladen, da zu verwendende Versionen noch nicht fest stehen

Lizenzschlüssel gibt es per mail (erreichen uns im Laufe der Woche, nur auf einem Endgerät installieren, gültig bis 30.09.2020)

PVsol Premium 2020-7- https://valentin-software.com/downloads/

Lizenzschlüssel gibt es per mail (erreichen uns im Laufe der Woche, nur auf einem Endgerät installieren, gültig bis 30.09.2020)

10. VeraCrypt 1.24

Optional


* Dokumentation für Installation und Setup vorhanden

Anmerkungen zu Verschlüsselung:

Das ist schon (relativ) hohes Nerd-Level, aber eigentlich ganz einfach. Ziel: Dadurch muss in git nicht username und pw eingegeben werden, das wird schnell müßig und führt dazu, ein zu einfaches Passwort zu verwenden.

https://sachinsharm.wordpress.com/2015/05/04/pageant-ssh-agent-for-windows/

https://stackoverflow.com/questions/35110079/git-bash-and-pageant-are-not-using-keys

Erstelle deinen SSH-Schlüssel (private und public key) mit puttygen (wird mit PuTTY installiert), setzte ein sicheres PW

Hinterlege den öffentlichen SSH-Schlüssel "public key" bei GitHub

Öffne SSH-Schlüssel mit pageant (verwende das PW)

Leite den geöffneten Schlüssel an git weiter

Literatur:

https://de.wikipedia.org/wiki/Public-Key-Authentifizierung

https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem

 https://tools.ietf.org/html/rfc4819 



Fehlersuche hat in der Installationsanleitung nix zu suchen, da kommen nur die Ergebnisse rein:

Mit der Windows Kommandozeile (bzw. PowerShell) hat das erstellen von envs bei mir nicht funktioniert

HTTP Error ja bei mir auch

CondaHTTPError: HTTP 000 CONNECTION FAILED for url <https://repo.anaconda.com/pkgs/main/win-64/current_repodata.json>

Elapsed: -

An HTTP error occurred when trying to retrieve this URL.

Mit der Anaconda PowerShell hat es problemlos funktioniert <- das Problem umgehen ist nicht das Problem lösen ;)


Das sind Zusätze, die haben in der Install garnix zu suchen!

pip install xlrd

sonst gibts nen Error in PyCharm bei Pandas Befehlen zu Excel

Pvlib

conda install -c pvlib pvlib

A collection of various different notebook extensions for Jupyter:

conda install -c conda-forge jupyter_contrib_nbextensions

Mehr Funktionalitäten für das Jupyter Notebook, wie z.B. autocomplete, code folding etc.

https://jupyter-contrib-nbextensions.readthedocs.io/en/latest/install.html



### Aufgaben
☐ ☑ ☒
☐ Protokolle aufbereiten und ausarbeiten [ALL] -> Umwandeln in Markdown (MD) und ablage auf GitHub!

☑ 1. 2020-04-06 [LH] 

☒ 2. 2020-04-15 [LH]

☐ 3. 

☐ Remote-Zugriff auf HTW-Rechner

☐ VPN

☐ Remotedesktopverbindung

Schreibweise Remote Desktop: f1-inf-f226-XX.intern.f1.htw-berlin.de

XX durch PC Nummer ersetzen

Username: login\s0XXXXXX

☐ Erstellen der 3. und 4. Aufgabe
☐ Tutorial Install & Setup Postgres, Postgis, QGIS




1. branch
2. pushen
3. pull-request

branch:
feature/add-proticol-3

commit message:

Add first version of file #11