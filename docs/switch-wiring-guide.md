# Comprehensive Wiring Guide (Box-by-Box)

This guide provides detailed, step-by-step wiring instructions for each electrical box in the final, optimized bathroom circuit.

## ⚠️ Critical Safety Reminders
- **Turn off power** at the breaker before beginning any work.
- **Use a voltage tester** to confirm the power is off.
- **No Re-identification Needed**: In this design, all wires are used for their standard purpose (black/red for hot, white for neutral). No re-identifying of wires with tape is necessary.
- **Pigtails**: Use 6-inch pigtails of the same color wire to connect devices when multiple wires are spliced in a wire nut. This improves organization and safety.

---

### Box 1: GFCI Outlet (Simple Design)
*   **Purpose**: Provides GFCI protection for entire circuit.
*   **Cables**: 14-2 from Panel (IN), 14-2 to Box 2 (OUT).

| Connection Point | Wire To Connect                               | Notes                                     |
| :--------------- | :-------------------------------------------- | :---------------------------------------- |
| **LINE (Brass)** | Black wire from Panel                         | Incoming Hot                              |
| **LINE (Silver)**| White wire from Panel                         | Incoming Neutral                          |
| **LOAD (Brass)** | Black wire to Box 2                           | Protected Hot to circuit                  |
| **LOAD (Silver)**| White wire to Box 2                           | Protected Neutral to circuit              |
| **Ground Screw** | Pigtail from ground wire nut                  |                                           |

#### Wire Nut Connections in Box 1
-   **Wire Nut #1 (GROUND)**:
    -   Bare ground from Panel
    -   Bare ground to Box 2  
    -   Pigtail to GFCI Ground Screw

---

### Box 2: Vanity Switch 1 & Power Distribution
*   **Purpose**: Houses vanity 3-way switch AND distributes power downstream.
*   **Cables**: 14-2 from Box 1 (IN), 14-2 to Box 4 (OUT), 14-3 to Box 7 (3-way), 14-2 to Box 3 (Vanity Light).

#### Wire Nut Connections in Box 2
-   **Wire Nut #1 (HOT DISTRIBUTION)**:
    -   Black wire from Box 1 (Incoming Hot)
    -   Black wire to Box 4 (Power continuation)
    -   Pigtail to Vanity SW 1 (COM terminal)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 1 (Incoming Neutral)
    -   White wire to Box 4 (Neutral continuation)
    -   White wire from Box 7 (via 14-3 - Neutral for vanity light)
    -   White wire to Box 3 (Vanity Light neutral)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 1
    -   Bare ground to Box 4
    -   Bare ground to/from Box 7
    -   Bare ground to Box 3 (Vanity Light)
    -   Pigtail to Vanity SW 1 (Ground Screw)

#### Device Connections in Box 2
-   **Vanity Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut
    -   **T1**: Black wire to Box 7 (Traveler 1)
    -   **T2**: Red wire to Box 7 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut

---

### Box 4: Main Light Switch 1 & Power Distribution
*   **Purpose**: Houses main 3-way switch AND distributes power to Box 7.
*   **Cables**: 14-2 from Box 2 (IN), 14-2 to Box 7 (OUT), 14-3 to Box 7 (3-way), 14-2 to Box 5 (Main Light).

#### Wire Nut Connections in Box 4
-   **Wire Nut #1 (HOT DISTRIBUTION)**:
    -   Black wire from Box 2 (Incoming Hot)
    -   Black wire to Box 7 (Power continuation)
    -   Pigtail to Main SW 1 (COM terminal)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 2 (Incoming Neutral)
    -   White wire to Box 7 (Neutral continuation) 
    -   White wire from Box 7 (via 14-3 - Neutral for main light)
    -   White wire to Box 5 (Main Light neutral)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 2
    -   Bare ground to Box 7 (via 14-2)
    -   Bare ground to/from Box 7 (via 14-3)
    -   Bare ground to Box 5 (Main Light)
    -   Pigtail to Main SW 1 (Ground Screw)

#### Device Connections in Box 4
-   **Main Switch 1 (3-Way)**:
    -   **COM**: Pigtail from HOT wire nut
    -   **T1**: Black wire to Box 7 (Traveler 1)
    -   **T2**: Red wire to Box 7 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut

---

### Box 7: Control Center (Triple Gang Box) - End of Feed
*   **Purpose**: Houses second switches for both 3-way circuits and fan switch.
*   **Cables**: 14-2 from Box 4 (IN), 14-3 from Box 2 (3-way), 14-3 from Box 4 (3-way), 14-2 to Box 6 (Fan).

#### Wire Nut Connections in Box 7  
-   **Wire Nut #1 (HOT for Fan)**:
    -   Black wire from Box 4 (Incoming Hot)
    -   Pigtail to Fan Switch (Hot terminal)
-   **Wire Nut #2 (NEUTRAL)**:
    -   White wire from Box 4 (Incoming Neutral)
    -   White wire to Box 2 (via 14-3 - for vanity light return)
    -   White wire to Box 4 (via 14-3 - for main light return)
    -   White wire to Box 6 (Fan neutral)
-   **Wire Nut #3 (GROUND)**:
    -   Bare ground from Box 4 (via 14-2)
    -   Bare ground to/from Box 2 (via 14-3)
    -   Bare ground to/from Box 4 (via 14-3)
    -   Bare ground to Box 6 (Fan)
    -   Pigtail to Main SW 2 (Ground Screw)
    -   Pigtail to Vanity SW 2 (Ground Screw)
    -   Pigtail to Fan Switch (Ground Screw)

#### Device Connections in Box 7
-   **Vanity Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 3 (Switched Hot - routed back through Box 2)
    -   **T1**: Black wire from Box 2 (Traveler 1)
    -   **T2**: Red wire from Box 2 (Traveler 2)
    -   **Ground**: Pigtail from GROUND wire nut
-   **Main Switch 2 (3-Way)**:
    -   **COM**: Black wire to Box 5 (Switched Hot - routed back through Box 4)
    -   **T1**: Black wire from Box 4 (Traveler 1)
    -   **T2**: Red wire from Box 4 (Traveler 2)
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
