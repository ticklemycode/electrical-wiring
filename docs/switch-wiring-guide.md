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

**IMPORTANT**: The vanity light operates like a normal 3-way switched light - you can turn it ON/OFF from either switch location. The difference is that power is available at the fixture location (rather than at the first switch), but the light still switches normally.

### Vanity Light Fixture Connections:
```
From GFCI (14-2 Cable):       Vanity Light Fixture:
- Hot (Black)     →           - Fixture Hot (Black) - Power available
- Neutral (White) →           - Fixture Neutral (White) - Direct to panel
- Ground (Bare)   →           - Fixture Ground (Green)

Note: NO RED WIRE connects to the vanity light fixture
Hot wire is also tapped to feed the 3-way switch system for control
```

### How Vanity Light Switching Works:
The vanity light uses **standard 3-way switch control** where:
1. **Hot wire**: Available at fixture from GFCI, also feeds first switch
2. **Switched hot**: Controlled by the 3-way switch system through travelers
3. **Light turns ON**: When switches complete the hot path through travelers
4. **Light turns OFF**: When switches break the hot path

**Important**: This is normal 3-way switching - the switches control the hot wire, not the neutral.

### Vanity Switch 1:
```
From Vanity Light Box (14-3):     To Vanity Switch 2 (14-3):  
- Hot (Black)     →  COM          - Traveler 1 (Red)   →  T1  
- Red (Traveler)  →  T1           - Traveler 2 (Black) →  T2  
- Black (Traveler)→  T2           - Neutral (White)    →  Pass-through (wire nut)
- White (Neutral) →  Pass-through (wire nut)
- Ground (Bare)   →  Switch ground
```

### Vanity Switch 2:
```
From Vanity Switch 1 (14-3):      To Main Circuit (14-2):
- Traveler 1 (Red)   →  T1        - Hot (Black)        →  COM output (to main circuit)
- Traveler 2 (Black) →  T2        - Neutral (White)    →  Continue circuit (wire nut)
- White (Neutral)    →  Pass-through (wire nut)
- Ground (Bare)      →  Switch ground
```

**Key Point**: The vanity light turns ON/OFF normally from either switch. The 3-way switches control the **hot path** to complete the circuit.

## How Vanity Light 3-Way Switching Works

**Critical Understanding**: The vanity light operates like a normal 3-way switched light - it can be turned ON and OFF from either switch location.

### Power Flow Explanation:
```
1. GFCI provides HOT → Vanity Light Fixture (hot side always available)
                    ↓
2. Same hot wire → 3-Way Switch System (for switching control)
                    ↓
3. When switches align → Complete hot path → Light ON
   When switches differ → Broken hot path → Light OFF
                    ↓
4. Continuing circuit → Provides switched hot to main lights
```

### What Each Wire Does:
- **Black from GFCI**: Provides hot to vanity fixture + feeds switch system  
- **White (neutral)**: Direct path from fixture to panel (not switched)
- **Red in 14-3 cable**: Traveler wire between switches ONLY
- **Black in 14-3 cable**: Second traveler wire between switches ONLY
- **Ground**: Safety ground for all devices

### The Switching Logic:
- **Both switches same position**: Vanity light OFF (hot path broken)
- **Switches different positions**: Vanity light ON (hot path complete)
- **Either switch can control**: Normal 3-way operation

**Key Point**: The vanity light operates completely normally - you can turn it on and off from either switch location just like any other 3-way switched light.

## Wire Color Code Standards

### 14-2 Cable:
- **Black**: Hot (Line/Load)
- **White**: Neutral
- **Bare/Green**: Ground

### 14-3 Cable:
- **Black**: Hot or Traveler
- **Red**: Traveler
- **White**: Neutral (sometimes used as traveler when properly marked)
- **Bare/Green**: Ground

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
Junction Box Connections (Switch Loop Method):
┌──────────────────────────────────────────┐
│ From GFCI (14-2) │ To Switch 1 (14-3)   │
│                  │                       │
│ Hot (Black) ─────┼→ Hot to switch (Black) │
│       │          │   (for control)       │
│       └─────────→ Fixture Hot (Black)    │
│                  │   (power available)   │
│                  │                       │
│ Neutral (White) ─┼→ Switch pass-through    │
│       │          │   (wire nut - not to   │
│       │          │    switch terminals)   │
│       └─────────→ Fixture Neutral (White)│
│                  │   (direct to panel)    │
│                  │                       │
│ Ground (Bare) ───┼→ Ground (Bare)        │
│       │          │                       │
│       └─────────→ Fixture Ground (Green) │
│                  │                       │
│                  │ Red Wire: ONLY between │
│                  │ switches - NOT to      │
│                  │ fixture!              │
└──────────────────────────────────────────┘

Note: Vanity light operates normally (ON/OFF control from both switches).
      The hot path is switched by the 3-way system.
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

#### Connection 3: Vanity Switch 1 to Vanity Switch 2
```
Cable: 14-3 between Vanity Switch boxes

Vanity Switch 1         →    Vanity Switch 2
├─ Red (T1 terminal)    →    Red to T1 terminal
├─ Black (T2 terminal)  →    Black to T2 terminal
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 4: Vanity Switch 2 to Main Switch 1
```
Cable: 14-2 from Vanity Switch 2 box to Main Switch 1 box

Vanity Switch 2 Box     →    Main Switch 1 Box
├─ Black (Hot Feed)     →    Black to COM terminal
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 5: Main Switch 1 to Main Switch 2
```
Cable: 14-3 between Main Switch boxes

Main Switch 1           →    Main Switch 2
├─ Red (T1 terminal)    →    Red to T1 terminal
├─ Black (T2 terminal)  →    Black to T2 terminal
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 6: Main Switch 2 to Main Light Fixture
```
Cable: 14-2 from Main Switch 2 box to Main Light box

Main Switch 2 Box       →    Main Light Junction Box
├─ Black (COM terminal) →    Black to main fixture + splice to fan
├─ White (Neutral)      →    White to main fixture + splice to fan
└─ Bare (Ground)        →    Green to main fixture + splice to fan
```

#### Connection 7: Main Light Fixture to Fan Switch
```
Cable: 14-2 from Main Light box to Fan Switch box

Main Light Box          →    Fan Switch Box
├─ Black (Pass-through) →    Black to LINE terminal (hot feed)
├─ White (Neutral)      →    White splice (not to switch)
└─ Bare (Ground)        →    Switch ground wire + box ground
```

#### Connection 8: Fan Switch to Exhaust Fan
```
Cable: 14-2 from Fan Switch box to Fan box

Fan Switch Box          →    Exhaust Fan Junction Box
├─ Black (LOAD terminal)→    Black to fan motor
├─ White (Neutral)      →    White to fan motor
└─ Bare (Ground)        →    Green to fan motor + fan housing
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

## Quick Reference Guide

### Wire Color Code Summary
| Wire Color | Function | Connects To |
|------------|----------|------------|
| **Black** | Hot (always) | GFCI LOAD → Vanity Light Fixture → Switch feed |
| **Black** | Hot (switched) | Switch COM → Main Light Fixture |
| **Black** | Travelers | Between 3-way switches (T2 terminals) - NOT to fixtures |
| **Red** | Travelers | Between 3-way switches (T1 terminals) - NOT to fixtures |
| **White** | Neutral | All fixtures, pass through switches |
| **Bare/Green** | Ground | All devices, boxes, fixtures |

### Switch Terminal Quick ID
| Switch Type | Terminal | Wire Connection |
|-------------|----------|----------------|
| **3-Way** | COM | Hot IN (power side) or Hot OUT (load side) |
| **3-Way** | T1 | Red traveler wire |
| **3-Way** | T2 | Black traveler wire |
| **Single Pole** | LINE | Hot IN (from source) |
| **Single Pole** | LOAD | Hot OUT (to fixture) |

### Troubleshooting Checklist
- [ ] Power OFF at breaker
- [ ] Test with voltage tester
- [ ] Check GFCI reset button
- [ ] Verify COM terminal connections
- [ ] Check traveler wire pairs (T1-T1, T2-T2)
- [ ] Confirm neutral splices
- [ ] Test ground continuity
- [ ] Verify fixture connections

### Load Calculations (15A Circuit)
- **GFCI Outlet**: 1.5A (max)
- **Vanity Light**: 1-2A (LED/CFL)
- **Main Light**: 1-2A (LED/CFL)  
- **Exhaust Fan**: 0.5-1.5A
- **Total Load**: ~4-7A (well under 15A limit)

---

*Remember: When in doubt, consult a licensed electrician. Electrical work must meet local codes and inspection requirements.*

## Switch Grounding Methods

Since your switches don't have ground screws, here are the proper grounding methods:

### Method 1: Pigtail Connection (Most Common)
```
Switch Grounding with Pigtail:
┌─────────────────────────────────────┐
│ Junction Box                        │
│                                     │
│ Circuit Ground ──┐                  │
│ (bare wire)      │                  │
│                  ├── Wire Nut       │
│ Box Ground ──────┤   Connection     │
│ (to metal box)   │                  │
│                  │                  │
│ Switch Pigtail ──┘                  │
│ (green wire)                        │
│        │                            │
│        └── To Switch Ground Wire    │
└─────────────────────────────────────┘
```

### Method 2: Push-In Ground Connection
```
Switch with Push-In Ground:
┌─────────────────────────────┐
│        Back of Switch       │
│                             │
│  ○ ○ ○    [GROUND HOLE]     │ ← Push bare wire in here
│  │ │ │                     │
│  COM T1 T2                 │
└─────────────────────────────┘

Note: Strip 3/4" of ground wire and push firmly into hole
```

### Method 3: Self-Grounding Switch (If Applicable)
```
Self-Grounding Switch Installation:
1. Metal box must be properly grounded
2. Switch grounds through mounting screws
3. Circuit ground connects to box only
4. Verify continuity between switch and box ground
```

### Ground Wire Connection Steps:
1. **Strip all ground wires**: 3/4" of insulation
2. **Twist grounds together**: Circuit ground + box ground + switch pigtail
3. **Apply wire nut**: Secure all ground connections
4. **Connect switch ground**: Via pigtail, push-in, or self-grounding
5. **Test continuity**: Verify ground path from panel to switch
