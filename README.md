# Bathroom Electrical Wiring Diagram

## Project Overview
This document provides a complete wiring diagram and installation guide for a bathroom electrical system featuring:
- GFCI outlet (main power entry point)
- Main light with 3-way switch control
- Vanity light with 3-way switch control  
- Exhaust fan with single switch control
- Proper wire configurations (2-wire and 3-wire)

## Circuit Configuration

### Power Flow Sequence
1. **GFCI Outlet** (Power entry point)
2. **Vanity Light Fixture**
3. **Vanity Light Switch #1**
4. **Main Light Switch #1**
5. **Main Light Fixture**
6. **Exhaust Fan**
7. **Main Light Switch #2**
8. **Vanity Light Switch #2**
9. **Fan Switch**

## Detailed Wiring Diagram

```
ELECTRICAL PANEL
      |
      | 14-2 w/Ground (15A Circuit)
      ↓
┌─────────────────┐
│   GFCI OUTLET   │ ← Main power entry point
│   (15A, 120V)   │
└─────────────────┘
      |
      | 12-2 w/Ground
      ↓
┌─────────────────┐
│  VANITY LIGHT   │
│   FIXTURE       │
└─────────────────┘
      |
      | 14-3 w/Ground (for 3-way switching)
      ↓
┌─────────────────┐
│ VANITY SWITCH 1 │ ← First 3-way switch for vanity
│   (3-way)       │
└─────────────────┘
      |
      | 14-3 w/Ground
      ↓
┌─────────────────┐
│ MAIN SWITCH 1   │ ← First 3-way switch for main light
│   (3-way)       │
└─────────────────┘
      |
      | 14-3 w/Ground
      ↓
┌─────────────────┐
│  MAIN LIGHT     │
│   FIXTURE       │
└─────────────────┘
      |
      | 14-2 w/Ground
      ↓
┌─────────────────┐
│  EXHAUST FAN    │
└─────────────────┘
      |
      | 14-3 w/Ground
      ↓
┌─────────────────┐
│ MAIN SWITCH 2   │ ← Second 3-way switch for main light
│   (3-way)       │
└─────────────────┘
      |
      | 14-3 w/Ground (traveler wires back to vanity)
      ↓
┌─────────────────┐
│ VANITY SWITCH 2 │ ← Second 3-way switch for vanity
│   (3-way)       │
└─────────────────┘
      |
      | 14-2 w/Ground
      ↓
┌─────────────────┐
│   FAN SWITCH    │ ← Single pole switch for fan
│  (Single Pole)  │
└─────────────────┘
```

## Wire Configuration Details

### Wire Types Used:
- **14-2 w/Ground**: 2 conductor + ground (Hot, Neutral, Ground)
- **14-3 w/Ground**: 3 conductor + ground (Hot, Traveler 1, Traveler 2, Neutral, Ground)

### Wire Gauge: 14 AWG (15 Amp circuit)

## 3-Way Switch Wiring Details

### Main Light 3-Way Switches:
- **Hot (Black)**: Connects to common terminal of first 3-way switch
- **Traveler Wires (Red & Black)**: Run between both 3-way switches
- **Switched Hot**: From common terminal of second switch to light fixture
- **Neutral (White)**: Runs continuously to light fixture
- **Ground (Bare/Green)**: Connects all switches and fixtures

### Vanity Light 3-Way Switches:
- **Hot (Black)**: Tapped from main power feed
- **Traveler Wires (Red & Black)**: Run between both vanity 3-way switches  
- **Switched Hot**: From common terminal to vanity light fixture
- **Neutral (White)**: Runs continuously to vanity light fixture
- **Ground (Bare/Green)**: Connects all switches and fixtures

## Switch Terminal Connections

### 3-Way Switch Terminals:
- **Common (COM)**: Hot wire input or switched hot output
- **Traveler 1**: First traveler wire (typically red)
- **Traveler 2**: Second traveler wire (typically black)
- **Ground**: Green/bare ground wire

### Single Pole Fan Switch:
- **Hot In**: Black wire from power source
- **Hot Out**: Black wire to fan
- **Neutral**: White wire (pigtailed in box)
- **Ground**: Green/bare ground wire

## Installation Notes

⚠️ **SAFETY WARNING**: All electrical work should be performed by a licensed electrician and must comply with local electrical codes.

### Key Installation Points:
1. **GFCI Protection**: Required for all bathroom outlets and must be first in the circuit
2. **Circuit Rating**: 15A circuit recommended for bathroom with multiple fixtures
3. **Wire Gauge**: 14 AWG wire required for 15A circuit
4. **Grounding**: All metal fixtures and switch boxes must be properly grounded
5. **Box Fill**: Ensure electrical boxes are large enough for wire connections
6. **Code Compliance**: Installation must meet NEC (National Electrical Code) requirements

### Testing:
1. Test GFCI outlet with test/reset buttons
2. Verify all switches operate their intended fixtures
3. Check that 3-way switches work from both locations
4. Confirm proper grounding with multimeter

## Materials List

### Wire:
- 14-2 w/Ground NM-B cable (approximately 50 feet)
- 14-3 w/Ground NM-B cable (approximately 75 feet)

### Devices:
- 1x GFCI outlet (15A, 120V)
- 4x 3-way switches
- 1x Single pole switch
- Wire nuts (assorted sizes)
- Electrical boxes (appropriate sizes)

### Fixtures:
- 1x Main light fixture
- 1x Vanity light fixture  
- 1x Exhaust fan

## Troubleshooting Guide

### 3-Way Switches Not Working:
1. Check traveler wire connections
2. Verify common terminal connections
3. Ensure hot wire is on correct common terminal

### GFCI Tripping:
1. Check for ground faults
2. Verify neutral connections
3. Test load balance

### Fan Not Working:
1. Check single pole switch connections
2. Verify power to fan
3. Check fan motor connections
