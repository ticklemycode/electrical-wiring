# Bathroom Electrical Wiring Diagram

## Project Overview
This document provides a complete wiring diagram and installation guide for a bathroom electrical system featuring:
- **GFCI Protection**: A 15A GFCI outlet provides power and protection for the entire circuit.
- **3-Way Switches**: For independent control of the main and vanity lights from two locations each.
- **Single-Pole Switch**: For the exhaust fan.
- **Centralized Distribution**: A main switch box (Box 2) acts as a hub for distributing power.

## Final Circuit Configuration

### Power Flow Sequence
The circuit follows a logical, hub-based design for safety and simplicity.
1.  **Power Source**: A 15A breaker at the electrical panel feeds the circuit.
2.  **Box 1 (GFCI Outlet)**: Power enters the bathroom here. The GFCI outlet protects all downstream devices.
3.  **Box 2 (Distribution Hub)**: A 14-2 cable from the GFCI's LOAD terminals feeds this box. Inside, hot and neutral wires are distributed to the switch legs controlling the various fixtures. This box contains:
    - **Main Switch 1** (3-Way)
    - **Vanity Switch 1** (3-Way)
4.  **Box 4 (Main Light Control)**: Contains **Main Switch 2** (3-Way). It's connected to Box 2 via a 14-3 cable.
5.  **Box 7 (Vanity & Fan Control)**: Contains **Vanity Switch 2** (3-Way) and the **Fan Switch** (Single-Pole). It's connected to Box 2 via a 14-3 cable.
6.  **Fixtures**: Each light and the fan is fed directly from its final control switch.

### Quick Wire Flow Overview
```
⚫ HOT WIRE FLOW:
Panel → GFCI → Box 2 (Hot/Neutral Hub)
   ↓
   ├─ (via 14-3) → Box 4 (Main SW 2) → Main Light
   └─ (via 14-3) → Box 7 (Vanity SW 2 & Fan SW) → Vanity Light & Fan

⚪ NEUTRAL WIRE FLOW:  
Panel → GFCI → Box 2 (Neutral Hub)
   ↓
   ├─ (via 14-3) → Box 4 → Main Light
   └─ (via 14-3) → Box 7 → Vanity Light & Fan

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
      ┌────────────────┐
(BOX 1) │  GFCI OUTLET   │
      └────────────────┘
             |
             | 14-2 Cable
             ↓
      ┌──────────────────────────┐
(BOX 2) │   DISTRIBUTION HUB       │
      │  - Main Switch 1 (3-Way) │
      │  - Vanity Switch 1 (3-Way) │
      └──────────────────────────┘
        |                      |
14-3 Cable             14-3 Cable
        |                      |
        ↓                      ↓
┌────────────────┐   ┌──────────────────────────┐
│ MAIN SWITCH 2  │   │  VANITY SWITCH 2 (3-Way) │ (BOX 7)
│   (3-Way)      │   │  FAN SWITCH (Single-Pole)│
└────────────────┘   └──────────────────────────┘
        |                      |           |
14-2 Cable             14-2 Cable  14-2 Cable
        |                      |           |
        ↓                      ↓           ↓
┌────────────┐         ┌──────────────┐  ┌─────────────┐
│ MAIN LIGHT │         │ VANITY LIGHT │  │ EXHAUST FAN │
└────────────┘         └──────────────┘  └─────────────┘
```

## Wire Configuration Details

### Wire Types Used:
- **14-2 NM-B w/Ground**: Contains one hot (black), one neutral (white), and one ground (bare copper).
- **14-3 NM-B w/Ground**: Contains two travelers/hots (black, red), one neutral (white), and one ground (bare copper).

### Wire Gauge: 14 AWG for a 15-Amp circuit.

## 3-Way Switch Wiring (Correct & Simplified)

In this design, the wiring is straightforward and code-compliant, with no re-identified white wires.

- **Hot Source**: The constant hot (black) from the power source connects to the **common (COM) terminal** of the *first* 3-way switch in each pair (both located in Box 2).
- **Travelers**: The red and black wires in the 14-3 cables run between the traveler terminals of the two 3-way switches for each light.
- **Switched Hot**: The **common (COM) terminal** of the *second* 3-way switch connects to the hot terminal of the light fixture it controls.
- **Neutral**: The white neutral wire is passed through all switch boxes and connects directly to the neutral terminal of each fixture. **Neutrals are never connected to switches.**
- **Ground**: The bare copper ground wire connects to the green ground screw on all switches, boxes, and fixtures.
