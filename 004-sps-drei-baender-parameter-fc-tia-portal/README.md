
# SPS Drei Bänder – Parameter-FC – TIA Portal

Dieses Projekt zeigt die SPS-Steuerung von drei Förderbändern mit Siemens TIA Portal.

Die drei Bänder werden so angesteuert, dass beim Einschalten zuerst Band 3 startet. Danach startet Band 2 mit Verzögerung und anschließend Band 1. Beim Ausschalten wird die Anlage in umgekehrter Reihenfolge gestoppt.

---

## Ziel des Projekts

Ziel des Projekts ist es, eine Ablaufsteuerung für drei Förderbänder zu programmieren, zu dokumentieren und zu simulieren.

Dabei werden folgende Funktionen umgesetzt:

* Anlage einschalten
* Bänder starten
* Bänder stoppen
* Not-Aus überwachen
* Reset nach Not-Aus
* Motorschutzrelais auswerten
* zeitverzögerter Start der drei Bänder
* zeitverzögertes Stoppen der drei Bänder
* Ansteuerung der Antriebe über Funktionsbausteine
* Simulation der Steuerung

---

## Verwendete Software

* Siemens TIA Portal
* Siemens SPS / PLC
* FUP / Funktionsplan
* PLCSIM oder Simulationsumgebung

---

## Ablaufbeschreibung

### Einschalten

Reihenfolge beim Einschalten:

1. M3 / Band 3 startet.
2. Nach 5 Sekunden startet M2 / Band 2.
3. Nach weiteren 10 Sekunden startet M1 / Band 1.

### Ausschalten

Reihenfolge beim Ausschalten:

1. M1 / Band 1 stoppt sofort.
2. M2 / Band 2 stoppt nach 10 Sekunden.
3. M3 / Band 3 stoppt nach weiteren 5 Sekunden.


## Sicherheits- und Überwachungsfunktionen

Die Anlage überwacht:

* Not-Aus
* Reset Not-Aus
* Motorschutzrelais F5
* Motorschutzrelais F7
* Motorschutzrelais F9

Wenn ein Motorschutzrelais auslöst oder der Not-Aus betätigt wird, bleiben alle Antriebe sofort stehen.

Nach dem Reset des Fehlers darf die Anlage im letzten Zustand weiterlaufen.

---

## Was ich in diesem Projekt gelernt habe

* Aufbau eines SPS-Projekts in TIA Portal
* Strukturierung des Programms mit mehreren FC-Bausteinen
* Programmierung einer Ablaufsteuerung
* Verwendung von Timern
* zeitverzögertes Starten und Stoppen von Motoren
* Auswertung von Not-Aus und Motorschutz
* Verwendung von Parametern in FC-Bausteinen
* Dokumentation von SPS-Projekten
* Testen der Steuerung mit Simulation

---

## Autor

<div align="center">

### **Wessam Abo Zayed**

**Data Analyst | SPS-/PLC-Programmierung**

</div>

---

**Data Analyst** mit Erfahrung in **Datenanalyse**, **Machine Learning** und **industrieller Automatisierung**.

Ich kombiniere analytische Fähigkeiten aus der Datenverarbeitung mit praktischen Kenntnissen in **SPS-/PLC-Programmierung**, insbesondere mit **Siemens TIA Portal**.

---

## Kontakt

| Kontakt      | Link                                                                            |
| ------------ | ------------------------------------------------------------------------------- |
| **E-Mail**   | [abozayed.wessam@gmail.com](mailto:abozayed.wessam@gmail.com)                   |
| **LinkedIn** | [linkedin.com/in/wessam-abozayed](https://www.linkedin.com/in/wessam-abozayed/) |
