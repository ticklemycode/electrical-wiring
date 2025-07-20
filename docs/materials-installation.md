# Materials List and Installation Guide

## Required Materials

### Electrical Wire
| Item              | Quantity | Specification                | Usage                                     |
| ----------------- | -------- | ---------------------------- | ----------------------------------------- |
| 14-2 NM-B Cable   | 50 feet  | 14 AWG, 2 conductor + ground | Power feeds, single fixture connections   |
| 14-3 NM-B Cable   | 25 feet  | 14 AWG, 3 conductor + ground | Runs from hub to downstream switch boxes  |
| Wire Nuts         | 1 box    | Red/Yellow Assortment        | Splicing wires                            |
| Electrical Tape   | 1 roll   | Black, 3/4" x 60'            | Securing wire nuts (optional)             |

### Electrical Devices
| Item               | Quantity | Specification         | Notes                                     |
| ------------------ | -------- | --------------------- | ----------------------------------------- |
| GFCI Outlet        | 1        | 15A, 120V, Self-Test  | Must be first device in circuit (Box 1)   |
| 3-Way Switches     | 4        | 15A, 120V             | 2 for main, 2 for vanity                  |
| Single Pole Switch | 1        | 15A, 120V             | For exhaust fan                           |
| Switch Plates      | 3        | Appropriate gang sizes| For Boxes 2, 4, and 7                     |

### Electrical Boxes
| Item                   | Quantity | Specification         | Usage                                     |
| ---------------------- | -------- | --------------------- | ----------------------------------------- |
| Single Gang Box        | 2        | 18 cubic inch         | Box 2 (Vanity SW 1), Box 4 (Main SW 1)   |
| Triple Gang Box        | 1        | 40+ cubic inch        | Box 7 (Control Center - 3 switches)      |
| Outlet Box             | 1        | Standard single gang  | Box 1 (GFCI)                              |
| Ceiling/Wall Boxes     | 3        | Rated for fixture weight | Box 3, Box 5, Box 6 (Fixtures)        |

## Installation Guide

### Step 1: Safety First
- **Turn OFF power** at the main electrical panel.
- Use a non-contact voltage tester to confirm power is off at the circuit.
- Always follow local electrical codes and NEC guidelines.

### Step 2: Cable Routing (Corrected Design)
Run cables according to the revised layout.
1.  **Panel → Box 1 (GFCI)**: Run one **14-2** cable.
2.  **Box 1 → Box 7 (Control Center)**: Run one **14-2** cable from the GFCI's LOAD terminals.
3.  **Box 7 → Box 2 (Vanity SW 1)**: Run one **14-3** cable (Hot + 2 Travelers + Neutral).
4.  **Box 7 → Box 4 (Main SW 1)**: Run one **14-3** cable (Hot + 2 Travelers + Neutral).
5.  **Box 7 → Box 3 (Vanity Light)**: Run one **14-2** cable.
6.  **Box 7 → Box 5 (Main Light)**: Run one **14-2** cable.
7.  **Box 7 → Box 6 (Fan)**: Run one **14-2** cable.

**Key Design Feature**: Box 7 acts as both the control center AND power distribution hub. It receives power from the GFCI and distributes it to the remote switches (Box 2 and Box 4) while also controlling all fixtures directly. This design ensures proper GFCI protection for all circuits.

### Step 3: GFCI Outlet Wiring (Box 1)
- Connect the incoming 14-2 cable from the panel to the **LINE** terminals.
- Connect the outgoing 14-2 cable (to Box 2) to the **LOAD** terminals.
- **Black to Brass (Hot)**, **White to Silver (Neutral)**, **Bare to Green (Ground)**.
- **CRITICAL**: Correct LINE/LOAD wiring is essential for GFCI protection.

### Step 4: Switch and Fixture Wiring
- Refer to the `switch-wiring-guide.md` for detailed, box-by-box connection instructions.
- Ensure all ground wires are connected in every box.
- Use wire nuts to create secure splices.

### Step 5: Final Checks and Testing
- Double-check all connections against the diagrams.
- Ensure no bare wires are exposed.
- Turn the power back on and test every switch and the GFCI outlet.
