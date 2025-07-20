# Complete Bathroom Wiring Layout (Final Design)

This document provides a detailed physical and logical layout for the optimized bathroom wiring circuit. The design uses **Box 2 as the central distribution hub** to simplify wiring, ensure code compliance, and provide clear, safe power distribution.

## Physical Layout Diagram

This diagram shows the physical placement of each box and the cable runs between them.

```text
BATHROOM ELECTRICAL LAYOUT (HUB-BASED DESIGN)
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
                              ┌────────────────────────┐
                              │ Box 2: DISTRIBUTION HUB│
                              │ • Main Switch 1        │
                              │ • Vanity Switch 1      │
                              └───────────┬────────────┘
                                          │
                  ┌───────────────────────┴───────────────────────┐
                  │ 14-3 Cable                                    │ 14-3 Cable
                  ↓                                               ↓
    WALL 2 (Shower Side)      ┌────────────────────────┐    WALL 3 (Vanity Side)
    ───────────────────       │ Box 4: Main Switch 2   │    ───────────────────
                              │ (3-way)                │          ┌────────────────────────┐
                              └───────────┬────────────┘          │ Box 7: Combined Box    │
                                          │ 14-2 Cable            │ • Vanity SW 2 (3-way)  │
                                          ↓                       │ • Fan Switch (1-pole)  │
                              ┌────────────────────────┐          └─┬──────────┬───────────┘
                              │ Box 5: Main Light      │            │ 14-2     │ 14-2
                              └────────────────────────┘            ↓          ↓
                                                              ┌─────────┐  ┌─────────┐
                                                              │ Vanity  │  │ Fan     │
                                                              │ Light   │  │         │
                                                              └─────────┘  └─────────┘
```

## Wire Routing and Logic

This diagram illustrates the flow of power and the purpose of each conductor within the cables.

```text
WIRING LOGIC & CABLE ROUTING (FINAL)
═══════════════════════════════════════════════════════════════

[PANEL] → 14-2 → [BOX 1: GFCI] → 14-2 → [BOX 2: DISTRIBUTION HUB]
                                             │
                                             ├─(14-3 to Box 4)─→ • Black: Traveler 1 (Main Light)
                                             │                     • Red:   Traveler 2 (Main Light)
                                             │                     • White: Neutral for Main Light
                                             │
                                             └─(14-3 to Box 7)─→ • Black: Constant Hot for Fan Switch
                                                                 • Red:   Traveler (Vanity Light)
                                                                 • White: Neutral for Vanity & Fan

[BOX 4: MAIN SW 2] → 14-2 → [BOX 5: MAIN LIGHT]
   • Black: Switched hot from 3-way logic
   • White: Neutral from Box 2 (passed through Box 4)

[BOX 7: COMBINED BOX]
   ├─(14-2 to Vanity Light)─→ • Black: Switched hot from Vanity SW 2
   │                           • White: Neutral from Box 2 (passed through Box 7)
   │
   └─(14-2 to Fan)──────────→ • Black: Switched hot from Fan Switch
                               • White: Neutral from Box 2 (passed through Box 7)

VANITY 3-WAY SWITCHING:
Box 2 (Vanity SW 1) ←→ Box 7 (Vanity SW 2) via RED traveler wire.
• Standard 3-way circuit.

MAIN 3-WAY SWITCHING:
Box 2 (Main SW 1) ←→ Box 4 (Main SW 2) via BLACK & RED traveler wires.
• Standard 3-way circuit.
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
