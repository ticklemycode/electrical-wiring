# Complete Bathroom Wiring Layout

## Physical Layout Diagram

```
BATHROOM ELECTRICAL LAYOUT
═══════════════════════════════════════════════════════════════

                    Electrical Panel (20A Breaker)
                              │
                              │ 12-2 w/Ground
                              ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 1                               │
    │  ┌─────────────┐                                       │
    │  │ GFCI OUTLET │ ← Power Entry Point                   │
    │  │   (20A)     │                                       │
    │  └─────────────┘                                       │
    │         │                                               │
    │         │ 12-2 w/Ground                                │
    │         ↓                                               │
    │  ┌─────────────┐                                       │
    │  │ VANITY LIGHT│                                       │
    │  │  FIXTURE    │                                       │
    │  └─────────────┘                                       │
    └─────────────────────────────────────────────────────────┘
              │
              │ 12-3 w/Ground (for 3-way switching)
              ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 2                               │
    │  ┌─────────────┐    ┌─────────────┐                    │
    │  │ VANITY SW1  │    │ MAIN SW1    │                    │
    │  │  (3-way)    │    │  (3-way)    │                    │
    │  └─────────────┘    └─────────────┘                    │
    └─────────────────────────────────────────────────────────┘
                                   │
                                   │ 12-3 w/Ground
                                   ↓
    ┌─────────────────────────────────────────────────────────┐
    │                   CEILING                               │
    │                ┌─────────────┐                          │
    │                │ MAIN LIGHT  │                          │
    │                │  FIXTURE    │                          │
    │                └─────────────┘                          │
    │                        │                                │
    │                        │ 12-2 w/Ground                 │
    │                        ↓                                │
    │                ┌─────────────┐                          │
    │                │ EXHAUST FAN │                          │
    │                └─────────────┘                          │
    └─────────────────────────────────────────────────────────┘
                             │
                             │ 12-3 w/Ground
                             ↓
    ┌─────────────────────────────────────────────────────────┐
    │                    WALL 3                               │
    │  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐ │
    │  │ MAIN SW2    │    │ VANITY SW2  │    │  FAN SWITCH │ │
    │  │  (3-way)    │    │  (3-way)    │    │ (Single)    │ │
    │  └─────────────┘    └─────────────┘    └─────────────┘ │
    └─────────────────────────────────────────────────────────┘
```

## Detailed Wire Run Diagram

```
WIRE ROUTING AND CONNECTIONS
═══════════════════════════════════════════════════════════════

┌─ ELECTRICAL PANEL ─┐
│   20A Breaker      │
│   Hot │ Neutral │  │
└───────┼─────────┼──┘
        │         │
        │ 12-2 w/Ground Cable
        │         │
        ↓         ↓
┌───────────────────────┐
│    GFCI OUTLET        │ ← Junction point for all circuits
│  Hot │ Neutral │ Gnd  │
└──────┼─────────┼──────┘
       │         │
       │ 12-2 w/Ground
       │         │
       ↓         ↓
┌───────────────────────┐
│   VANITY LIGHT        │
│  Hot │ Neutral │ Gnd  │ ← Always on hot supply
└──────┼─────────┼──────┘
       │         │
       │ 12-3 w/Ground (Hot + 2 Travelers)
       │         │
       ↓         ↓
┌───────────────────────┐
│   VANITY SWITCH 1     │
│ COM │  T1  │  T2  │Gnd│ ← First 3-way for vanity
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 12-3 w/Ground
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│   MAIN SWITCH 1       │
│ COM │  T1  │  T2  │Gnd│ ← First 3-way for main light
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 12-3 w/Ground
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│    MAIN LIGHT         │
│ Sw.Hot│ Neutral │ Gnd │ ← Controlled by 3-way switches
└───────┼─────────┼─────┘
        │         │
        │ 12-2 w/Ground
        │         │
        ↓         ↓
┌───────────────────────┐
│   EXHAUST FAN         │
│  Hot │ Neutral │ Gnd  │ ← Pass-through power to switches
└──────┼─────────┼──────┘
       │         │
       │ 12-3 w/Ground
       │         │
       ↓         ↓
┌───────────────────────┐
│   MAIN SWITCH 2       │
│ COM │  T1  │  T2  │Gnd│ ← Second 3-way for main light
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 12-3 w/Ground (Travelers back to vanity)
      │      │   │   │
      ↓      ↓   ↓   ↓
┌───────────────────────┐
│   VANITY SWITCH 2     │
│ COM │  T1  │  T2  │Gnd│ ← Second 3-way for vanity
└─────┼──────┼───┼───┼──┘
      │      │   │   │
      │ 12-2 w/Ground
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
- **Circuit Rating**: 20 Amperes
- **Wire Gauge**: 12 AWG (American Wire Gauge)
- **Cable Type**: NM-B (Non-metallic sheathed cable, Building wire)
- **Voltage**: 120V AC
- **Frequency**: 60 Hz

### Wire Current Capacity:
- **12 AWG**: 20A maximum (perfect for 20A circuit)
- **Safety Factor**: Wire rated for exactly the breaker size
- **Temperature Rating**: 90°C (194°F) cable rating

### Protection Devices:
- **Main Breaker**: 20A single pole
- **GFCI**: 20A, 120V (required for bathroom)
- **Arc Fault**: May be required by local code

## Installation Sequence

### Step-by-Step Wire Installation:
1. **Install GFCI outlet** (power entry point)
2. **Run 12-2 to vanity light** fixture location
3. **Run 12-3 from vanity light** to first switch box
4. **Run 12-3 between all switch boxes** (maintains 3-way capability)
5. **Run 12-3 from switch box** to main light fixture
6. **Run 12-2 from main light** to fan location
7. **Connect control wire** from fan switch back to fan

### Critical Connection Points:
- **Hot splices**: Use appropriate wire nuts
- **Neutral splices**: Maintain continuous neutral path
- **Ground connections**: Bond all metal components
- **Traveler connections**: Maintain T1-to-T1, T2-to-T2 continuity
