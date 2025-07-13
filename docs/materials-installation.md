# Materials List and Installation Guide

## Required Materials

### Electrical Wire
| Item | Quantity | Specification | Usage |
|----#### Step 3: GFCI Outlet Wiring
```
GFCI Outlet Connections:
┌─────────────────┐
│      GFCI       │
│  LINE    LOAD   │
│ H  N  G  H  N  G│
└─┬──┬──┬──┬──┬──┬┘
  │  │  │  │  │  │
  │  │  │  │  │  └─ Ground to downstream devices
  │  │  │  │  └──── Neutral to downstream devices  
  │  │  │  └─────── Hot to downstream devices
  │  │  └────────── Ground from panel
  │  └───────────── Neutral from panel
  └──────────────── Hot from panel

CRITICAL: LINE side connects to panel, LOAD side to downstream devices
```

### Detailed GFCI Outlet Wiring Guide

#### GFCI Terminal Identification:
```
GFCI Outlet Back View:
┌─────────────────────────┐
│  ○ LINE ○    ○ LOAD ○  │ ← Hot terminals (brass)
│                         │
│  ○ LINE ○    ○ LOAD ○  │ ← Neutral terminals (silver)  
│                         │
│      ○ GROUND ○        │ ← Ground terminals (green)
│                         │
│   [TEST]    [RESET]    │ ← Test/Reset buttons
└─────────────────────────┘
```

#### Step-by-Step GFCI Wiring:
1. **Turn OFF power** at breaker and verify with tester
2. **Strip wires**: 3/4" of insulation on all wires
3. **Connect LINE side** (from electrical panel):
   - Black (hot) wire → LINE HOT terminal
   - White (neutral) wire → LINE NEUTRAL terminal
   - Bare/Green (ground) wire → GROUND terminal
4. **Connect LOAD side** (to downstream devices):
   - Black (hot) wire → LOAD HOT terminal  
   - White (neutral) wire → LOAD NEUTRAL terminal
   - Bare/Green (ground) wire → GROUND terminal
5. **Fold wires** carefully into box
6. **Mount GFCI** flush with wall surface
7. **Test operation** with TEST/RESET buttons

#### GFCI Safety Notes:
- **Never reverse LINE/LOAD** - this disables GFCI protection
- **Test monthly** using TEST/RESET buttons
- **GFCI protects** all downstream devices when wired correctly
- **Replace immediately** if GFCI won't reset or trips frequently-----------|-------|
| 14-2 NM-B Cable | 50 feet | 14 AWG, 2 conductor + ground | Power feeds, simple connections |
| 14-3 NM-B Cable | 75 feet | 14 AWG, 3 conductor + ground | 3-way switch travelers |
| Wire Nuts | 1 box each | Yellow (small), Red (medium) | Wire connections |
| Electrical Tape | 2 rolls | 3/4" x 60' | Securing connections |

#### Wire Composition Clarification

**14-2 NM-B Cable contains:**
- ⚫ **One black wire** (hot)
- ⚪ **One white wire** (neutral)  
- 🟢 **One bare/green wire** (ground)

**14-3 NM-B Cable contains:**
- ⚫ **One black wire** (hot or traveler)
- 🔴 **One red wire** (traveler)
- ⚪ **One white wire** (neutral)
- 🟢 **One bare/green wire** (ground)

**Important**: 14-3 cable has exactly **one wire of each color** - not multiple wires of the same color.

### Electrical Devices
| Item | Quantity | Specification | Notes |
|------|----------|---------------|-------|
| GFCI Outlet | 1 | 15A, 120V, Self-Test | Must be first device in circuit |
| 3-Way Switches | 4 | 15A, 120V | 2 for main light, 2 for vanity |
| Single Pole Switch | 1 | 15A, 120V | For exhaust fan |
| Switch Plates | 3 | 1-gang, 2-gang, 3-gang | Based on switch groupings |
| Outlet Cover | 1 | Standard GFCI cover | Weather-resistant if needed |

### Electrical Boxes
| Item | Quantity | Specification | Usage |
|------|----------|---------------|-------|
| Single Gang Switch Box | 2 | 18 cubic inch capacity | Vanity Switch 1, Main Switch 2 |
| Triple Gang Switch Box | 1 | 22+ cubic inch capacity | Combined box (3 switches) |
| Outlet Box | 1 | Standard single gang | GFCI outlet |
| Ceiling Boxes | 2 | Rated for fixture weight | Light fixtures and fan |
| Box Connectors | 10 | 1/2" NM cable connectors | Secure cable to boxes |

### Fixtures and Components
| Item | Quantity | Specification | Notes |
|------|----------|---------------|-------|
| Main Light Fixture | 1 | Bathroom rated, LED compatible | Choose appropriate style |
| Vanity Light | 1 | Bathroom rated, LED compatible | Consider length of vanity |
| Exhaust Fan | 1 | CFM rated for bathroom size | Humidity sensor optional |
| Light Bulbs | As needed | LED recommended | Check fixture compatibility |

## Tools Required

### Basic Electrical Tools
- Non-contact voltage tester
- Digital multimeter
- Wire strippers (14-16 AWG)
- Needle-nose pliers
- Flat and Phillips screwdrivers
- Wire nuts and crimp tool

### Installation Tools
- Drill with bits (wood/masonry)
- Stud finder
- Fish tape or wire pulling system
- Utility knife
- Level
- Measuring tape

### Safety Equipment
- Safety glasses
- Work gloves
- Flashlight or headlamp
- Voltage tester

## Pre-Installation Planning

### Circuit Load Calculation
```
Device Load Analysis:
┌─────────────────┬──────────┬─────────┬──────────┐
│ Device          │ Quantity │ Wattage │ Total W  │
├─────────────────┼──────────┼─────────┼──────────┤
│ GFCI Outlet     │    1     │   N/A   │    0     │
│ Main Light      │    1     │   60W   │   60W    │
│ Vanity Light    │    1     │   80W   │   80W    │
│ Exhaust Fan     │    1     │   90W   │   90W    │
│ Future Devices  │    -     │    -    │  200W    │
├─────────────────┼──────────┼─────────┼──────────┤
│ TOTAL LOAD      │          │         │  430W    │
└─────────────────┴──────────┴─────────┴──────────┘

Circuit Capacity: 15A × 120V = 1800W
Load Percentage: 430W ÷ 1800W = 24% (Well within safe limits)
```

### Code Compliance Checklist
- [ ] GFCI protection for bathroom outlets (NEC 210.8)
- [ ] Proper wire gauge for circuit amperage (NEC 310.15)
- [ ] Adequate box fill calculations (NEC 314.16)
- [ ] Proper grounding of all components (NEC 250)
- [ ] Switch accessibility requirements (NEC 404.2)
- [ ] Fixture mounting requirements (NEC 314.27)

## Installation Steps

### Phase 1: Rough-In Wiring

#### Step 1: Install Electrical Boxes
```
1. Mark box locations:
   - GFCI outlet: 42" from floor
   - Switches: 48" from floor (center of box)
   - Ceiling fixtures: As per design

2. Cut openings:
   - Use appropriate hole saw or utility knife
   - Check for studs and obstacles
   - Ensure boxes fit snugly

3. Mount boxes:
   - Secure to studs when possible
   - Use box supports for drywall mounting
   - Verify boxes are flush with finished wall
```

#### Step 2: Run Cable Routing
```
Cable Run Sequence:
1. Panel → GFCI Outlet (14-2)
2. GFCI → Vanity Switch 1 (14-2)
3. Vanity Switch 1 → Vanity Light (14-3, switching junction)
4. Vanity Light → Combined Switch Box (14-3, switching completion)
5. Combined Switch Box → Main Switch 2 (14-3)
6. Main Switch 2 → Main Light (14-2)
7. Main Light → Fan (14-2, hot pass-through)
8. Fan → Combined Switch Box (14-2, fan control)

Notes:
- Leave 8" of cable at each box
- Secure cable every 4.5 feet
- Use cable staples within 12" of boxes
- Protect cable through framing
- Combined switch box requires larger capacity for 3 switches
```

### Phase 2: Device Installation

#### Step 3: GFCI Outlet Wiring
```
GFCI Outlet Connections:
┌─────────────────┐
│      GFCI       │
│  LINE    LOAD   │
│ H  N  G  H  N  G│
└─┬──┬──┬──┬──┬──┬┘
  │  │  │  │  │  │
  │  │  │  │  │  └─ Ground to downstream devices
  │  │  │  │  └──── Neutral to downstream devices  
  │  │  │  └─────── Hot to downstream devices
  │  │  └────────── Ground from panel
  │  └───────────── Neutral from panel
  └──────────────── Hot from panel

CRITICAL: LINE side connects to panel, LOAD side to downstream devices
```

#### Step 4: 3-Way Switch Wiring

### Detailed 3-Way Switch Wiring Guide

#### 3-Way Switch Terminal Identification:
```
3-Way Switch Back View:
┌─────────────────┐
│      COM        │ ← Common terminal (dark/black screw)
│                 │
│   T1      T2    │ ← Traveler terminals (brass screws)
│                 │
│     GROUND      │ ← Ground terminal (green screw)
└─────────────────┘
```

#### Main Light 3-Way Switch Configuration:

##### Switch Box 1 (First Main Light Switch):
```
Wire Connections in Box:
┌──────────────────────────────────────┐
│ Incoming 14-3 Cable | Outgoing 14-3  │
│ (from prev device)   | (to switch 2)  │
│                      |                │
│ Hot (Black) ────→ COM terminal        │
│ Red wire ───────→ T1 terminal         │
│ Black wire ─────→ T2 terminal         │
│ White (Neutral) → Wire nut splice     │
│ Ground ─────────→ Switch + wire nut   │
└──────────────────────────────────────┘
```

##### Switch Box 2 (Second Main Light Switch):  
```
Wire Connections in Box:
┌──────────────────────────────────────┐
│ Incoming 14-3 Cable | Outgoing 14-3  │
│ (from switch 1)      | (to light)     │
│                      |                │
│ Red wire ───────→ T1 terminal         │
│ Black wire ─────→ T2 terminal         │
│ Hot to light ───→ COM terminal        │
│ White (Neutral) → Wire nut splice     │
│ Ground ─────────→ Switch + wire nut   │
└──────────────────────────────────────┘
```

#### Vanity Light 3-Way Switch Configuration:

##### Vanity Switch 1 (receives power from GFCI):
```
Wire Connections:
- Hot from GFCI ──────→ COM terminal (input)
- Black to light ─────→ Connected to white going to VS2 (at fixture)
- White to light ─────→ T2 terminal (direct hot feed to fixture)
- Red traveler ───────→ T1 terminal (pass-through to VS2 via fixture)
- Neutral ────────────→ Wire nut (pass through to circuit)
- Ground ─────────────→ Switch + wire nut
```

##### Vanity Switch 2 (in combined switch box):
```
Wire Connections:
- White from fixture ─→ COM terminal (carries hot from VS1 black junction)
- Red traveler ───────→ T1 terminal (from VS1 via fixture)
- Black from fixture ─→ T2 terminal (switched hot return from light)
- Neutral ────────────→ Wire nut (pass through to circuit)  
- Ground ─────────────→ Switch + wire nut
```

**Key Point**: The switching junction occurs AT THE VANITY LIGHT FIXTURE. VS1 black connects to white going to VS2, VS1 white feeds the light directly, and the light's black returns to VS2.

#### 3-Way Switch Wiring Rules:
1. **COM terminal**: Always connects to hot source OR switched hot to load
2. **T1 and T2**: Connect traveler wires between switches (T1 to T1, T2 to T2)
3. **Neutral**: Never connects to 3-way switch terminals (wire nut splice only)
4. **Ground**: Always connect to switch ground screw and splice with other grounds

##### Main Light Switches:
```
Switch 1 (Power Source):        Switch 2 (Load Side):
┌─────────────────┐              ┌─────────────────┐
│   3-WAY SW1     │              │   3-WAY SW2     │
│ COM  T1   T2    │              │ COM  T1   T2    │
└──┬───┬────┬─────┘              └──┬───┬────┬─────┘
   │   │    │                       │   │    │
   │   │    └── Black (Traveler) ───┘   │    │
   │   └─────── Red (Traveler) ─────────┘    │
   │                                         │
   └── Hot from source          Switched Hot ┘
                                to light fixture
```

##### Vanity Light Switches:
```
Similar configuration but with separate hot source from main circuit
```

#### Step 5: Single Pole Fan Switch Wiring

### Detailed Single Pole Switch Wiring Guide

#### Single Pole Switch Terminal Identification:
```
Single Pole Switch Back View:
┌─────────────────┐
│    HOT IN       │ ← Input terminal (brass screw)
│                 │
│   HOT OUT       │ ← Output terminal (brass screw)  
│                 │
│    GROUND       │ ← Ground terminal (green screw)
└─────────────────┘
```

#### Fan Switch Wiring Configuration:
```
Fan Switch Box Connections:
┌────────────────────────────────────────┐
│ Incoming 14-2 Cable | Control to Fan   │
│ (continuous power)   | (switched hot)   │
│                      |                  │
│ Hot (Black) ────→ HOT IN terminal       │
│ Switch Hot ─────→ HOT OUT terminal      │
│ Neutral (White) → Wire nut (no switch)  │
│ Ground ─────────→ Switch + wire nut     │
└────────────────────────────────────────┘
```

#### Step-by-Step Fan Switch Wiring:
1. **Identify wires** in switch box:
   - Continuous hot (black) from circuit
   - Neutral (white) - does NOT connect to switch
   - Ground (bare/green)
   - Control wire (black) going back to fan

2. **Make connections**:
   - Continuous hot → HOT IN terminal
   - Control wire to fan → HOT OUT terminal  
   - Neutral → wire nut splice (bypass switch)
   - Ground → switch ground screw + wire nut with other grounds

3. **Fan control operation**:
   - Switch OFF: No power to fan
   - Switch ON: Hot power sent to fan via control wire

#### Important Fan Switch Notes:
- **Hot pass-through**: Continuous power flows through fan location to reach switch
- **Control wire**: Separate wire carries switched power back to fan
- **Neutral handling**: Neutral never connects to single pole switch terminals
- **Switch location**: At end of circuit but controls fan in middle of circuit

**Important**: The fan switch receives continuous hot power from the circuit that passes through the fan location. The switch then sends switched hot back to the fan for control.

### Switch Wiring Comparison Chart

#### Quick Reference Guide:
```
┌─────────────────┬─────────────────┬─────────────────┐
│   GFCI OUTLET   │   3-WAY SWITCH  │ SINGLE POLE SW  │
├─────────────────┼─────────────────┼─────────────────┤
│ LINE: Hot In    │ COM: Hot/Load   │ HOT IN: Source  │
│ LINE: Neutral   │ T1: Traveler 1  │ HOT OUT: Load   │
│ LINE: Ground    │ T2: Traveler 2  │ GROUND: Safety  │
│ LOAD: Hot Out   │ GND: Safety     │                 │
│ LOAD: Neutral   │                 │                 │
│ LOAD: Ground    │                 │                 │
└─────────────────┴─────────────────┴─────────────────┘
```

#### Terminal Connection Rules:
1. **GFCI Outlet**:
   - LINE side: Connects to electrical panel
   - LOAD side: Connects to downstream devices
   - Provides protection for entire downstream circuit

2. **3-Way Switches**:
   - COM terminal: Hot input (first switch) OR switched output (second switch)
   - T1 & T2: Traveler wires between switches
   - Neutral: Never connects to switch (wire nut splice only)

3. **Single Pole Switch**:
   - Hot terminals: Input and output (both brass colored)
   - Neutral: Bypasses switch via wire nut
   - Controls one device from one location

#### Common Wiring Mistakes to Avoid:
- **GFCI**: Reversing LINE/LOAD connections (disables protection)
- **3-Way**: Connecting neutral to switch terminals (causes malfunction)
- **Single Pole**: Using wrong terminals for hot wires (no control)
- **All switches**: Forgetting ground connections (safety hazard)
````
