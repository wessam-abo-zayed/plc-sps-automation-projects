# SPS SCALE Aufgabe – Analogwertverarbeitung – TIA Portal

Dieses Projekt zeigt die Verarbeitung eines analogen Eingangswertes mit Siemens TIA Portal.

Im SPS-Programm wird der Siemens-Baustein `SCALE` verwendet, um einen analogen Eingangswert zu skalieren. Der Rohwert des Analogeingangs wird eingelesen und in einen normierten Realwert umgerechnet.

Das Projekt wurde nicht nur simuliert, sondern auch auf einer realen Siemens SPS getestet. Dabei wurde die Änderung eines realen analogen Eingangswertes direkt im SPS-Programm beobachtet und überprüft.

---

## Ziel des Projekts

Ziel des Projekts ist es, einen analogen Eingangswert in TIA Portal einzulesen, mit dem Baustein `SCALE` zu skalieren und den berechneten Wert im Programm zu überwachen.

Dabei werden folgende Funktionen umgesetzt:

* analogen Eingangswert einlesen
* SCALE-Baustein verwenden
* Rohwert in normierten Wert umrechnen
* unteren Grenzwert festlegen
* oberen Grenzwert festlegen
* Rückgabewert des SCALE-Bausteins überwachen
* skalierten Wert als Realwert speichern
* Programm auf realer Siemens SPS testen
* Änderung des realen Analogwertes im SPS-Programm beobachten
* Werte zwischen realer SPS und Programm vergleichen

---

## Verwendete Software und Hardware

* Siemens TIA Portal
* reale Siemens PLC
* analoger Eingang
* FUP / Funktionsplan
* Online-Beobachtung mit realen SPS-Werten
* Simulation und Test mit realen Analogwerten

---
## SCALE-Baustein

Der SCALE-Baustein wird verwendet, um den analogen Eingangswert in einen normierten Wert umzuwandeln.

Verwendete Parameter:

| Parameter | Bedeutung                                            |
| --------- | ---------------------------------------------------- |
| `IN`      | Eingangswert vom analogen Kanal                      |
| `HI_LIM`  | oberer Grenzwert                                     |
| `LO_LIM`  | unterer Grenzwert                                    |
| `BIPOLAR` | Auswahl zwischen unipolarer und bipolarer Skalierung |
| `RET_VAL` | Rückgabewert / Status des Bausteins                  |
| `OUT`     | skalierter Ausgangswert                              |

In diesem Projekt wird der Wertbereich von `0.0` bis `4000.0` verwendet.

---

## Simulation und Test

In der Simulation und im realen SPS-Test werden folgende Punkte geprüft:

* analoger Eingangswert wird gelesen
* SCALE-Baustein wird korrekt ausgeführt
* Grenzwerte `LO_LIM` und `HI_LIM` werden berücksichtigt
* `RET_VAL` wird überwacht
* skalierter Realwert wird korrekt gespeichert
* reale Analogwertänderung wird im SPS-Programm sichtbar
* reale SPS-Werte stimmen mit den beobachteten Programmwerten überein

---

## Was ich in diesem Projekt gelernt habe

* Einlesen analoger Werte in TIA Portal
* Verwendung des SCALE-Bausteins
* Skalierung von Rohwerten
* Arbeit mit Datentypen wie `Int`, `Word` und `Real`
* Überwachung von SPS-Variablen
* Testen eines Programms auf realer Siemens SPS
* Beobachtung realer Analogwertänderungen im SPS-Programm
* Vergleich zwischen realen SPS-Werten und Programmwerten

---
## Autor

<div align="center">

### **Wessam Abo Zayed**

**Automatisierungstechnik | SPS-/PLC-Programmierung | Data Analyst**
</div>

## Kontakt

| Kontakt      | Link                                                                            |
| ------------ | ------------------------------------------------------------------------------- |
| **E-Mail**   | [abozayed.wessam@gmail.com](mailto:abozayed.wessam@gmail.com)                   |
| **LinkedIn** | [linkedin.com/in/wessam-abozayed](https://www.linkedin.com/in/wessam-abozayed/) |
| **GitHub**   | [github.com/wessam-abo-zayed](https://www.github.com/wessam-abo-zayed)                   |
| **Tableau Public** | [public.tableau.com/app/profile/wessam3726](https://public.tableau.com/app/profile/wessam3726) |
