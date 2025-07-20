# Bathroom Electrical Wiring Diagram

## Project Overview
This document provides a complete wiring diagram and installation guide for a bathroom electrical system featuring:
- **GFCI Protection**: A 15A GFCI outlet provides power and protection for the entire circuit.
- **3-Way Switches**: For independent control of the main and vanity lights from two locations each.
- **Single-Pole Switch**: For the exhaust fan.
- **Power Distribution Hub**: Box 1 (GFCI) acts as the power distribution hub using wire nuts to feed three separate switch locations.

## Final Circuit Configuration

### Power Flow Sequence
The circuit follows a logical, GFCI-hub design for safety and code compliance.
1.  **Power Source**: A 15A breaker at the electrical panel feeds the circuit.
2.  **Box 1 (GFCI & Power Hub)**: Power enters here. The GFCI outlet protects all downstream devices AND uses wire nuts to distribute power to three switch locations.
3.  **Box 2 (Vanity Switch 1)**: Single-gang box with first 3-way switch for vanity light.
4.  **Box 4 (Main Switch 1)**: Single-gang box with first 3-way switch for main light.
5.  **Box 7 (Control Center)**: Triple-gang box containing:
    - **Main Switch 2** (3-Way)
    - **Vanity Switch 2** (3-Way)
    - **Fan Switch** (Single-Pole)
6.  **Fixtures**: Each light and the fan is fed directly from Box 7 (control center).

### Quick Wire Flow Overview
```
⚫ HOT WIRE FLOW:
Panel → GFCI (Box 1) → Distributed to Boxes 2, 4, & 7
   ↓
   ├─ Box 2 (Vanity SW 1) ←→ Box 7 (Vanity SW 2) → Vanity Light
   ├─ Box 4 (Main SW 1) ←→ Box 7 (Main SW 2) → Main Light
   └─ Box 7 (Fan SW) → Fan

⚪ NEUTRAL WIRE FLOW:  
Panel → GFCI (Box 1) → Distributed to all switches → All fixtures

🟢 GROUND WIRE FLOW:
Panel → All Boxes & Devices (continuous)
```

## Detailed Wiring Diagram (ASCII)

This diagram illustrates the physical layout and cable runs for the final design.

```
      ELECTRICAL PANEL
             |
             | 14-2 Cable
             ↓
      ┌──────────────────────────┐
(BOX 1) │ GFCI OUTLET & POWER HUB │
      └─┬──────────┬─────────────┘
        |          |      |
  14-2 Cable  14-2 Cable 14-2 Cable
        |          |      |
        ↓          ↓      ↓
┌────────────┐ ┌───────┐ ┌──────────────────────────────┐
│ VANITY     │ │ MAIN  │ │      CONTROL CENTER          │ (BOX 7)
│ SWITCH 1   │ │ SW 1  │ │ - Main Switch 2 (3-Way)      │
│ (3-Way)    │ │(3-Way)│ │ - Vanity Switch 2 (3-Way)    │
└──────┬─────┘ └───┬───┘ │ - Fan Switch (Single-Pole)   │
       |14-3       |14-3 └─┬──────────┬──────────┬──────┘
       |Travelers  |Travel | 14-2     | 14-2     | 14-2
       └───────────┼──────└┤          |          |
                   └───────┘          ↓          ↓
                                ┌──────────┐  ┌─────────────┐
                                │MAIN LIGHT│  │ EXHAUST FAN │
                                └──────────┘  └─────────────┘
                                      ↓
                              ┌──────────────┐
                              │ VANITY LIGHT │
                              └──────────────┘
```

## Wire Configuration Details

### Wire Types Used:
- **14-2 NM-B w/Ground**: Contains one hot (black), one neutral (white), and one ground (bare copper).
- **14-3 NM-B w/Ground**: Contains two travelers/hots (black, red), one neutral (white), and one ground (bare copper).

### Wire Gauge: 14 AWG for a 15-Amp circuit.

## 3-Way Switch Wiring (Code Compliant Design)

In this design, the wiring is straightforward and code-compliant, with no re-identified white wires.

- **Power Distribution**: Box 1 (GFCI) distributes protected power to all three switch locations using wire nuts.
- **3-Way Circuits**: Both lights use standard 2-traveler wiring between their switch pairs:
  - **Main Light**: Box 4 (SW 1) ←→ Box 7 (SW 2) via 14-3 cable
  - **Vanity Light**: Box 2 (SW 1) ←→ Box 7 (SW 2) via 14-3 cable
- **Hot Source**: Each first switch gets constant hot from Box 1 (GFCI).
- **Travelers**: The red and black wires in the 14-3 cables carry the two travelers between switch pairs.
- **Switched Hot**: Box 7 (control center) sends switched hot to all three fixtures.
- **Neutral**: White neutral wires run continuously from GFCI through all switches to all fixtures. **Neutrals are never connected to switches.**
- **Ground**: The bare copper ground wire connects to all switches, boxes, and fixtures.
