# 3-Way Switch Wiring Guide (Updated for Optimal Design)

This guide provides detailed instructions for wiring the 3-way switches in the optimized bathroom circuit. In this design, **Box 2 is the central distribution hub**.

## Core Concepts for This Design

1.  **Power Distribution**: Power flows from the GFCI (Box 1) to Box 2. Box 2 then distributes power and travelers to Box 4 (for the main light) and Box 7 (for the vanity light and fan).
2.  **Traveler Wires**: These wires run between two 3-way switches, allowing either switch to control the light. They are always contained within a single 14-3 cable.
3.  **Wire Re-identification (NEC 200.7)**: When a white wire is used as a hot conductor (like a traveler), it **MUST** be re-identified by wrapping it with black or red electrical tape at both ends. This is a critical safety step.

---

## 1. Vanity Light Circuit Wiring (Box 2 ↔ Box 7)

This circuit controls the vanity light (Box 3) using 3-way switches in Box 2 and Box 7.

### Cable Run: 14-3 from Box 2 to Box 7
-   **Black Wire**: **Constant Hot**. This wire is NOT a traveler. It provides the always-on power needed for the fan switch in Box 7.
-   **Red Wire**: **Traveler 1**. Connects the T1 terminals of the two switches.
-   **White Wire**: **Traveler 2**. Connects the T2 terminals. **MUST BE RE-IDENTIFIED WITH BLACK TAPE.**
-   **Bare Ground**: Connects the ground screws.

### Wiring at Box 2 (Vanity Switch 1)
-   **Incoming Hot (from GFCI)**: Connect to a pigtail that feeds:
    1.  The **COM (Common) terminal** of the vanity 3-way switch.
    2.  The **Black Wire** in the 14-3 cable going to Box 4 (for the main light circuit).
-   **Red Wire (to Box 7)**: Connect to the **T1 terminal**.
-   **White Wire (to Box 7)**: **Mark with black tape**, then connect to the **T2 terminal**.
-   **Neutrals**: All white neutral wires are bundled together in a wire nut. **They do not connect to the switch.**
-   **Grounds**: All bare ground wires are bundled together with a pigtail to the switch's ground screw.

### Wiring at Box 7 (Vanity Switch 2)
-   **Incoming Black Wire (from Box 2)**: This is **Constant Hot**. Pigtail it to feed:
    1.  The **LINE terminal** of the single-pole fan switch.
-   **Incoming Red Wire (from Box 2)**: Connect to the **T1 terminal** of the vanity 3-way switch.
-   **Incoming White Wire (from Box 2)**: **Mark with black tape**, then connect to the **T2 terminal**.
-   **Outgoing Switched Hot (to Vanity Light)**: Connect a black wire to the **COM terminal**. This wire runs in the 14-2 cable to the vanity light fixture (Box 3).
-   **Neutrals**: All white neutral wires are bundled together.
-   **Grounds**: All bare ground wires are bundled together with pigtails to both switches' ground screws.

---

## 2. Main Light Circuit Wiring (Box 2 ↔ Box 4)

This circuit controls the main light (Box 5) using 3-way switches in Box 2 and Box 4.

### Cable Run: 14-3 from Box 2 to Box 4
-   **Black Wire**: **Traveler 1**.
-   **Red Wire**: **Traveler 2**.
-   **White Wire**: **Neutral**. This is a true neutral, providing the return path for the main light.
-   **Bare Ground**: Connects the ground screws.

### Wiring at Box 2 (Main Switch 1)
-   **Incoming Hot (from GFCI)**: The same pigtail that feeds the vanity switch also connects to the **COM terminal** of this main light 3-way switch.
-   **Black Wire (to Box 4)**: Connect to the **T1 terminal**.
-   **Red Wire (to Box 4)**: Connect to the **T2 terminal**.
-   **Neutrals**: The white wire from the 14-3 cable joins the main neutral bundle in the box.
-   **Grounds**: The bare ground wire joins the main ground bundle.

### Wiring at Box 4 (Main Switch 2)
-   **Incoming Black Wire (from Box 2)**: Connect to the **T1 terminal**.
-   **Incoming Red Wire (from Box 2)**: Connect to the **T2 terminal**.
-   **Outgoing Switched Hot (to Main Light)**: Connect a black wire to the **COM terminal**. This wire runs in the 14-2 cable to the main light fixture (Box 5).
-   **Neutrals**: The incoming white wire (from Box 2) is bundled with the outgoing white wire (to Box 5).
-   **Grounds**: All bare ground wires are bundled together with a pigtail to the switch's ground screw.

---

## 3. Fan Circuit Wiring (in Box 7)

The fan is controlled by a simple single-pole switch in Box 7.

-   **Constant Hot**: The black wire from Box 2 provides constant power. Connect it to one terminal of the fan switch.
-   **Switched Hot**: Connect a black wire to the other terminal of the fan switch. This wire runs in the 14-2 cable to the fan (Box 6).
-   **Neutral & Ground**: The neutral and ground for the fan are provided by the bundles in Box 7.
