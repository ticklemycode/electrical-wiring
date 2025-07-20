# Comprehensive Wiring Guide (Box-by-Box)

This guide provides detailed, step-by-step wiring instructions for each electrical box in the final, optimized bathroom circuit.

## ⚠️ Critical Safety Reminders
- **Turn off power** at the breaker before beginning any work.
- **Use a voltage tester** to confirm the power is off.
- **No Re-identification Needed**: In this design, all wires are used for their standard purpose (black/red for hot, white for neutral). No re-identifying of wires with tape is necessary.
- **Pigtails**: Use 6-inch pigtails of the same color wire to connect devices when multiple wires are spliced in a wire nut. This improves organization and safety.

---

### Box 1: GFCI Outlet & Distribution
*   **Purpose**: Provides GFCI protection and distributes power to all circuits.
*   **Cables**: 14-2 from Panel (IN), 14-2 to Box 2 (OUT), 14-2 to Box 4 (OUT), 14-2 to Box 7 (OUT).

| Connection Point | Wire To Connect                               | Notes                                     |
| :--------------- | :-------------------------------------------- | :---------------------------------------- |
| **LINE (Brass)** | Black wire from Panel                         | Incoming Hot                              |
| **LINE (Silver)**| White wire from Panel                         | Incoming Neutral                          |
| **LOAD (Brass)** | Pigtail from HOT wire nut                     | Protected Hot to all circuits             |
| **LOAD (Silver)**| Pigtail from NEUTRAL wire nut                 | Protected Neutral to all circuits         |
| **Ground Screw** | Pigtail from GROUND wire nut                  |                                           |

#### Wire Nut Connections in Box 1
-   **Wire Nut #1 (HOT)**: 
    -   GFCI LOAD Hot wire
    -   Black wire to Box 2 (Vanity circuit)
    -   Black wire to Box 4 (Main circuit)  
    -   Black wire to Box 7 (Fan circuit)
-   **Wire Nut #2 (NEUTRAL)**:
    -   GFCI LOAD Neutral wire
    -   White wire to Box 2 (Vanity circuit)
    -   White wire to Box 4 (Main circuit)
    -   White wire to Box 7 (Fan circuit)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Panel
    -   Bare ground to Box 2
    -   Bare ground to Box 4  
    -   Bare ground to Box 7
    -   Pigtail to GFCI Ground Screw

---

### Box 2: Vanity Switch 1
*   **Purpose**: Houses the first 3-way switch for the vanity light.
*   **Cables**: 14-2 from Box 1 (IN), 14-3 to Box 7 (OUT).

#### Wire Nut Connections in Box 2
-   **Wire Nut #1 (NEUTRAL)**:
    -   White wire from Box 1 (Incoming Neutral)
    -   White wire to Box 7 (Neutral for Vanity Light circuit)
-   **Wire Nut #2 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground to Box 7
    -   Pigtail to Vanity SW 1 (Ground Screw)

#### Device Connections in Box 2
-   **Vanity Switch 1 (3-Way)**:
    -   **COM**: Black wire from Box 1 (Constant Hot)
    -   **T1**: Black wire to Box 7 (Traveler 1)
    -   **T2**: Red wire to Box 7 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut

---

### Box 4: Main Light Switch 1
*   **Purpose**: Houses the first 3-way switch for the main light.
*   **Cables**: 14-2 from Box 1 (IN), 14-3 to Box 7 (OUT).

#### Wire Nut Connections in Box 4
-   **Wire Nut #1 (NEUTRAL)**:
    -   White wire from Box 1 (Incoming Neutral)
    -   White wire to Box 7 (Neutral for Main Light circuit)
-   **Wire Nut #2 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground to Box 7
    -   Pigtail to Main SW 1 (Ground Screw)

#### Device Connections in Box 4
-   **Main Switch 1 (3-Way)**:
    -   **COM**: Black wire from Box 1 (Constant Hot)
    -   **T1**: Black wire to Box 7 (Traveler 1)
    -   **T2**: Red wire to Box 7 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut

---

### Box 7: Control Center (Triple Gang Box)
*   **Purpose**: Houses all the second switches and controls all fixtures.
*   **Cables**: 14-2 from Box 1 (IN), 14-3 from Box 2 (IN), 14-3 from Box 4 (IN), 14-2 to Box 3 (OUT), 14-2 to Box 5 (OUT), 14-2 to Box 6 (OUT).

#### Wire Nut Connections in Box 7
-   **Wire Nut #1 (HOT for Fan)**:
    -   Black wire from Box 1 (Constant Hot for Fan)
    -   Pigtail to Fan Switch (Top Terminal)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 2 (Neutral from Vanity circuit)
    -   White wire from Box 4 (Neutral from Main circuit)
    -   White wire to Box 3 (Vanity Light)
    -   White wire to Box 5 (Main Light)
    -   White wire to Box 6 (Fan)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground from Box 2
    -   Bare ground from Box 4
    -   Bare ground to Box 3 (Vanity Light)
    -   Bare ground to Box 5 (Main Light)
    -   Bare ground to Box 6 (Fan)
    -   Pigtail to Main SW 2 (Ground Screw)
    -   Pigtail to Vanity SW 2 (Ground Screw)
    -   Pigtail to Fan Switch (Ground Screw)

#### Device Connections in Box 7
-   **Main Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 5 (Switched Hot to Main Light)
    -   **T1**: Black wire from Box 4 (Traveler 1)
    -   **T2**: Red wire from Box 4 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut
-   **Vanity Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 3 (Switched Hot to Vanity Light)
    -   **T1**: Black wire from Box 2 (Traveler 1)
    -   **T2**: Red wire from Box 2 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut
-   **Fan Switch (Single-Pole)**:
    -   **Hot Terminal**: Pigtail from HOT wire nut
    -   **Load Terminal**: Black wire to Box 6 (Switched Hot to Fan)
    -   **Ground**: Pigtail from GROUND wire nut

---

### Fixture Boxes (Main Light, Vanity Light, Fan)
The wiring is straightforward. In each box:
-   Connect the black wire from the switch to the fixture's hot wire/terminal.
-   Connect the white wire to the fixture's neutral wire/terminal.
-   Connect the bare ground wire to the fixture's ground screw/wire.
