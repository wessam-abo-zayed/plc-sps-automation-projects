# SPS Motor Stern-Dreieck-Anlauf – TIA Portal

Dieses Projekt zeigt die SPS-Steuerung eines Motors mit Stern-Dreieck-Anlauf in Siemens TIA Portal.

Beim Stern-Dreieck-Anlauf wird der Motor zuerst in Sternschaltung gestartet. Nach einer bestimmten Zeit wird automatisch auf Dreieckschaltung umgeschaltet. Dadurch wird der Anlaufstrom des Motors reduziert.

---

## Ziel des Projekts

Ziel des Projekts ist es, eine Motorsteuerung mit Stern-Dreieck-Anlauf zu programmieren, zu dokumentieren und zu simulieren.

Dabei werden folgende Funktionen umgesetzt:

* Motor starten
* Motor stoppen
* Netzschütz ansteuern
* Sternschütz ansteuern
* Dreieckschütz ansteuern
* Zeitverzögerung für die Umschaltung von Stern auf Dreieck
* gegenseitige Verriegelung zwischen Stern- und Dreieckschütz
* Motorschutz auswerten
* Simulation der Steuerung

---

## Verwendete Software

* Siemens TIA Portal
* Siemens SPS / PLC
* FUP / Funktionsplan
* PLCSIM oder Simulationsumgebung

---

## Funktionsbeschreibung

### Start des Motors

Durch Betätigung des Starttasters wird die Motorsteuerung freigegeben. Danach werden das Netzschütz und das Sternschütz eingeschaltet.

---

### Sternbetrieb

Im Sternbetrieb läuft der Motor mit reduziertem Anlaufstrom an. Diese Phase ist zeitlich begrenzt.

---

### Umschaltung auf Dreieck

Nach Ablauf der eingestellten Zeit wird das Sternschütz ausgeschaltet. Anschließend wird das Dreieckschütz eingeschaltet.

---

### Dreieckbetrieb

Im Dreieckbetrieb läuft der Motor im normalen Dauerbetrieb.

---

### Stopp und Motorschutz

Wenn der Stopptaster gedrückt wird oder der Motorschutz auslöst, werden alle Schütze abgeschaltet.

---

## Verriegelung

Die Verriegelung ist ein wichtiger Bestandteil der Steuerung.

Das Sternschütz und das Dreieckschütz dürfen niemals gleichzeitig aktiv sein.

Dadurch wird verhindert, dass ein elektrischer Kurzschluss entsteht.

---

## Was ich in diesem Projekt gelernt habe

* Aufbau eines SPS-Projekts in TIA Portal
* Programmierung eines Stern-Dreieck-Anlaufs
* Verwendung von Timern
* Ansteuerung mehrerer Schütze
* gegenseitige Verriegelung von Schützen
* Motorsteuerung mit Start- und Stopp-Logik
* Motorschutz-Auswertung
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

