# 🔧 SPS Projekt – Biegewerkzeug 1 (TIA Portal)

Die Anlage wurde sowohl im **TIA Portal Simulator (PLCSIM)** als auch auf einer **realen Siemens SPS (CPU 314C-2 DP)** getestet.

---

## 🎯 Projektziel

Ziel des Projekts ist die Umsetzung einer **sequenziellen Ablaufsteuerung** für ein hydraulisches Biegewerkzeug.

Dabei werden reale Ein- und Ausgangssignale verarbeitet und der komplette Prozess logisch in der SPS abgebildet.

---

## ⚙️ Funktionsbeschreibung

Der Prozess läuft wie folgt ab:

1. Start über Taster **S1**
2. Zylinder 1 fährt aus → Werkstück wird gespannt und vorgebogen
3. Wenn Endlage **1B2** erreicht ist:
   - Zylinder 2 fährt aus
   - Biegevorgang wird durchgeführt
4. Nach Erreichen der Endlage fährt Zylinder 2 wieder ein
5. Danach fährt Zylinder 1 wieder ein
6. Der Zyklus ist abgeschlossen

---

## 📁 Projektstruktur


006-sps-biegewerkzeug-1-tia-portal/<br>
│<br>
├── README.md<br>
├── tia-project/ (TIA Portal Projekt)<br>
├── docs/ (Aufgabe + Beschreibung)<br>
└── video/ (Link zur Simulation)<br>

---

## 🧠 SPS Programmstruktur

Das Projekt wurde strukturiert in:

- OB1 (Main Cycle)
- FC1 (Ablaufsteuerung)
- SR-Glieder für Schrittketten
- Symbolische Variablen (PLC Tags)
- Beobachtungstabelle für Tests

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
