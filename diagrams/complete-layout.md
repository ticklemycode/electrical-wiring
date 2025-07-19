# Complete Bathroom Wiring Layout

## Physical Layout Diagram

```
BATHROOM ELECTRICAL LAYOUT (OPTIMAL DESIGN)
═══════════════════════════════════════════════════════════════

                    Electrical Panel (15A Breaker)
                              │
                              │ 14-2 w/Ground
                              ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 1                               │
    │  ┌─────────────┐                                       │
    │  │ GFCI OUTLET │ ← Power Entry Point                   │
    │  │   (15A)     │                                       │
    │  └─────────────┘                                       │
    │         │                                               │
    │         │ 14-2 w/Ground                                │
    │         ↓                                               │
    │  ┌─────────────┐       14-3 w/Ground                   │
    │  │ BOX 2       │ ────────────────────────────────────┐ │
    │  │ VANITY SW1  │ ← Distributes to Box 4 and Box 7   │ │
    │  │  (3-way)    │                                     │ │
    │  └─────────────┘                                     │ │
    │         │                                             │ │
    │         │ 14-2 w/Ground (to Box 4)                   │ │
    │         ↓                                             │ │
    │  ┌─────────────┐                                     │ │
    │  │ BOX 4       │                                     │ │
    │  │ MAIN SW2    │ ← Main circuit hub                  │ │
    │  │ (3-way)     │                                     │ │
    │  └─────────────┘                                     │ │
    │         │                                             │ │
    │         │ 14-2 w/Ground                              │ │
    │         ↓                                             │ │
    │  ┌─────────────┐                                     │ │
    │  │ BOX 5       │                                     │ │
    │  │ MAIN LIGHT  │                                     │ │
    │  │  FIXTURE    │                                     │ │
    │  └─────────────┘                                     │ │
    │         │                                             │ │
    │         │ 14-2 w/Ground                              │ │
    │         ↓                                             │ │
    │  ┌─────────────┐       14-2 w/Ground                 │ │
    │  │ BOX 6       │ ────────────────────────────────────┼─│
    │  │ EXHAUST FAN │                                     │ │
    │  └─────────────┘                                     │ │
    └─────────────────────────────────────────────────────┼─┼┘
                                                          │ │
              Multiple cables converge at Box 7           │ │
                              ↓                           │ │
    ┌─────────────────────────────────────────────────────┼─┼┐
    │                   WALL 2                            │ │ │
    │  ┌─────────────┐ ← 14-3 from Box 2                 │ │ │
    │  │ BOX 7       │ ← 14-3 from Box 4                 │ │ │
    │  │ COMBINED    │ ← 14-2 from Box 6                 ├─┘ │
    │  │ • Main SW1  │                                   │   │
    │  │ • Vanity SW2│                                   │   │
    │  │ • Fan SW    │                                   │   │
    │  └─────────────┘                                   │   │
    │         │                                           │   │
    │         │ 14-2 w/Ground (vanity power)             │   │
    │         ↓                                           │   │
    │  ┌─────────────┐                                   │   │
    │  │ BOX 3       │                                   │   │
    │  │ VANITY LIGHT│                                   │   │
    │  │  FIXTURE    │                                   │   │
    │  └─────────────┘                                   │   │
    └─────────────────────────────────────────────────────┼───┘
                                                          │
                                            14-3 from Box 4
```
                             │ 14-3 w/Ground
                             ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 3                               │
    │  ┌─────────────────────────────────────────────────────┐ │
    │  │           COMBINED SWITCH BOX                       │ │
    │  │  ┌───────────┐ ┌───────────┐ ┌───────────┐         │ │
    │  │  │ MAIN SW1  │ │VANITY SW2 │ │FAN SWITCH │         │ │
    │  │  │ (3-way)   │ │ (3-way)   │ │(Single)   │         │ │
    │  │  └───────────┘ └───────────┘ └───────────┘         │ │
    │  └─────────────────────────────────────────────────────┘ │
    └─────────────────────────────────────────────────────────┘
                             │
                             │ TWO 14-3 Cables w/Ground:  
                             │ • Cable A: Vanity circuit
                             │ • Cable B: Main light travelers
                             ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 4                               │
    │  ┌─────────────┐                                       │
    │  │ MAIN SW2    │ ← Receives both vanity pass-through   │
    │  │  (3-way)    │   and main light traveler cables     │
    │  └─────────────┘                                       │
    └─────────────────────────────────────────────────────────┘
```

## Detailed Wire Run Diagram

```
WIRE ROUTING AND CONNECTIONS
═══════════════════════════════════════════════════════════════

┌─ ELECTRICAL PANEL ─┐
│   15A Breaker      │
│   Hot │ Neutral │  │
└───────┼─────────┼──┘
        │         │
        │ 14-2 w/Ground Cable
        │         │
        ↓         ↓
┌───────────────────────┐
│    GFCI OUTLET        │ ← Junction point for all circuits
│  Hot │ Neutral │ Gnd  │
└──────┼─────────┼──────┘
       │         │
       │ 14-2 w/Ground
       │         │
       ↓         ↓
┌───────────────────────┐
│   VANITY LIGHT        │
│  Hot │ Neutral │ Gnd  │ ← Always on hot supply
└──────┼─────────┼──────┘
       │         │
       │ 14-3 w/Ground (Hot + 2 Travelers)
       │         │
       ↓         ↓
┌───────────────────────┐
│   VANITY SWITCH 1     │
│ COM │  T1  │  T2  │Gnd│ ← First 3-way for vanity
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 14-3 w/Ground
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│   MAIN SWITCH 1       │
│ COM │  T1  │  T2  │Gnd│ ← First 3-way for main light
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 14-3 w/Ground
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│    MAIN LIGHT         │
│ Sw.Hot│ Neutral │ Gnd │ ← Controlled by 3-way switches
└───────┼─────────┼─────┘
        │         │
        │ 14-2 w/Ground
        │         │
        ↓         ↓
┌───────────────────────┐
│   EXHAUST FAN         │
│  Hot │ Neutral │ Gnd  │ ← Pass-through power to switches
└──────┼─────────┼──────┘
       │         │
       │ 14-3 w/Ground
       │         │
       ↓         ↓
┌───────────────────────┐
│   MAIN SWITCH 2       │
│ COM │  T1  │  T2  │Gnd│ ← Second 3-way for main light
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ TWO 14-3 Cables w/Ground to Combined Box:
      │ • Cable A: Vanity circuit pass-through  
      │ • Cable B: Main light travelers
      │      │   │   │
      ↓      ↓   ↓   ↓
┌─────────────────────────────────────┐
│        COMBINED SWITCH BOX          │
│ ┌─────────┐┌─────────┐┌───────────┐ │
│ │MAIN SW1 ││VANITY SW2││FAN SWITCH │ │
│ │ COM│T1 ││ COM│T1 ││  COM│LOAD │ │
│ └────┼───┘└────┼───┘└─────┼──────┘ │
└──────┼─────────┼─────────┼─────────┘
       │         │         │
       │ 14-2    │ (N/A)   │ 14-2
       │         │         │
       ↓         ↓         ↓
   Main Light  (Internal) Fan
      │      │   │   │
      │ 14-2 w/Ground
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│    FAN SWITCH         │
│  Hot │ Load │ Gnd     │ ← Single pole switch for fan
└──────┼──────┼─────────┘
       │      │
       │ Control wire back to fan
       └──────┘
```

## Switch Control Logic

### Main Light 3-Way Control:
```
MAIN LIGHT SWITCHING LOGIC
═══════════════════════════

Switch 1 Position  │  Switch 2 Position  │  Light Status
─────────────────────┼─────────────────────┼──────────────
      UP           │         UP          │     OFF
      UP           │        DOWN         │     ON
     DOWN          │         UP          │     ON
     DOWN          │        DOWN         │     OFF

Traveler Wire Paths:
- Position UP: Power flows through T1 (Red wire)
- Position DOWN: Power flows through T2 (Black wire)
```

### Vanity Light 3-Way Control:
```
VANITY LIGHT SWITCHING LOGIC
════════════════════════════

Switch 1 Position  │  Switch 2 Position  │  Light Status
─────────────────────┼─────────────────────┼──────────────
      UP           │         UP          │     OFF
      UP           │        DOWN         │     ON
     DOWN          │         UP          │     ON
     DOWN          │        DOWN         │     OFF

Independent Control: Vanity switches operate separately from main light switches
```

## Wire Gauge and Circuit Protection

### Circuit Specifications:
- **Circuit Rating**: 15 Amperes
- **Wire Gauge**: 14 AWG (American Wire Gauge)
- **Cable Type**: NM-B (Non-metallic sheathed cable, Building wire)
- **Voltage**: 120V AC
- **Frequency**: 60 Hz

### Wire Current Capacity:
- **14 AWG**: 15A maximum (perfect for 15A circuit)
- **Safety Factor**: Wire rated for exactly the breaker size
- **Temperature Rating**: 90°C (194°F) cable rating

### Protection Devices:
- **Main Breaker**: 15A single pole
- **GFCI**: 15A, 120V (required for bathroom)
- **Arc Fault**: May be required by local code

## Installation Sequence

### Step-by-Step Wire Installation:
1. **Install GFCI outlet** (power entry point)
2. **Run 14-2 to vanity light** fixture location
3. **Run 14-3 from vanity light** to first switch box
4. **Run 14-3 between all switch boxes** (maintains 3-way capability)
5. **Run 14-3 from switch box** to main light fixture
6. **Run 14-2 from main light** to fan location
7. **Connect control wire** from fan switch back to fan

### Critical Connection Points:
- **Hot splices**: Use appropriate wire nuts
- **Neutral splices**: Maintain continuous neutral path
- **Ground connections**: Bond all metal components
- **Traveler connections**: Maintain T1-to-T1, T2-to-T2 continuity
