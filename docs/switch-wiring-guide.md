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
   │     GND     │ ← Ground terminal (green screw)
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

### Vanity Switch 1:
```
From Main Circuit (14-3):     To Vanity Switch 2 (14-3):  To Vanity Light:
- Hot (Black)     →  COM      - Traveler 1 (Red)   →  T1  - Switched Hot
- Neutral (White) →  Pigtail  - Traveler 2 (Black) →  T2  - Neutral
- Ground (Bare)   →  Switch   - Ground (Bare)      →  GND - Ground
```

### Vanity Switch 2:
```
From Vanity Switch 1 (14-3):  To Vanity Light Fixture:
- Traveler 1 (Red)   →  T1    - Switched Hot (Black) →  COM
- Traveler 2 (Black) →  T2    - Neutral (White)      →  Light
- Ground (Bare)      →  GND   - Ground (Bare)        →  Light & Switch
```

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
Junction Box Connections:
┌──────────────────────────────────────────┐
│ From GFCI (14-2) │ To Switch 1 (14-3)   │
│                  │                       │
│ Hot (Black) ─────┼→ Hot to switch (Black) │
│       │          │                       │
│       └─────────→ Fixture Hot (Black)    │
│                  │                       │
│ Neutral (White) ─┼→ Neutral (White)      │
│       │          │                       │
│       └─────────→ Fixture Neutral (White)│
│                  │                       │
│ Ground (Bare) ───┼→ Ground (Bare)        │
│       │          │                       │
│       └─────────→ Fixture Ground (Green) │
└──────────────────────────────────────────┘

Note: Vanity light gets constant power; switching occurs at switch locations
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
   - Black: Continuous hot from GFCI
   - White: Neutral return to panel
   - Bare: Ground for safety

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

## Complete Circuit Wire Tracing Guide

### End-to-End Wire Color Tracking:

#### Hot Wire Path (Black):
```
Electrical Panel → GFCI LINE (Black)
                ↓
GFCI LOAD (Black) → Vanity Light Hot (Black)
                  ↓
Vanity Light Pass-Through → Vanity Switch 1 COM (Black)
                         ↓
Vanity Switch 1 Travelers → Vanity Switch 2 Travelers
                         ↓
Vanity Switch 2 COM → Vanity Light Control (switched)

Main Circuit Continuation:
Vanity Switch Box → Main Switch 1 COM (Black)
                 ↓
Main Switch 1 Travelers → Main Switch 2 Travelers  
                       ↓
Main Switch 2 COM → Main Light Hot (switched Black)
                 ↓
Main Light Pass-Through → Fan Hot Pass-Through (Black)
                       ↓
Fan Pass-Through → Fan Switch HOT IN (Black)
                ↓
Fan Switch HOT OUT → Fan Control Wire (Black to fan)
```

#### Neutral Wire Path (White):
```
Electrical Panel → GFCI LINE (White)
                ↓
GFCI LOAD (White) → Vanity Light Neutral (White)
                  ↓
Vanity Light Pass-Through → All Switch Boxes (White)
                         ↓
Switch Box Splices → Main Light Neutral (White)
                  ↓
Main Light Pass-Through → Fan Neutral (White)
                       ↓
Fan Connection → Neutral Return to Panel
```

#### Ground Wire Path (Bare/Green):
```
Electrical Panel → GFCI Ground (Bare)
                ↓
GFCI Ground → Vanity Light Ground (Bare to fixture Green)
           ↓
All Junction Boxes → Switch Grounds + Box Grounds
                  ↓
Main Light Ground → Fan Ground → Panel Ground
```

### Traveler Wire Paths:

#### Main Light Travelers:
```
Main Switch 1 → Main Switch 2:
- T1 (Red wire): Switch 1 T1 ↔ Switch 2 T1
- T2 (Black wire): Switch 1 T2 ↔ Switch 2 T2
```

#### Vanity Light Travelers:
```
Vanity Switch 1 → Vanity Switch 2:
- T1 (Red wire): Switch 1 T1 ↔ Switch 2 T1  
- T2 (Black wire): Switch 1 T2 ↔ Switch 2 T2
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
- Use green grounding screws on switches
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

## Safety Reminders

⚠️ **ELECTRICAL SAFETY**:
- Turn off power at breaker before working
- Use a voltage tester to verify power is off
- Follow local electrical codes
- Consider hiring a licensed electrician
- Test GFCI outlets monthly

## Code Compliance Notes

- **NEC Article 210.52(D)**: GFCI protection required for bathroom outlets
- **NEC Article 404.2(C)**: Switch accessibility requirements
- **NEC Article 250**: Grounding and bonding requirements
- Local codes may have additional requirements
