# Comprehensive Wiring Guide (Box-by-Box)

This guide provides detailed, step-by-step wiring instructions for each electrical box in the final, optimized bathroom circuit.

## ⚠️ Critical Safety Reminders
- **Turn off power** at the breaker before beginning any work.
- **Use a voltage tester** to confirm the power is off.
- **No Re-identification Needed**: In this design, all wires are used for their standard purpose (black/red for hot, white for neutral). No re-identifying of wires with tape is necessary.
- **Pigtails**: Use 6-inch pigtails of the same color wire to connect devices when multiple wires are spliced in a wire nut. This improves organization and safety.

---

### Box 1: GFCI Outlet
*   **Purpose**: Provides GFCI protection for the entire circuit.
*   **Cables**: 14-2 from Panel (IN), 14-2 to Box 2 (OUT).

| Connection Point | Wire To Connect                               | Notes                                     |
| :--------------- | :-------------------------------------------- | :---------------------------------------- |
| **LINE (Brass)** | Black wire from Panel                         | Incoming Hot                              |
| **LINE (Silver)**| White wire from Panel                         | Incoming Neutral                          |
| **LOAD (Brass)** | Black wire to Box 2                           | Outgoing (Protected) Hot                  |
| **LOAD (Silver)**| White wire to Box 2                           | Outgoing (Protected) Neutral              |
| **Ground Screw** | Pigtail from ground wire nut                  |                                           |
| **Wire Nut #1**  | Bare grounds from both cables + pigtail       | Connects all grounds together.            |

---

### Box 2: The Distribution Hub
*   **Purpose**: The most important box. It houses the first switches for both lights and distributes power.
*   **Cables**: 14-2 from Box 1 (IN), 14-3 to Box 4 (OUT), 14-3 to Box 7 (OUT).

#### Wire Nut Connections in Box 2
-   **Wire Nut #1 (HOT)**:
    -   Black wire from Box 1 (Incoming Hot)
    -   Pigtail to Main SW 1 (COM terminal)
    -   Pigtail to Vanity SW 1 (COM terminal)
    -   Black wire from 14-3 to Box 7 (Constant Hot for Fan)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 1 (Incoming Neutral)
    -   White wire from 14-3 to Box 4 (Neutral for Main Light)
    -   White wire from 14-3 to Box 7 (Neutral for Vanity Light & Fan)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground from 14-3 to Box 4
    -   Bare ground from 14-3 to Box 7
    -   Pigtail to Main SW 1 (Ground Screw)
    -   Pigtail to Vanity SW 1 (Ground Screw)

#### Device Connections in Box 2
-   **Main Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut.
    -   **T1**: Black wire from 14-3 to Box 4 (Traveler 1).
    -   **T2**: Red wire from 14-3 to Box 4 (Traveler 2).
    -   **Ground**: Pigtail from GROUND wire nut.
-   **Vanity Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut.
    -   **T1**: Red wire from 14-3 to Box 7 (Traveler).
    -   **T2**: **NOT CONNECTED**. The black wire in this cable is used for constant hot, not a traveler.
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Box 4: Main Light Switch 2
*   **Purpose**: Houses the second 3-way switch for the main light.
*   **Cables**: 14-3 from Box 2 (IN), 14-2 to Main Light (OUT).

#### Wire Nut Connections in Box 4
-   **Wire Nut #1 (NEUTRAL)**:
    -   White wire from Box 2.
    -   White wire to Main Light.
-   **Wire Nut #2 (GROUND)**:
    -   Bare ground from Box 2.
    -   Bare ground to Main Light.
    -   Pigtail to the switch's ground screw.

#### Device Connections in Box 4
-   **Main Switch 2 (3-Way)**:
    -   **COM**: Black wire to Main Light (Switched Hot to light).
    -   **T1**: Black wire from Box 2 (Traveler).
    -   **T2**: Red wire from Box 2 (Traveler).
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Box 7: Combined Switch Box
*   **Purpose**: Houses the second vanity switch and the fan switch.
*   **Cables**: 14-3 from Box 2 (IN), 14-2 to Vanity Light (OUT), 14-2 to Fan (OUT).

#### Wire Nut Connections in Box 7
-   **Wire Nut #1 (HOT for Fan)**:
    -   Black wire from Box 2 (Constant Hot).
    -   Pigtail to Fan Switch (Top Terminal).
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 2 (Neutral).
    -   White wire to Vanity Light.
    -   White wire to Fan.
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 2.
    -   Bare ground to Vanity Light.
    -   Bare ground to Fan.
    -   Pigtail to Vanity SW 2 (Ground Screw).
    -   Pigtail to Fan Switch (Ground Screw).

#### Device Connections in Box 7
-   **Vanity Switch 2 (3-Way)**:
    -   **COM**: Black wire to Vanity Light (Switched Hot).
    -   **T1**: Red wire from Box 2 (Traveler from Vanity SW 1).
    -   **T2**: **NOT CONNECTED**.
    -   **Ground**: Pigtail from GROUND wire nut.
-   **Fan Switch (Single-Pole)**:
    -   **Top Terminal**: Pigtail from HOT wire nut.
    -   **Bottom Terminal**: Black wire to Fan (Switched Hot).
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Fixture Boxes (Main Light, Vanity Light, Fan)
The wiring is straightforward. In each box:
-   Connect the black wire from the switch to the fixture's hot wire/terminal.
-   Connect the white wire to the fixture's neutral wire/terminal.
-   Connect the bare ground wire to the fixture's ground screw/wire.
