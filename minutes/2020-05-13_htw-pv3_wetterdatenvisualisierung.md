#2020-05-13 14:00 - 15:30 Wetterdatenvisualisierung mit Python (und Jupyter) -----#6

## Kurzes Feedback und aktueller Stand

- Git ist prinzipiell sehr wichtig und wertgeschätzt.(Einfach ausprobieren, man kann nix damit kaputt machen. Workflow ist dezentralisiert, allse kann repariert werden.)
- Das WIE ist bei der Vermittlung essentiell! Leichteres Heranführen und eventuell bessere Strukturen
- git-commit: so klein wie möglich - atomic commit
- "git sanitary" entwickeln:
    - Meta-Regeln für die git Nutzung (bsp: Sobald ein PR reviewed wurde, wird er vom Reviewer auch gemerged)
- Leichteres Herangehen für verschiedene Vorkenntnisse

- Ich finde den Kurs der Beste dieses Semester aber wünsche mir:
    - Bessere Aufgabenbeschreibung, beschreiben was Schritt zu Schritt gemacht werden soll (Aufgabe 4 war ein Filter und hat leute vom Kurz rausgeschickt, es war schwer zu verstehen was es gemacht werden muss) einmal man verstanden hat (nach sehr viele stunden recherchieren), war die Aufgabe nicht so schwer. 
    - die Größe der Aufgabe eingrenzen. Beispiel: ein esssenzieller commit kann auch "nur" eine Rechtschreibkorrektur sein. Zur Orientierung nochmal: Die Aufgaben sind auf ein bis max. zwei Stunden angelegt(!)
    - Beste Aufgabe Lösung mitteilen um die fehler zu korrigieren, sowieso sind die Aufgaben schon abgegeben und man kriegt keine Note mehr, das ist wichtig um nicht im Kurs mit der Fehler weiter zu gehen.

## Wetterdatenvisualisierung mit Python

__vorab:__ Wiederholung der Einrichtung eines environmnets mit anaconda
Wichtig: zunächst die aktuellen Skripte aus dem git-Repo ziehen (git pull, htw-pv3/weather-data, git bash)

Das Setup von Anaconda (pv3_python_0_setup_environment.txt) liegt im git repo weather-data/python. Das Setup-Skript wird z.B. in der Windows-Eingabeaufforderung (als Admin) ausgeführt.

### Workflow python environment

* Eingabeaufforderung (cmd) als Admin ausführen
* in das Verzeichnis von git wechseln und anaconda version checken (conda --version)
* environment erstellen [siehe Skript](https://github.com/htw-pv3/weather-data/blob/master/python/pv3_python_0_setup_environment.txt) Nur beim ersten mal, ansonsten überspringen
* environment starten (activate -<environment_name>
* Jupyter Notebook öffnen, Link aus der Cmd inklusive Token in Firefox oder Chrome öffnen 

# Hands-On-Übung

* Well-known Fehler

_Zugriff auf Datenbank wird verweigert_

__Fix:__

    Port anpassen: port = '5432', Passwort checken (PW: "sonnja")


_Grafik kann nicht erstellt werden_

__FIX:__
    
    Den namen des Mat. Views auf "pv3.pv3_time_weather_wr1_2015_mview" ändern, 

    Variablen auf "timestamp, p_ac" ändern


* Spezialfehler

* HTTP Error 
* in der cmd echo %path% eingeben, falls ihr den HTTP error bekommt müsst ihr zusützlich zu 
* C:\Users\Anaconda3\Scripts, C:\Users\Anaconda3\ den path Anaconda3\Library\bin als path eingeben
*  in der cmd: set PATH=%PATH%;C:\anaconda3\Library\bin (also einfach den pfad des bin ordners eingeben)
* in der cmd: echo %path% und checken ob alle 3 paths aufgeführt werden

_(OSError: [WinError 193] %1 is not a valid Win32 application)_

- Problem tritt auf beim import von pandas->numpy->ctype lib
- Mögliche Probleme: Anaconda ist falsche Bit-Version

_FIX:_ 
        
        command: "set CONDA_FORCE_32BIT=1", danach neue env erstellen. Alle Packages werden dann in 32-Bit Version installiert

- [stackoverflow](https://stackoverflow.com/questions/33709391/using-multiple-python-engines-32bit-64bit-and-2-7-3-5)


* Debugging
* Datenanalyse

__Vorteile und Nachteile von Jupyter Notebook:__

_Zweck:_ Tutorials und Präsentationen

- positiv
    -  Link auf GitHub
    -  GitHub stellt das gut dar
    -  Einfacher Einstieg für Python

- negativ
    - Komplizierter in git (Bilder, Run-Order)
    - Schwieriger zu debuggen
    - Kein verwenden von externen Skripten
    - Nicht geeignet zum schreiben von größeren Programmen (z.B. mehr als 3 Funktionen)


## Environments in jupyter notebooks: advanced -- add-on

Links:

- [nb\_conda\_kernels](https://github.com/Anaconda-Platform/nb_conda_kernels)
- [Ipython kernel](https://ipython.readthedocs.io/en/stable/install/kernel_install.html)

Einfach das Package im base-environment installieren:
    
```
conda install conda-forge::nb_conda_kernels
```

evtl muss in dem entsprechenden environment noch das Ipython kernel package installieren (erstmal ohne probieren):

```
conda activate d_py37_vis
conda install ipykernel
conda activate
```

