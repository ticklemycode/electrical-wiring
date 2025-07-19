# Complete Bathroom Wiring Layout (Updated Design)

This document provides a detailed physical and logical layout for the optimized bathroom wiring circuit. The design uses Box 2 (Vanity Switch 1) as the central distribution hub to simplify wiring and ensure code compliance.

## Physical Layout Diagram

This diagram shows the physical placement of each box and the cable runs between them.

```text
BATHROOM ELECTRICAL LAYOUT (OPTIMAL DESIGN)
═══════════════════════════════════════════════════════════════

                    ┌────────────────────────┐
                    │ Electrical Panel (15A) │
                    └───────────┬────────────┘
                                │ 14-2 Cable
                                ↓
    WALL 1 (Vanity Side)      ┌────────────────────────┐
    ───────────────────       │ Box 1: GFCI Outlet     │
                              └───────────┬────────────┘
                                          │ 14-2 Cable
                                          ↓
                              ┌────────────────────────┐
                              │ Box 2: Vanity SW 1     │ --(14-3)--> To Box 4 (Main Light SW)
                              │ (MAIN DISTRIBUTION HUB)│
                              └───────────┬────────────┘
                                          │ 14-3 Cable
                                          ↓
    WALL 2 (Door Side)        ┌────────────────────────┐
    ───────────────────       │ Box 7: Combined Box    │ <-- (from Box 2)
                              │ • Vanity SW 2 (3-way)  │
                              │ • Fan Switch (1-pole)  │
                              └───────────┬────────────┘
                                          │ 14-2 Cable
                                          ↓
                              ┌────────────────────────┐
                              │ Box 3: Vanity Light    │
                              └────────────────────────┘


    WALL 3 (Shower Side)      ┌────────────────────────┐
    ───────────────────       │ Box 4: Main SW 2       │ <--(14-3)-- From Box 2
                              │ (3-way)                │
                              └───────────┬────────────┘
                                          │ 14-2 Cable
                                          ↓
                              ┌────────────────────────┐
                              │ Box 5: Main Light      │
                              └───────────┬────────────┘
                                          │ 14-2 Cable
                                          ↓
                              ┌────────────────────────┐
                              │ Box 6: Exhaust Fan     │
                              └────────────────────────┘
```

## Wire Routing and Logic

This diagram illustrates the flow of power and the purpose of each cable.

```text
WIRING LOGIC & CABLE ROUTING
═══════════════════════════════════════════════════════════════

[PANEL] → 14-2 → [BOX 1: GFCI] → 14-2 → [BOX 2: VANITY SW 1 (HUB)]
                                             │
                                             ├─(14-3 to Box 4)─→ • Black: Traveler 1 (Main Light)
                                             │                     • Red:   Traveler 2 (Main Light)
                                             │                     • White: Neutral
                                             │
                                             └─(14-3 to Box 7)─→ • Black: Constant Hot for Fan
                                                                 • Red:   Traveler 1 (Vanity Light)
                                                                 • White: Traveler 2 (Vanity Light) - Re-identified as HOT

[BOX 4: MAIN SW 2] → 14-2 → [BOX 5: MAIN LIGHT]
   • Receives switched hot from 3-way logic.
   • Neutral is fed from Box 2 via the 14-3 cable.

[BOX 7: COMBINED BOX] → 14-2 → [BOX 3: VANITY LIGHT]
   • Receives switched hot from vanity 3-way logic.
   • Neutral is fed from Box 2 via the 14-3 cable.

[BOX 7: COMBINED BOX] → 14-2 → [BOX 6: EXHAUST FAN]
   • Receives switched hot from the single-pole fan switch.
   • Neutral is fed from Box 2 via the 14-3 cable.
```

## Installation Sequence (Updated)

Follow this sequence to ensure a logical and correct installation.

1.  **Install All Boxes**: Mount all 6 electrical boxes in their designated locations.
2.  **Run All Cables**:
    *   Run **14-2** from Panel to Box 1 (GFCI).
    *   Run **14-2** from Box 1 to Box 2 (Vanity SW 1).
    *   Run **14-3** from Box 2 to Box 4 (Main SW 2).
    *   Run **14-3** from Box 2 to Box 7 (Combined Box).
    *   Run **14-2** from Box 4 to Box 5 (Main Light).
    *   Run **14-2** from Box 7 to Box 3 (Vanity Light).
    *   Run **14-2** from Box 7 to Box 6 (Exhaust Fan).
3.  **Wire Devices in Order**:
    *   **Box 1**: Wire the GFCI outlet, connecting incoming power to LINE and outgoing power to LOAD.
    *   **Box 2**: This is the most complex box. Splice incoming hot to feed both 14-3 cables. Bundle all neutrals. Connect travelers.
    *   **Box 4**: Wire the 3-way switch for the main light.
    *   **Box 7**: Wire the 3-way switch for the vanity light and the single-pole switch for the fan.
    *   **Fixtures**: Connect the Main Light (Box 5), Vanity Light (Box 3), and Fan (Box 6).
4.  **Test Circuit**: After verifying all connections, turn on the breaker and test all functions.

## Critical Connection Points

-   **Box 2 (Main Hub)**: This box is the key to the simplified design.
    -   The incoming hot from the GFCI is spliced to provide constant power to both 3-way circuits.
    -   All neutrals are bundled here, providing the return path for all fixtures.
-   **Re-identifying Wires**: In the 14-3 cable from Box 2 to Box 7, the white wire is used as a traveler. It **must be re-identified** with black or red electrical tape on both ends to indicate it carries a hot charge.
-   **Grounding**: Ensure all ground wires are properly connected in every box and to every device. A continuous ground path is required for safety.

## Switch Control Logic

The 3-way switching logic is standard for both the main and vanity lights.

-   **Main Light**: Controlled by 3-way switches in Box 2 and Box 4.
-   **Vanity Light**: Controlled by 3-way switches in Box 2 and Box 7.
-   **Fan**: Controlled by a single-pole switch in Box 7.
