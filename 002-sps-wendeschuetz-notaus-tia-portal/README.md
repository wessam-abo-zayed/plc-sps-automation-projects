# SPS Wendeschütz mit Not-Aus – TIA Portal

Dieses Projekt zeigt die SPS-Steuerung eines Wendeschützes mit Not-Aus-Funktion in Siemens TIA Portal.

---

## Ziel des Projekts

Ziel des Projekts ist es, eine Motorsteuerung mit Rechtslauf, Linkslauf und Not-Aus-Funktion zu programmieren und zu testen.

Dabei werden folgende Funktionen umgesetzt:

* Motor Rechtslauf starten
* Motor Linkslauf starten
* Motor stoppen
* Not-Aus-Funktion auswerten
* Reset nach Not-Aus
* gegenseitige Verriegelung der Schütze
* Motorschutz auswerten
* Simulation der Steuerung

---

## Verwendete Software

* Siemens TIA Portal
* Siemens SPS / PLC
* FUP / Funktionsplan
* PLCSIM oder Simulationsumgebung

---

## Programmstruktur

Das Hauptprogramm befindet sich im Baustein `Main [OB1]`.

Im OB1 werden zwei Funktionen aufgerufen:

| Baustein | Name                  | Funktion                                     |
| -------- | --------------------- | -------------------------------------------- |
| `FC5`    | `fc005_NotAus`        | Not-Aus- und Reset-Logik                     |
| `FC50`   | `fc050_AnsteuerungM1` | Ansteuerung Motor 1 Rechtslauf und Linkslauf |

---

## Was ich in diesem Projekt gelernt habe

* Aufbau eines SPS-Projekts in TIA Portal
* Verwendung von `OB1`, `FC5` und `FC50`
* Programmierung mit FUP
* Motorsteuerung mit Rechtslauf und Linkslauf
* Verwendung von Merkern
* Setzen und Rücksetzen mit SR-Gliedern
* Not-Aus- und Reset-Logik
* gegenseitige Verriegelung von Schützen
* Dokumentation von SPS-Variablen
* Testen der Steuerung mit Simulation

---

## Autor

Wessam Abo Zayed
