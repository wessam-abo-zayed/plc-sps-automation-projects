# 007 – SPS Motorsteuerung (FC – TIA Portal)

## 🎯 Projektziel
Ziel dieses Projekts ist die Entwicklung einer modularen Motorsteuerung für zwei Motoren in Siemens TIA Portal.  
Die Steuerlogik wird in einem Funktionsbaustein (FC50) implementiert, sodass sie für beide Motoren wiederverwendbar ist.

Die Motoren können über ein Bedienpult in Rechtslauf und Linkslauf gesteuert werden.  
Ein Richtungswechsel ist nur über die Aus-Funktion möglich.  
Zusätzlich ist ein Motorschutz integriert, der den Motor im Fehlerfall sofort stoppt.

---

## ⚙️ Funktionsbeschreibung

- Steuerung von zwei Motoren (Motor 1 & Motor 2)
- Bedienung über:
  - 🔄 Rechtslauf
  - 🔄 Linkslauf
  - ⛔ Aus
- Sicherheitsfunktion:
  - Motorschutz stoppt den Motor sofort bei Auslösung
  - Neustart nur möglich, wenn Motorschutz wieder OK ist
- Not-Aus Funktion für die gesamte Anlage
- Wiederverwendbare Logik über FC50 (lokale Parametrierung)

---

## 🧠 SPS Programmstruktur

Das Projekt basiert auf einer strukturierten SPS-Architektur in TIA Portal:

- **OB1 (Hauptzyklus)**
  - Aufruf des Funktionsbausteins FC50 für beide Motoren

- **FC50 (Motorlogik)**
  - Zentrale Steuerlogik für einen Motor
  - Parametrierung über lokale Variablen
  - Steuerung von:
    - Rechtslauf
    - Linkslauf
    - Stop
    - Motorschutzüberwachung

- **I/O Zuordnung**
  - Bedienpult Eingänge (Start/Stop/Richtung)
  - Motorschutzsignale
  - Ausgänge für Motorsteuerung

- **Wiederverwendbarkeit**
  - FC50 wird zweimal verwendet (Motor 1 & Motor 2)
  - Unterschiedliche Parameter über Übergabevariablen

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
