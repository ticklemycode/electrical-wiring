# Complete Bathroom Wiring Layout (Corrected Design)

This document provides the corrected physical and logical layout for the bathroom wiring circuit. The design uses **Box 7 as both the control center AND power distribution hub** to ensure code compliance and proper GFCI protection.

## Physical Layout Diagram

```text
BATHROOM ELECTRICAL LAYOUT (BOX 7 HUB DESIGN)
═══════════════════════════════════════════════════════════════

                    ┌────────────────────────┐
                    │ Electrical Panel (15A) │
                    └───────────┬────────────┘
                                │ 14-2 Cable
                                ↓
    WALL 1 (Entry)          ┌────────────────────────┐
    ───────────────────       │ Box 1: GFCI Outlet     │
                              └───────────┬────────────┘
                                          │ 14-2 Cable
                                          ↓
                              ┌──────────────────────────────┐
                              │ Box 7: CONTROL CENTER & HUB │
                              │ • Main Switch 2 (3-Way)     │
                              │ • Vanity Switch 2 (3-Way)   │
                              │ • Fan Switch (Single-Pole)  │
                              │ • Power Distribution         │
                              └─┬─────────────┬──────────────┘
                                │ 14-3 Cable  │ 14-3 Cable
                                ↓             ↓
           ┌─────────────────────────┐   ┌─────────────────────────┐
           │ Box 2: Vanity Switch 1  │   │ Box 4: Main Switch 1    │
           │ (3-Way)                 │   │ (3-Way)                 │
           └─────────────────────────┘   └─────────────────────────┘

    FIXTURES (All fed from Box 7):
    ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
    │ Box 3:      │  │ Box 5:      │  │ Box 6:      │
    │ Vanity      │  │ Main        │  │ Exhaust     │
    │ Light       │  │ Light       │  │ Fan         │
    └─────────────┘  └─────────────┘  └─────────────┘
         ↑                 ↑                 ↑
         └─────14-2────────┼─────14-2───────┘
                          14-2
```

## Wire Routing and Logic

```text
POWER & CONTROL FLOW (CORRECTED)
═══════════════════════════════════════════════════════════════

[PANEL] → 14-2 → [BOX 1: GFCI] → 14-2 → [BOX 7: CONTROL CENTER & HUB]
                                             │
                                             ├─(14-3 to Box 2)─→ • Black: Traveler 1 (Vanity)
                                             │                    • Red:   Traveler 2 (Vanity)  
                                             │                    • White: Hot Power + Neutral
                                             │
                                             ├─(14-3 to Box 4)─→ • Black: Traveler 1 (Main)
                                             │                    • Red:   Traveler 2 (Main)
                                             │                    • White: Hot Power + Neutral
                                             │
                                             ├─(14-2 to Box 3)─→ • Black: Switched Hot (Vanity Light)
                                             │                    • White: Neutral
                                             │
                                             ├─(14-2 to Box 5)─→ • Black: Switched Hot (Main Light)
                                             │                    • White: Neutral
                                             │
                                             └─(14-2 to Box 6)─→ • Black: Switched Hot (Fan)
                                                                 • White: Neutral

3-WAY SWITCHING:
Box 2 (Vanity SW 1) ←→ Box 7 (Vanity SW 2) via RED & BLACK travelers
Box 4 (Main SW 1) ←→ Box 7 (Main SW 2) via RED & BLACK travelers

NEUTRAL FLOW:
Panel → GFCI → Box 7 → distributed to all fixtures and remote switches
```

## Installation Sequence (Final)

Follow this sequence to ensure a logical and correct installation.

1.  **Install All Boxes**: Mount all electrical boxes in their designated locations.
2.  **Run All Cables**:
    *   Run **14-2** from Panel to Box 1 (GFCI).
    *   Run **14-2** from Box 1 to Box 2 (Distribution Hub).
    *   Run **14-3** from Box 2 to Box 4 (Main SW 2).
    *   Run **14-3** from Box 2 to Box 7 (Combined Box).
    *   Run **14-2** from Box 4 to the Main Light location.
    *   Run **14-2** from Box 7 to the Vanity Light location.
    *   Run **14-2** from Box 7 to the Fan location.
3.  **Wire Devices in Order**:
    *   **Box 1**: Wire the GFCI outlet (LINE/LOAD).
    *   **Box 2**: This is the hub. Make all hot and neutral splices here. See `switch-wiring-guide.md` for detailed instructions.
    *   **Box 4 & 7**: Wire the downstream switches.
    *   **Fixtures**: Connect the Main Light, Vanity Light, and Fan.
4.  **Test Circuit**: After verifying all connections, turn on the breaker and test all functions.

## Critical Connection Points

-   **Box 2 (Distribution Hub)**: This box is the key to the design.
    -   The incoming hot (black) from the GFCI is spliced to feed the common terminals of Main Switch 1 and Vanity Switch 1, and the constant hot for the fan circuit.
    -   The incoming neutral (white) from the GFCI is bundled with the white neutrals in the two outgoing 14-3 cables, providing the return path for all fixtures.
-   **White Wires**: In this design, all white wires are used as **neutrals**. No re-identification is required.
-   **Grounding**: Ensure all ground wires are properly connected in every box and to every device.
