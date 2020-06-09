# 2020-05-20 14:00 - 15:30 PV-Modellierung mit Polys -----#7

## Kurzes Feedback und aktueller Stand

### Fragen: 
    
- db_log:

    - project? welche ebene? z.B. pv3?o der  aufgabe4?

    - version? was bedeutet das?

    - comment: "join_data" ausreichend?

- reichen 4 gb RAM? jaja

### Rückmeldung Aufgaben # ToDo LH

### Aufgabe #7: Datenverknüpfung mittels SQL-Join
### Aufgabe #8: Systematische Bestimmung der Messlücken

## Skript PV-Modul (PV-Modellierung)

1. Zelltechnologien

    - Zellarten: kristallin (mono und poly) / dünnschicht / nanostrukturierte

    - Fokus: Standardzellen mit mono- und polykristalliner und dünnschicht (amorphes Silizium) Zellstruktur

    - Wirkungsgrad

    - Wirkungsgrade (Labor): mono: 25, poly: 20,4 und 13,2 %

    - Wirkungsgrade (Serienproduktion): mono: 17, poly: 16 und dünn: 7,5 %

    - Best Research-Cell Efficiencies ermöglicht Rückschluss auf Entwicklung(-sfähigkeit) der Zellarten

    - spektrale Antwort der Zellarten

2. Kennlinien -> Modellierung

    - U-I-Kennlinien-Ratespiel: Widerstand klein, Widerstand groß, Diode, Batterie (mit Innenwiderstand)

    - U-I-Kennlinie-PV-Modul: Kurzschlussstrom, Leerlaufspannung, MPP, Füllfaktor, Wirkungsgrad_PV

    - relativer Wirkungsgrad: Effizienz im Bezug auf Effizienz bei STC-Bedingungen 

    - __Forschungsfrage:__

    > Wie ist das Schwachlichtverhalten der Module? Wie ist die Häufigkeitsverteilung der Globalstrahlung und wie ist der Gesamtertrag der Zelltechnologien im Vergleich zu den anderen Zelltechnologien?

3. MPP ->Modellierung

    - Leistungskennlinie mit und ohne Beleuchtung/Bestrahlung: mit Beleuchutng = Dunkeltest: gibt Rückschluss auf das "Verbrauchsverhalten" des PV-Moduls. Wird in der Praxis durch eine Sperrdiode unterbunden. 

    - Erste Näherung: Mit steigender Temperatur nimmt die Spannung im Pv-Modul ab.

    - __Forschungsfrage:__

    > Kann das Temperaturverhalten der PV-Module (Theorie) anhand der Messdaten validiert werden? 


    - MPP-Tracking: Verfahren, bei dem die elektirsche Belastung eines PV-Moduls so angepasst wird, dass die größte mögliche Leistung entnommen werden kann. Abhängig von Bestrahlungsstärke, Temp und Zelltyp. Durch Gleichspannungswandler elektronisch eingestellt.

4. Testbedingungen -> Datenblätter einlesen

    - STC (1000|25|-|-|1,5) und NOCT (800|-|20|1|1,5) siehe auch: https://photovoltaiksolarstrom.com/photovoltaiklexikon/standard-testbedingungen-stc/

    - Festlegung von Standardbedingungen ermöglicht Vergleichbarkeit der Module

5. Modellierung(-saspekte)

    Modell zur Beschreibung von PV-Modulen in Komponenten:

    Physik der Sonnenstrahlung

    elektrisches Modell (ideal, einfach, Ein- und Zweidioden, effektives Solarzelle): Ersatzschaltbild / PV-Kennliniengleichung 

    PVSOL und Polysun liefern wahrscheinlich keine präzisen/tiefen Aussagen über den Simulationskern


Welche wichtigen Faktoren machen die PV-Simulationssoftware im Bezug auf die Versuchsanlage "SonnJa!" aus?

- __Handling__: sollte möglichst einfach sein komplexe Einstellungen vorzunehmen
- schneller Einstieg und bei Bedarf hoher __Detailierungsgrad__: 
    - Grey-Box vs. Black-Box
- Für wen ist die Software vorgesehen (__Standpunkt__)?
- können __5 Modulfelder__ abgebildet werden? 5 Projekte vs. 1 Projekt. (Polysun=JA, aber keine Vorlage, PVSOL=?)
- __Wetterdatensatz einpflegbar__ (PVSol=Ja, Polysun=?)? -> Auflösung
- Berechnungsgeschwindigkeit -> wie lange muss man warten bis die Simulationsergebnisse ausgegeben werden?
- Verschattungsanalyse
- API (Schnittstelle zu anderen Programmen/Programmiersprachen)
- Aktivität im Hilfeforum 
- Dokumentation
- Datenbanken PV und WR: Aktualität und Breite der Datenbank


## Gruppenarbeit:

- PVSol
- Polysun


Tutorials: PV-SOL

- [2D_Anlagenplanung](http://downloads.valentin.de/webinar/PV_SOL_premium_2D_Anlagenplanung.wmv)

- [3D_Anlagenplanung](http://downloads.valentin.de/webinar/PV_SOL_premium_3D_Anlagenplanung.wmv)



__WICHTIGER LINK:__ informationen zur Versuchanlage SonnJa (Datenblätter, Messsystem, tech. Zeichnungen)
https://next.rl-institut.de/s/LRi8yMsxob6toeY

## Polysun Einstellungen

Projekt

- Projektname: SonnJA-WR1
- Bemerkung: WR1
- Standort aus Karte: 52,455 / 13,525 HüN 35 Name HTW-Berlin (G-Geb)

Vorlage:

- Energie-Erzeuger

    - Photovoltaik: Ja da neben auch Photovoltaik

- Anlagen-Spezifikation

    - Kollektor-/Generatorfeld: Ein Feld

    - Unter der Vorlagen : 50a: Photovoltaik auswählen


Netz:

- Stromnetz: Dreiphasen (230V/400V, 50 Hz, Stern, DE)
    
PV Generatorfeld:

- Generatorfeld:

    - Modultyp: ASI 105, Katalognr.: 115184

    - Ausrichtung: -35

    - Anstellwinkel: 15 (14,57)

    - Anzahl Module: 30


PV Auslegung:

- Filter

    - Hersteller: Danfoss S/A -> funktioniert nicht! was tun?

    - max. Wechselrichtertypen: 3

    - Auslegungskonzept: Strangwechselrichter


Katalognummern der Module:

- Aleo Solar:
    - S19L285: 174700
    - S18.240: 208020
    - S19.245: 116014
- Schott:
    - ASI 105: 115184