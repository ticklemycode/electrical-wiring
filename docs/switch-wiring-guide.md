# 3-Way Switch Wiring Guide

## Critical Understanding: Traveler Wires and Cable Runs

**IMPORTANT**: Before diving into specific switch connections, understand that "traveler wires" are not separate wires running between switches. They are specific conductors within the 14-3 cables that connect the components.

### Physical Cable Installation
- **Vanity 3-Way Circuit**: Box 2 (VS1) connects to Box 7 (VS2) via 14-3 cable
  - Box 7 powers vanity light directly via 14-2 cable
- **Main 3-Way Circuit**: Box 4 (MS2) connects to Box 7 (MS1) via 14-3 cable
  - Box 4 powers main light directly via 14-2 cable

### Traveler Wire Function
**Vanity Circuit (Box 2 → Box 7):**
- **Red wire**: Traveler 1 (VS1 T1 ↔ VS2 T1)
- **White wire**: Traveler 2 (VS1 T2 ↔ VS2 T2) **MARK BLACK TAPE**
- **Black wire**: Always hot from VS1 COM to power Box 7 circuits

**Main Circuit (Box 4 → Box 7):**
- **Red wire**: Traveler 1 (MS2 T1 ↔ MS1 T1)  
- **Black wire**: Traveler 2 (MS2 T2 ↔ MS1 T2)
- **White wire**: Neutral feed from Box 4 to Box 7

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

## ⚠️ Wire Identification Requirements (NEC 200.7)

**CRITICAL SAFETY**: White wires used as hot conductors in switch loops MUST be re-identified with black electrical tape at both ends.

**In this circuit, the following white wires carry HOT (not neutral):**
1. **White wire from Box 2 to Box 7** - Vanity Traveler 2 (VS1 T2 to VS2 T2)

**Re-identification locations:**
- At Box 2 (mark white wire going to Box 7 T2 terminal)
- At Box 7 (mark white wire from Box 2 going to VS2 T2 terminal)

**Why this matters**: Failure to identify switch loop conductors can result in dangerous confusion between true neutrals and hot wires.

## Main Light 3-Way Wiring Configuration

**IMPORTANT**: The main light 3-way circuit uses Main Switch 1 (in Combined Box at end of run) and Main Switch 2 (separate box). Traveler wires run between these switches via 14-3 cable.

### Switch Box 1 (Main Switch 1 - in Combined Box):
**This switch is at the END of the circuit run and receives continuous hot**
```
Incoming Power (14-2):           Main Switch 1 Connections:      To Main Switch 2 (14-3 Travelers):
- Hot (Black)     →  COM         - Red Traveler    →  T1        - Red to MS2 T1
- Neutral (White) →  Pass-through - Black Traveler  →  T2        - Black to MS2 T2  
- Ground (Bare)   →  Switch GND   - Ground          →  GND       - Ground to MS2 GND
```

### Switch Box 2 (Main Switch 2):
**IMPORTANT**: Main Switch 2 now connects to the Combined Box via **TWO separate 14-3 cables** for clean circuit separation:
- **Cable A**: Vanity circuit pass-through (white=hot, red=traveler, black=neutral)
- **Cable B**: Main light travelers (red=traveler1, black=traveler2, white=neutral)

```
From Vanity Light (14-3):           To Combined Box - Cable A (14-3):        
- WHITE (Hot from VS circuit) → White (marked as hot with tape)    
- Red (Traveler to VS2)       → Red (traveler pass-through)        
- Black (Hot continues)       → Black (neutral pass-through)       

From/To Combined Box - Cable B (14-3):  Main Switch 2 Connections:        
- Red to Combined Box         →  T1   (Red Traveler)              
- Black to Combined Box       →  T2   (Black Traveler)            
- White (neutral)             →  Pass-through                     
- Ground from Combined Box    →  GND  (Ground)

IMPORTANT: Main Switch 2 does NOT directly control main light
- Main light is controlled by Combined Box (Main Switch 1)
- Main Switch 2 provides 3-way travelers to Combined Box via Cable B
- Combined Box uses these travelers to provide 3-way control

TRUE NEUTRALS in this box:
- White from incoming 14-2 power (always neutral)
- White in Cable B to Combined Box (always neutral)
- Black from vanity light in Cable A (neutral pass-through)

WHITE WIRE CARRYING HOT (mark with black tape):
- White from vanity light circuit (switched hot - NOT neutral)
- White in Cable A to Combined Box (continuation of above hot)
```

**Wire Identification Required**: The white wire from the vanity light circuit carries HOT and must be marked with black electrical tape at both ends per NEC 200.7(C).

### Main Light Fixture Box:
**Receives switched hot from Main Switch 2 COM terminal**
```
From Main Switch 2 (14-2):       Main Light Connections:        To Fan (14-2 Pass-Through):
- Switched Hot (Black) → Light Hot + Pass-through to fan     - Hot Continue (Black)
- Neutral (White)      → Light Neutral + Pass-through       - Neutral Continue (White)  
- Ground (Bare)        → Light Ground + Pass-through        - Ground Continue (Bare)
```

**Important Notes:**
- Main light only receives power when Main Switch 1 and Main Switch 2 are in correct 3-way positions
- Hot wire continues through light fixture to feed fan downstream
- All three conductors (hot, neutral, ground) pass through to continue the circuit

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

**IMPORTANT**: Combined Box now receives **TWO separate 14-3 cables from Main Switch 2** for clean circuit separation:
- **Cable A**: Vanity circuit (white=hot marked with tape, red=traveler, black=neutral)  
- **Cable B**: Main light travelers (red=traveler1, black=traveler2, white=neutral)

#### Main Switch 1 (3-Way for Main Light):
```
From Main Switch 2 - Cable B (14-3):    Main Switch 1 Connections:      To Main Light (14-2):
- Red Traveler 1      →  T1             - Hot (spliced)    →  COM        - Switched Hot (Black)
- Black Traveler 2    →  T2             - Red Traveler     →  T1         - Neutral (White)      
- White (neutral)     →  Pass-through   - Black Traveler   →  T2         - Ground (Bare)
- Ground             →  Switch ground   - Ground           →  GND
```

#### Vanity Switch 2 (3-Way for Vanity Light):
```
From Main Switch 2 - Cable A (14-3):    Vanity Switch 2 Connections:
- White (hot marked) →  COM             - Hot from VS1     →  COM (marked white)
- Red Traveler       →  T1              - Red Traveler     →  T1         
- Black (neutral)    →  Pass-through    - Neutral Return   →  T2 (black wire)
- Ground            →  Switch ground    - Ground           →  GND
```

#### Fan Switch (Single Pole):
```
Wire Connections in Combined Box:
- Hot (spliced from main feed) →  LINE     - Switched Hot       →  LOAD (to fan)
- Ground (from ground bundle)  →  Switch ground
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

### Exhaust Fan Fixture Connections:
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

### Main Switch 2 Box - Complete Wire Summary:

**All wires present in this box:**

1. **14-3 Cable from Vanity Light:**
   - ⚪ White → HOT from vanity circuit (mark with black tape) → continues to Combined Box
   - 🔴 Red → Traveler from VS1 → continues to Combined Box for VS2
   - ⚫ Black → Hot continuation → continues to Combined Box
   - 🟢 Green → Ground → continues to Combined Box

2. **14-3 Cable from Combined Box (Main Switch 1 travelers):**
   - 🔴 Red → MS2 T1 terminal (traveler from Main Switch 1)
   - ⚫ Black → MS2 T2 terminal (traveler from Main Switch 1)
   - ⚪ White → TRUE neutral (pass-through only)
   - 🟢 Green → MS2 GND terminal

3. **14-2 Cable to Main Light:**
   - ⚫ Black → MS2 COM terminal output (switched hot to main light)
   - ⚪ White → TRUE neutral (pass-through to main light)
   - 🟢 Bare → Ground connection (pass-through to main light)

**Key Points:**
- Main Switch 2 controls the main light via 3-way switching with Main Switch 1
- Vanity circuit wires pass through this box but don't connect to Main Switch 2
- The white wire from vanity circuit is HOT and must be marked
- True neutrals never connect to any switch terminals
