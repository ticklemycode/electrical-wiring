# Comprehensive Wiring Guide (Box-by-Box)

This guide provides detailed, step-by-step wiring instructions for each electrical box in the optimized bathroom circuit.

## ⚠️ Critical Safety Reminders
- **Turn off power** at the breaker before beginning any work.
- **Use a voltage tester** to confirm the power is off.
- **Re-identify wires** as required by the NEC. In this corrected design, all white wires carry neutrals - no white wire re-identification is required.
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
*   **Purpose**: The most important box. It houses two 3-way switches and distributes power to the rest of the circuit.
*   **Cables**: 14-2 from Box 1 (IN), 14-3 to Box 4 (OUT), 14-3 to Box 7 (OUT).

#### Wire Nut Connections in Box 2
-   **Wire Nut #1 (HOT)**:
    -   Black wire from Box 1 (Incoming Hot)
    -   Pigtail to Vanity SW 1 (COM terminal)
    -   Pigtail to Main SW 1 (COM terminal)
    -   Black wire from 14-3 to Box 7 (Constant Hot for Fan)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 1 (Incoming Neutral)
    -   White wire from 14-3 to Box 4 (Neutral for Main Light)
    -   White wire from 14-3 to Box 7 (Neutral for Vanity Light & Fan)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground from 14-3 to Box 4
    -   Bare ground from 14-3 to Box 7
    -   Pigtail to Vanity SW 1 (Ground Screw)
    -   Pigtail to Main SW 1 (Ground Screw)

#### Device Connections in Box 2
-   **Vanity Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut.
    -   **T1**: Red wire from 14-3 to Box 7 (Traveler).
    -   **T2**: **NOT CONNECTED** (single traveler design).
    -   **Ground**: Pigtail from GROUND wire nut.
-   **Main Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut.
    -   **T1**: Black wire from 14-3 to Box 4 (Traveler 1).
    -   **T2**: Red wire from 14-3 to Box 4 (Traveler 2).
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Box 4: Main Light Switch 2
*   **Purpose**: Houses the second 3-way switch for the main light.
*   **Cables**: 14-3 from Box 2 (IN), 14-2 to Box 5 (Main Light) (OUT).

#### Wire Nut Connections in Box 4
-   **Wire Nut #1 (NEUTRAL)**:
    -   White wire from Box 2.
    -   White wire to Box 5.
-   **Wire Nut #2 (GROUND)**:
    -   Bare ground from Box 2.
    -   Bare ground to Box 5.
    -   Pigtail to the switch's ground screw.

#### Device Connections in Box 4
-   **Main Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 5 (Switched Hot to light).
    -   **T1**: Black wire from Box 2 (Traveler).
    -   **T2**: Red wire from Box 2 (Traveler).
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Box 7: Combined Switch Box
*   **Purpose**: Houses the second vanity switch and the fan switch.
*   **Cables**: 14-3 from Box 2 (IN), 14-2 to Box 3 (Vanity Light) (OUT), 14-2 to Box 6 (Fan) (OUT).

#### Wire Nut Connections in Box 7
-   **Wire Nut #1 (HOT)**:
    -   Black wire from Box 2 (Constant Hot).
    -   Pigtail to Fan Switch (LINE terminal).
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 2 (Neutral).
    -   White wire to Box 3 (Vanity Light Neutral).
    -   White wire to Box 6 (Fan Neutral).
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 2.
    -   Bare ground to Box 3.
    -   Bare ground to Box 6.
    -   Pigtail to Vanity SW 2 (Ground Screw).
    -   Pigtail to Fan Switch (Ground Screw).

#### Device Connections in Box 7
-   **Vanity Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 3 (Switched Hot to vanity light).
    -   **T1**: Red wire from Box 2 (Traveler from Vanity SW 1).
    -   **T2**: **NOT CONNECTED** (single traveler design).
    -   **Ground**: Pigtail from GROUND wire nut.
-   **Fan Switch (Single-Pole)**:
    -   **Top Terminal**: Pigtail from HOT wire nut.
    -   **Bottom Terminal**: Black wire to Box 6 (Switched Hot to fan).
    -   **Ground**: Pigtail from GROUND wire nut.

---

### Boxes 3, 5, and 6: Fixture Boxes
These boxes are for the light fixtures and the fan. The wiring is straightforward.

-   **Box 3 (Vanity Light)**:
    -   Connect the black and white wires from the 14-2 cable (from Box 7) to the corresponding wires on the light fixture.
    -   Connect the bare ground wire to the fixture's ground screw/wire.
-   **Box 5 (Main Light)**:
    -   Connect the black and white wires from the 14-2 cable (from Box 4) to the corresponding wires on the light fixture.
    -   Connect the bare ground wire to the fixture's ground screw/wire.
-   **Box 6 (Exhaust Fan)**:
    -   Connect the black and white wires from the 14-2 cable (from Box 7) to the corresponding wires on the fan.
    -   Connect the bare ground wire to the fan's ground screw/wire.
