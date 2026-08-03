# 🏭 S7-300 Bandsteuerung – OB / FB / Diagnose (TIA Portal)

## 📌 Projektübersicht

Dieses Projekt implementiert eine industrielle Förderbandsteuerung auf einer Siemens S7-300 CPU 314C-2 DP.

Der Fokus liegt auf einer strukturierten SPS-Softwarearchitektur mit:

- OB1 (zyklische Hauptverarbeitung)
- OB100 (Anlaufverhalten)
- OB121 (Fehlerbehandlung)
- FB10 (modulare Steuerlogik)
- DB-basierte Datenverwaltung
- Diagnose durch gezielte Speicherzugriffe

---

# 🏗️ PLC ARCHITEKTUR (SYSTEMÜBERSICHT)
                                                         ┌──────────────┐
                                                         │    OB100     │
                                                         │  Startup OB  │
                                                         └──────┬───────┘
                                                                │
                                                                ▼
                                                  ┌────────────────────────────┐
                                                  │           OB1              │
                                                  │   Main Cyclic Program      │
                                                  └────────────┬───────────────┘
                                                               │
                                                    ┌──────────┴─────────────────┐
                                                    ▼                            ▼
                                        ┌──────────────────────────┐ ┌──────────────────────────┐
                                        │          OB1             │ │          OB1             │
                                        │  Main Cyclic Program     │ │  Main Cyclic Program     │
                                        └──────────┬───────────────┘ └──────────────────────────┘
                                                   │
                                                   ▼
                                        ┌──────────────────────────┐
                                        │          OB1             │
                                        │  Main Cyclic Program     │
                                        └──────────┬───────────────┘
                                                   │
                                        ┌──────────┴───────────┐
                                        ▼                      ▼   
                                 DB100 Variables     DB101 Dummy Access Test

---

## ⚙️ Funktionsbeschreibung

Die Anlage simuliert eine industrielle Förderbandsteuerung mit folgenden Funktionen:

- Start / Stop Steuerung
- Moduswechsel (Main / Mod / Break / Direction)
- Sicherheitslogik im FB10
- zyklische Prozesssteuerung
- Fehlerreaktion über OB121
- strukturierte Datenverwaltung über DBs

---

## 🧠 SPS Programmstruktur

### 🔹 OB1 – Hauptprogramm
- Zyklische Steuerung
- Aufruf von FB10

### 🔹 FB10 – Bandsteuerung
- Zentrale Logik der Förderbandsteuerung
- Verarbeitung von Steuerbits:
  - Main_Switch
  - Mod_Switch
  - Break_Ctrl
  - Dir_Ctrl

### 🔹 OB100 – Startup
- Initialisierung nach CPU-Start
- definierte Startzustände

### 🔹 OB121 – Fehlerbehandlung
- Reaktion auf Laufzeit- oder Zugriffsfehler
- verhindert CPU-STOP

---

## 🔍 DUMMY DB TEST (WICHTIG – INDUSTRIAL LOGIC)

### 📌 Was wurde implementiert?

Im Projekt wird bewusst auf einen **Dummy-Datenbaustein (DB101)** zugegriffen.

Beispiel:
- Zugriff auf nicht produktiv genutzte Speicherbereiche
- gezielte Speicheroperationen zur Diagnose

---

### 🧠 Technischer Zweck

Der Dummy-DB-Test dient zur:

- Überprüfung von Speicherzugriffen
- Simulation von fehlerhaften oder kritischen DB-Zugriffen
- Test der OB121 Fehlerreaktion
- Validierung der SPS-Stabilität

---

### 🏭 Industrielle Bedeutung

In realen Automatisierungssystemen wird dieses Konzept genutzt für:

- Memory Integrity Tests
- Fault Reaction Validation
- Runtime Exception Handling
- Safety Behaviour Verification

---

## 🎯 Projektziel

- Aufbau einer modularen SPS-Architektur
- saubere Trennung von Logik und Daten
- Fehlerrobuste Programmstruktur
- industrielle Diagnosefähigkeit
- realistische Simulation eines Förderbandsystems


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
