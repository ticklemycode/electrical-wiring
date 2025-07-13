# 3-Way Switch Wiring Guide

## Understanding 3-Way Switches

3-way switches allow you to control a single light fixture from two different locations. This is essential for the main light and vanity light in your bathroom configuration.

## 3-Way Switch Terminal Identification

```
    3-Way Switch
   ┌─────────────┐
   │    COM      │ ← Common terminal (darker colored screw)
   │             │
   │  T1     T2  │ ← Traveler terminals (brass colored screws)
   │             │
   │   [GND]     │ ← Ground wire (pigtail or push-in connection)
   └─────────────┘
```

## Main Light 3-Way Wiring Configuration

### Switch Box 1 (Main Switch 1):
```
INCOMING POWER → 14-3 Cable to Switch 2 → 14-3 Cable to Light

Power Source (14-2):          To Switch 2 (14-3):         To Light (14-3):
- Hot (Black)    →  COM       - Traveler 1 (Red)   →  T1  - Switched Hot → COM
- Neutral (White) → Pigtail   - Traveler 2 (Black) →  T2  - Neutral     → Light
- Ground (Bare)   → Switch    - Ground (Bare)      →  GND - Ground      → GND
```

### Switch Box 2 (Main Switch 2):
```
From Switch 1 (14-3):         To Light Fixture (14-2):
- Traveler 1 (Red)   →  T1    - Switched Hot (Black) →  COM
- Traveler 2 (Black) →  T2    - Neutral (White)      →  Pigtail
- Ground (Bare)      →  GND   - Ground (Bare)        →  Switch
```

## Vanity Light 3-Way Wiring Configuration

**IMPORTANT**: The vanity light operates as a 3-way switched light where the switching junction occurs **at the light fixture**. Power flows from GFCI to Vanity Switch 1, then through the vanity light fixture to create the switching junction for Vanity Switch 2.

### Vanity Switch 1 (Receives Power from GFCI):
```
From GFCI (14-2 Cable):          To Vanity Light (14-3):        
- Hot (Black)     →  COM         - Black (from COM) → White to VS2 junction
- Neutral (White) →  Pass-through - White (from T2)  → Light fixture hot
- Ground (Bare)   →  Switch ground- Red (from T1)    → Red pass-through to VS2
                                 - Neutral (White)   → Pass-through to circuit
                                 - Ground (Green)    → Continue to VS2
```

### How Vanity Light Switching Works:
The vanity light uses **3-way switch control through the fixture** where:
1. **Hot wire**: From GFCI to Vanity Switch 1 COM terminal
2. **Black from VS1**: Connected to white wire going to VS2 in light fixture
3. **White from VS1**: Direct hot feed to vanity light fixture
4. **Red wire**: Pass-through traveler between VS1 and VS2 via light fixture
5. **Black from light**: Switched hot return to VS2 T2 terminal
6. **Light turns ON**: When switch positions complete the circuit through VS2

**Important**: This is normal 3-way switching - both switches control the same light.

### Combined Switch Box (Main Switch 1, Vanity Switch 2, Fan Switch):

#### Main Switch 1 (3-Way for Main Light):
```
Wire Connections in Combined Box:
- Hot (spliced from incoming) →  COM      - Traveler 1 (Red)   →  T1 (to Main Switch 2)
- Red (from Main Switch 2)    →  T1       - Traveler 2 (Black) →  T2 (to Main Switch 2)  
- Black (from Main Switch 2)  →  T2       - Switched Hot       →  COM (to main light)
- Ground (from ground bundle) →  Switch ground
```

#### Vanity Switch 2 (3-Way for Vanity Light):
```
Wire Connections in Combined Box:
- White from Light Fixture   →  COM      - This carries hot from VS1 black
- Red (from Vanity Switch 1) →  T1       - Red traveler pass-through
- Black (from Light Fixture)→  T2       - Black switched hot from fixture
- Ground (from ground bundle)→  Switch ground
```

#### Fan Switch (Single Pole):
```
Wire Connections in Combined Box:
- Hot (spliced from incoming) →  LINE     - Switched Hot       →  LOAD (to fan)
- Ground (from ground bundle) →  Switch ground
```

**Key Point**: The vanity light turns ON/OFF normally from either switch. The 3-way switches control the **hot path** to complete the circuit.

## How Vanity Light 3-Way Switching Works

**Critical Understanding**: The vanity light operates like a normal 3-way switched light - it can be turned ON and OFF from either switch location.

### Power Flow Explanation:
```
1. GFCI provides HOT → Vanity Switch 1 COM terminal
                    ↓
2. VS1 black output → Connected to white wire to VS2 (at light fixture)
                    ↓
3. VS1 white output → Direct to vanity light fixture (hot feed)
                    ↓
4. Light fixture black → VS2 T2 terminal (switched hot return)
                    ↓
5. VS1 red traveler → VS2 red traveler (switching control)
                    ↓
6. When VS1 & VS2 positions complete path → Light ON
   When positions break path → Light OFF
```

### What Each Wire Does:
- **Black from GFCI**: Provides hot to VS1 COM terminal  
- **Black from VS1**: Connected to white wire going to VS2 (switching junction)
- **White from VS1**: Direct hot feed to vanity light fixture
- **Red in 14-3 cable**: Traveler wire pass-through between VS1 and VS2 via fixture
- **Black from light fixture**: Switched hot output to VS2 T2 terminal  
- **White (neutral)**: Direct path through circuit for other devices
- **Ground**: Safety ground for all devices

### The Switching Logic:
- **Both switches same position**: Circuit complete → Vanity light ON
- **Switches different positions**: Circuit broken → Vanity light OFF
- **Either switch can control**: Normal 3-way operation

**Key Point**: The vanity light operates completely normally - you can turn it on and off from either switch location just like any other 3-way switched light.

## Wire Color Code Standards

### 14-2 Cable (contains one of each):
- **⚫ Black**: Hot (Line/Load)
- **⚪ White**: Neutral
- **🟢 Bare/Green**: Ground

### 14-3 Cable (contains one of each):
- **⚫ Black**: Hot or Traveler (used for hot lines and black traveler)
- **🔴 Red**: Traveler (only used between 3-way switches)
- **⚪ White**: Neutral (sometimes used as traveler when properly marked)
- **🟢 Bare/Green**: Ground

**Important**: All hot wires are black (⚫). Red (🔴) is only used for the red traveler wire in 3-way switch circuits.

## Fixture Wiring Guide

### Complete Wire Color Connections for Entire Circuit

#### GFCI Outlet to Vanity Light Fixture (14-2 Cable):
```
GFCI LOAD Side → Vanity Light Junction Box:
- Black (Hot) ────────→ Black fixture wire (always hot)
- White (Neutral) ────→ White fixture wire (neutral return)
- Bare (Ground) ──────→ Green fixture wire + box ground
```

#### Vanity Light Fixture Connections:
```
Junction Box Connections (3-Way Switching Junction):
┌────────────────────────────────────────────────────────────┐
│ From VS1 (14-3)        │ To VS2 (14-3)     │ To Fixture    │
│                        │                   │               │
│ Black (from VS1 COM) ──┼→ White to VS2 ────┼→ (junction)   │
│                        │   (switching hot) │               │
│ White (from VS1 T2) ───┼→ Fixture Hot ─────┼→ Light Hot    │
│                        │   (direct feed)   │               │
│ Red (from VS1 T1) ─────┼→ Red to VS2 ──────┼→ (pass-thru)  │
│                        │   (traveler)      │               │
│ Fixture Black ─────────┼→ Black to VS2 ────┼→ Light Return │
│   (switched return)    │   (to T2 terminal)│               │
│                        │                   │               │
│ Neutral (White) ───────┼→ Neutral continue ─┼→ Fixture Neut │
│                        │   (to circuit)    │               │
│                        │                   │               │
│ Ground (Green) ────────┼→ Ground continue ──┼→ Fixture Grnd │
│                        │   (to circuit)    │               │
└────────────────────────────────────────────────────────────┘

Note: Vanity light switching junction occurs AT THE FIXTURE.
      VS1 and VS2 coordinate through this junction point.
```

#### Main Light Fixture Connections:
```
Main Light Junction Box:
┌──────────────────────────────────────────┐
│ From Switch 2 (14-3) │ To Fan (14-2)     │
│                      │                   │
│ Switched Hot (Black) ┼→ Hot to fan (pass) │
│       │              │                   │
│       └─────────────→ Fixture Hot (Black)│
│                      │                   │
│ Neutral (White) ─────┼→ Neutral (White)  │
│       │              │                   │
│       └─────────────→ Fixture Neutral    │
│                      │                   │
│ Ground (Bare) ───────┼→ Ground (Bare)    │
│       │              │                   │
│       └─────────────→ Fixture Ground     │
└──────────────────────────────────────────┘

Note: Main light receives switched hot from 3-way switch system
```

#### Exhaust Fan Fixture Connections:
```
Fan Junction Box (Pass-Through + Control):
┌──────────────────────────────────────────┐
│ From Main Light (14-2) │ To Switches (14-3) │
│                        │                     │
│ Hot (Black) ───────────┼→ Hot continue (Black)│
│       │                │                     │
│       └── Control wire from fan switch ─────┐│
│                                             ││
│ Fan Motor Connections:                      ││
│ - Hot from switch ←─────────────────────────┘│
│ - Neutral (White) ←─ Neutral (White)        │
│ - Ground (Bare) ←─── Ground (Bare)          │
└──────────────────────────────────────────────┘

Note: Fan gets power from separate control wire from fan switch
```

### Fixture Wiring Color Code Summary:

#### Standard Fixture Wire Colors:
- **Black**: Hot (power input to fixture)
- **White**: Neutral (return path from fixture)
- **Green or Bare Copper**: Ground (safety connection)

#### Circuit Wire Color Functions:
1. **Always Hot Circuits** (Vanity Light):
   - Black: Hot available at fixture + switch feed (power source)
   - White: Direct neutral path (not switched)
   - Bare: Ground for safety
   - **Red: Traveler wire between switches (NOT to fixture)**

2. **Switched Hot Circuits** (Main Light):
   - Black: Switched hot from 3-way switches
   - White: Neutral return to panel
   - Bare: Ground for safety

3. **Controlled Circuits** (Exhaust Fan):
   - Black: Hot pass-through + switched control
   - White: Neutral return to panel
   - Bare: Ground for safety

## Detailed Fixture Installation Steps

### Vanity Light Installation:
```
Step-by-Step Connection:
1. Turn OFF power at breaker
2. Test with voltage tester
3. Identify fixture wires:
   - Black (or red) = Hot input
   - White = Neutral
   - Green/Bare = Ground
4. Connect in junction box:
   - Circuit black → Fixture black (wire nut)
   - Circuit white → Fixture white (wire nut)
   - Circuit ground → Fixture ground + box ground (wire nut)
5. Mount fixture to box
6. Install bulbs and test
```

### Main Light Installation:
```
Step-by-Step Connection:
1. Verify switched hot available at box
2. Connect fixture wires:
   - Switched hot (black) → Fixture hot (black)
   - Neutral (white) → Fixture neutral (white)  
   - Ground (bare) → Fixture ground (green/bare)
3. Ensure proper support for fixture weight
4. Test 3-way switch operation from both locations
```

### Exhaust Fan Installation:
```
Special Fan Wiring Considerations:
1. Fan receives power from control wire (not pass-through hot)
2. Connection sequence:
   - Control black from switch → Fan black
   - Circuit neutral (white) → Fan white
   - Circuit ground (bare) → Fan ground
3. Pass-through hot continues to switches (no fan connection)
4. Test fan operation from fan switch
```

### Junction Box Wire Management:

#### Proper Wire Nut Sizing:
- **Yellow wire nuts**: 2-3 wires (14 AWG)
- **Red wire nuts**: 3-4 wires (14 AWG)
- **Blue wire nuts**: 4-5 wires (14 AWG)

#### Wire Splicing Best Practices:
1. **Strip wires**: 3/4" of insulation
2. **Twist together**: Clockwise direction
3. **Apply wire nut**: Hand-tight plus 1/4 turn
4. **Tug test**: Gentle pull to verify connection
5. **Tape if needed**: Additional security for multiple wires

### Fixture-Specific Wiring Notes:

#### LED Fixtures:
- **Compatibility**: Verify with dimmer switches if used
- **Neutral required**: Always connect white wire
- **Grounding**: Essential for metal fixtures

#### Fan/Light Combinations:
- **Separate controls**: May require additional switching
- **Wire capacity**: Ensure box can handle extra connections
- **Load calculations**: Add both fan and light wattage

#### Moisture Considerations:
- **Bathroom rating**: All fixtures must be bathroom-rated
- **GFCI protection**: Required for all bathroom circuits
- **Proper sealing**: Use appropriate gaskets and mounting

## Complete Circuit Wire Flow Guide

### Circuit Path Overview (From Panel to Each Device)

```
ELECTRICAL PANEL (15A Breaker)
      ↓ 14-2 Cable
  GFCI OUTLET (power source)
      ↓ 14-2 Cable  
  VANITY LIGHT ──→ Vanity Switches (3-way control)
      ↓ 14-3 Cable (via switches)
  MAIN LIGHT ──→ Main Switches (3-way control)  
      ↓ 14-2 Cable (hot pass-through)
  EXHAUST FAN ──→ Fan Switch (single pole control)
```

### Wire-by-Wire Flow Summary

#### 🔴 HOT WIRE PATHS (Black Wires)

**Always Hot Branch:**
```
Panel → GFCI LINE → GFCI LOAD → Vanity Light (always energized)
```

**Switched Hot Branch:**  
```
Vanity Light → Vanity Switches → Main Switches → Main Light (switched)
```

**Fan Control Branch:**
```
Main Light Box → Fan Switch → Fan Motor (switched)
```

#### ⚪ NEUTRAL WIRE PATH (White Wires)
```
Panel Neutral → GFCI → Vanity → Switches → Main Light → Fan → Return to Panel
```
*Neutrals pass through switches but don't connect to switch terminals*

#### 🟢 GROUND WIRE PATH (Bare/Green Wires)
```
Panel Ground → All Devices & Metal Boxes → Return to Panel
```

### Detailed Point-to-Point Wire Connections

#### Connection 1: GFCI Outlet to Vanity Light Fixture
```
Cable: 14-2 from GFCI LOAD terminals to Vanity Light box

GFCI LOAD Side          →    Vanity Light Junction Box
├─ Black (Hot)          →    Black to vanity fixture + splice to switches
├─ White (Neutral)      →    White to vanity fixture + splice to switches  
└─ Bare (Ground)        →    Green to vanity fixture + splice to switches
```

#### Connection 2: Vanity Light to Vanity Switch 1
```
Cable: 14-3 from Vanity Light box to Vanity Switch 1 box

Vanity Light Box        →    Vanity Switch 1 Box
├─ Black (Always Hot)   →    Black to COM terminal
├─ Red (Traveler 1)     →    Red to T1 terminal
├─ Black (Traveler 2)   →    Black to T2 terminal
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 3: Vanity Switch 1 to Combined Switch Box
```
Cable: 14-3 from Vanity Switch 1 box to Combined Switch Box

Vanity Switch 1         →    Combined Switch Box
├─ Red (T1 terminal)    →    Red to Vanity Switch 2 T1 terminal
├─ Black (T2 terminal)  →    Black to Vanity Switch 2 T2 terminal
├─ White (Neutral)      →    White splice (neutral bundle)
└─ Bare (Ground)        →    Ground splice (ground bundle)
```

#### Connection 4: Combined Switch Box to Main Switch 2
```
Cable: 14-3 from Combined Switch Box to Main Switch 2 box

Combined Switch Box     →    Main Switch 2 Box
├─ Black (Main SW1 COM) →    Black to COM terminal
├─ Red (Main SW1 T1)    →    Red to T1 terminal
├─ Black (Main SW1 T2)  →    Black to T2 terminal
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 5: Main Switch 2 to Main Light Fixture
```
Cable: 14-2 from Main Switch 2 box to Main Light box

Main Switch 2 Box       →    Main Light Junction Box
├─ Black (COM terminal) →    Black to main fixture + splice to fan
├─ White (Neutral)      →    White to main fixture + splice to fan
└─ Bare (Ground)        →    Green to main fixture + splice to fan
```

#### Connection 6: Main Light Fixture to Combined Switch Box (Fan Control)
```
Cable: 14-2 from Main Light box to Combined Switch Box

Main Light Box          →    Combined Switch Box
├─ Black (Pass-through) →    Black to Fan Switch LINE terminal (hot feed)
├─ White (Neutral)      →    White to neutral bundle
└─ Bare (Ground)        →    Bare to ground bundle
```

#### Connection 7: Combined Switch Box to Exhaust Fan
```
Cable: 14-2 from Combined Switch Box to Fan box

Combined Switch Box     →    Exhaust Fan Junction Box
├─ Black (Fan SW LOAD)  →    Black to fan motor
├─ White (Neutral)      →    White to fan motor
└─ Bare (Ground)        →    Green to fan motor + fan housing
```

### Vanity Switch 1 Terminal Connections:
```
⚫ COM Terminal  ← Black hot wire from GFCI (input)
⚫ COM Terminal  → Black switched hot to vanity light (output)
🔴 T1 Terminal   → Red traveler wire to VS2 T1 (14-3 cable)
⚫ T2 Terminal   → Black traveler wire to VS2 T2 (14-3 cable)  
🟢 Ground Screw  ← Bare ground wire (spliced)
⚪ Neutral       → Wire nut only (pass-through, not connected to switch)
```

### Wire Function Summary by Location:

#### At GFCI Outlet:
- **LINE Black**: From panel breaker
- **LINE White**: From panel neutral
- **LOAD Black**: To vanity light
- **LOAD White**: To vanity light
- **Ground**: Panel and downstream ground

#### At Vanity Light:
- **Black**: Always hot (spliced: to fixture + to switches)
- **White**: Neutral (spliced: to fixture + to switches)
- **Bare**: Ground (spliced: to fixture + to switches)

#### At Main Light:
- **Black**: Switched hot from 3-way switches (to fixture + pass-through)
- **White**: Neutral (to fixture + pass-through)
- **Bare**: Ground (to fixture + pass-through)

#### At Exhaust Fan:
- **Black Pass-Through**: Continues to switches (not to fan motor)
- **Black Control**: From fan switch to fan motor
- **White**: Neutral to fan motor
- **Bare**: Ground to fan motor and case

This complete wire tracing helps ensure proper connections throughout the entire bathroom electrical circuit.

## Critical Wiring Rules

### 1. Common Terminal Usage:
- **Power Side**: Hot wire connects to COM terminal
- **Load Side**: Switched hot to fixture connects to COM terminal

### 2. Traveler Wires:
- Always use the same terminals (T1 to T1, T2 to T2) between switches
- Traveler wires carry the switched signal between switches

### 3. Neutral Handling:
- Neutral wires pass through switch boxes but don't connect to switch terminals
- Use wire nuts to splice neutral connections
- Neutral must run continuously to light fixtures

### 4. Ground Connections:
- All switches, fixtures, and metal boxes must be grounded
- **Switch grounding methods**:
  - **Pigtail method**: Green wire from switch connects to ground wire bundle
  - **Push-in connection**: Ground wire pushes into back of switch
  - **Self-grounding**: Switch grounds through mounting screws (if box is grounded)
- Bond all grounds together in each box

## Testing 3-Way Switch Operation

### Proper Operation:
1. **Both switches in same position**: Light OFF
2. **Switches in different positions**: Light ON
3. **Either switch can turn light on/off**: Regardless of other switch position

### Troubleshooting Steps:
1. **Light doesn't work at all**:
   - Check power at first switch
   - Verify hot wire on COM terminal of power switch
   - Check switched hot wire on COM terminal of load switch

2. **Light works from one switch only**:
   - Check traveler wire connections
   - Ensure T1 connects to T1, T2 connects to T2
   - Verify continuity of traveler wires

3. **Light stays on constantly**:
   - Check for crossed wires
   - Verify neutral connections
   - Check for short circuits

## Switch Box Wiring Diagrams

### Main Light Switch Box 1:
```
┌─────────────────────────────────────┐
│  Switch Box 1 (Main Light)         │
│                                     │
│  14-2 FROM PANEL    14-3 TO SWITCH2│
│  ┌─ Black (Hot)  ────── COM         │
│  │  White (Neutral) ── Splice ──┐   │
│  │  Ground ─────────── GND ──┐  │   │
│  │                           │  │   │
│  │  14-3 TO LIGHT            │  │   │
│  └─ Red (Traveler) ────── T1 │  │   │
│     Black (Traveler) ──── T2 │  │   │
│     White (Neutral) ────────┘  │   │
│     Ground ─────────────────────┘   │
└─────────────────────────────────────┘
```

### Main Light Switch Box 2:
```
┌─────────────────────────────────────┐
│  Switch Box 2 (Main Light)         │
│                                     │
│  14-3 FROM SWITCH1  14-2 TO LIGHT  │
│  ┌─ Red (Traveler) ────── T1        │
│  │  Black (Traveler) ──── T2        │
│  │  White (Neutral) ─── Splice ──┐  │
│  │  Ground ─────────── GND ──┐   │  │
│  │                           │   │  │
│  │  TO LIGHT FIXTURE         │   │  │
│  └─ Black (Switched) ──── COM │   │  │
│     White (Neutral) ─────────┘   │  │
│     Ground ──────────────────────┘  │
└─────────────────────────────────────┘
```

## Combined Switch Box Configuration

**IMPORTANT**: Main Switch 1, Vanity Switch 2, and Fan Switch are all located in the same electrical box. This simplifies wiring significantly as all three switches share common neutral and ground connections.

### Physical Switch Layout:
```
Combined Switch Box Contains:
├─ Main Switch 1 (3-Way)     - Controls main light
├─ Vanity Switch 2 (3-Way)   - Controls vanity light  
└─ Fan Switch (Single Pole)  - Controls exhaust fan

Shared Connections in Box:
├─ Neutral Bundle: All white wires spliced together (not to switches)
├─ Ground Bundle: All grounds + switch grounds spliced together
└─ Hot Distribution: Fed from vanity switch chain
```

### Wire Routing to Combined Switch Box:
```
From Vanity Switch 1 → To Combined Switch Box (14-3):
├─ Black (Hot) ────────→ Feeds all three switches
├─ Red (Traveler) ─────→ Vanity Switch 2 T1 terminal
├─ Black (Traveler) ───→ Vanity Switch 2 T2 terminal  
├─ White (Neutral) ────→ Neutral bundle (wire nut)
└─ Bare (Ground) ──────→ Ground bundle (wire nut)

From Combined Switch Box → To Main Switch 2
├─ Black (Switched) ───→ From Main Switch 1 COM terminal
├─ Red (Traveler) ─────→ Main Switch 1 T1 terminal
├─ Black (Traveler) ───→ Main Switch 1 T2 terminal
├─ White (Neutral) ────→ From neutral bundle
└─ Bare (Ground) ──────→ From ground bundle

From Combined Switch Box → To Fan (14-2):
├─ Black (Switched) ───→ From Fan Switch LOAD terminal
├─ White (Neutral) ────→ From neutral bundle  
└─ Bare (Ground) ──────→ From ground bundle
```

### Combined Switch Box Wire Management:
```
Wire Nut Connections in Combined Box:
┌─────────────────────────────────────────┐
│ Hot Distribution (Red Wire Nut):        │
│ ├─ Hot from vanity switch chain         │
│ ├─ To Main Switch 1 COM                 │
│ ├─ To Vanity Switch 2 COM               │
│ └─ To Fan Switch LINE                   │
│                                         │
│ Neutral Bundle (Yellow Wire Nut):       │
│ ├─ Neutral from vanity switch chain     │
│ ├─ Neutral to main light                │
│ └─ Neutral to fan                       │
│                                         │
│ Ground Bundle (Green Wire Nut):         │
│ ├─ Ground from vanity switch chain      │
│ ├─ Ground to main light                 │
│ ├─ Ground to fan                        │
│ ├─ Main Switch 1 ground wire            │
│ ├─ Vanity Switch 2 ground wire          │
│ ├─ Fan Switch ground wire               │
│ └─ Metal box grounding                  │
└─────────────────────────────────────────┘
```
