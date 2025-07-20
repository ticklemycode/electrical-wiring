# Complete Bathroom Wiring Layout (Final Design)

This document provides the final physical and logical layout for the bathroom wiring circuit. The design uses **Box 1 (GFCI) as the power distribution hub** and **Box 7 as the control center** to ensure code compliance and proper GFCI protection.

## Physical Layout Diagram

```text
BATHROOM ELECTRICAL LAYOUT (BOX 1 POWER HUB DESIGN)
═══════════════════════════════════════════════════════════════

                    ┌────────────────────────┐
                    │ Electrical Panel (15A) │
                    └───────────┬────────────┘
                                │ 14-2 Cable
                                ↓
    WALL 1 (Entry)          ┌──────────────────────────────┐
    ───────────────────       │ Box 1: GFCI OUTLET & HUB    │
                              │ • GFCI Protection            │
                              │ • Power Distribution         │
                              └─┬─────────┬──────────┬───────┘
                                │14-2     │14-2      │14-2
                                ↓         ↓          ↓
           ┌─────────────────────────┐   ┌─────────┐   ┌──────────────────────────────┐
           │ Box 2: Vanity Switch 1  │   │Box 4:   │   │ Box 7: CONTROL CENTER        │
           │ (3-Way)                 │   │Main SW 1│   │ • Main Switch 2 (3-Way)      │
           └──────────┬──────────────┘   │(3-Way)  │   │ • Vanity Switch 2 (3-Way)    │
                      │14-3 Travelers    │         │   │ • Fan Switch (Single-Pole)   │
                      └──────────────────┼─────────┼───│                              │
                                         │14-3     │   └─┬─────────┬──────────┬──────┘
                                         │Travelers│     │14-2     │14-2      │14-2
                                         └─────────┘     ↓         ↓          ↓

    FIXTURES (All fed from Box 7):
    ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
    │ Box 3:      │  │ Box 5:      │  │ Box 6:      │
    │ Vanity      │  │ Main        │  │ Exhaust     │
    │ Light       │  │ Light       │  │ Fan         │
    └─────────────┘  └─────────────┘  └─────────────┘
```

## Wire Routing and Logic

```text
POWER & CONTROL FLOW (FINAL DESIGN)
═══════════════════════════════════════════════════════════════

[PANEL] → 14-2 → [BOX 1: GFCI & POWER HUB]
                     │
                     ├─(14-2 to Box 2)─→ Hot Power + Neutral (Vanity SW 1)
                     │                    
                     ├─(14-2 to Box 4)─→ Hot Power + Neutral (Main SW 1)
                     │                    
                     └─(14-2 to Box 7)─→ Hot Power + Neutral (Control Center)
                                             │
                                             ├─(14-2 to Box 3)─→ Switched Hot (Vanity Light)
                                             │                    + Neutral Return
                                             │
                                             ├─(14-2 to Box 5)─→ Switched Hot (Main Light)
                                             │                    + Neutral Return
                                             │
                                             └─(14-2 to Box 6)─→ Switched Hot (Fan)
                                                                 + Neutral Return

3-WAY SWITCHING:
Box 2 (Vanity SW 1) ←→ Box 7 (Vanity SW 2) via 14-3 cable (RED & BLACK travelers)
Box 4 (Main SW 1) ←→ Box 7 (Main SW 2) via 14-3 cable (RED & BLACK travelers)

NEUTRAL FLOW:
Panel → GFCI (Box 1) → distributed to all switches → continues to all fixtures
```

## Installation Sequence (Final)

Follow this sequence to ensure a logical and correct installation.

1.  **Install All Boxes**: Mount all electrical boxes in their designated locations.
2.  **Run All Cables**:
    *   Run **14-2** from Panel to Box 1 (GFCI).
    *   Run **14-2** from Box 1 to Box 2 (Vanity SW 1).
    *   Run **14-2** from Box 1 to Box 4 (Main SW 1).
    *   Run **14-2** from Box 1 to Box 7 (Control Center).
    *   Run **14-3** from Box 2 to Box 7 (Vanity 3-way circuit).
    *   Run **14-3** from Box 4 to Box 7 (Main 3-way circuit).
    *   Run **14-2** from Box 7 to Box 3 (Vanity Light).
    *   Run **14-2** from Box 7 to Box 5 (Main Light).
    *   Run **14-2** from Box 7 to Box 6 (Fan).
3.  **Wire Devices in Order**:
    *   **Box 1**: Wire the GFCI outlet with wire nuts for power distribution.
    *   **Box 7**: This is the control center. Wire all three switches carefully.
    *   **Box 2 & 4**: Wire the first switches for each 3-way circuit.
    *   **Fixtures**: Connect the Vanity Light, Main Light, and Fan.
4.  **Test Circuit**: After verifying all connections, turn on the breaker and test all functions.

## Critical Connection Points

-   **Box 1 (GFCI & Power Hub)**: This box distributes GFCI-protected power to all three switch locations.
    -   The GFCI outlet protects the entire circuit.
    -   Wire nuts are used to split the LOAD side of the GFCI to feed Boxes 2, 4, and 7.
    -   All neutral connections are made here for proper GFCI function.
-   **Box 7 (Control Center)**: This triple-gang box contains all "second" switches and controls all fixtures.
    -   Gets constant hot from Box 1 for the fan switch and as a connection point for 3-way circuits.
    -   Sends switched hot to all three fixtures (vanity light, main light, fan).
-   **White Wires**: In this design, all white wires are used as **neutrals**. No re-identification is required.
-   **Grounding**: Ensure all ground wires are properly connected in every box and to every device.
