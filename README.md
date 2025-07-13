# Bathroom Electrical Wiring Diagram

## Project Overview
This document provides a complete wiring diagram and installation guide for a bathroom electrical system featuring:
- GFCI outlet (main power entry point)
- Main light with 3-way switch control
- Vanity light with 3-way switch control  
- Exhaust fan with single switch control
- Proper wire configurations (2-wire and 3-wire)

## Circuit Configuration

### Quick Wire Flow Overview
```
⚫ HOT WIRE FLOW:
Panel → GFCI → Vanity Switch 1 → Vanity Light (switched) + Combined Switch Box → Main Light (switched) → Fan Switch → Fan Motor

⚪ NEUTRAL WIRE FLOW:  
Panel → GFCI → All Fixtures → Return to Panel

🟢 GROUND WIRE FLOW:
Panel → All Devices & Boxes → Return to Panel
```

### Power Flow Sequence
1. **GFCI Outlet** (Power entry point)
2. **Vanity Switch #1** (separate box - controls vanity light)
3. **Vanity Light Fixture** (switched from VS1)
4. **Combined Switch Box** (Main Switch #1, Vanity Switch #2, Fan Switch)
5. **Main Light Switch #2** (separate box)
6. **Main Light Fixture**
7. **Exhaust Fan**

## Switch Box Configuration

### Switch Box Locations:
- **Vanity Switch 1**: Separate single-gang box
- **Combined Switch Box**: Triple-gang box containing:
  - Main Switch 1 (3-way for main light)
  - Vanity Switch 2 (3-way for vanity light)  
  - Fan Switch (single pole for exhaust fan)
- **Main Switch 2**: Separate single-gang box (3-way for main light)

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
      | 14-2 w/Ground
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
│  EXHAUST FAN    │ ← Hot wire passes through; controlled by switch downstream
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
- **Hot In**: Black wire from continuous circuit power
- **Hot Out**: Black wire back to fan (control wire)
- **Neutral**: White wire (pigtailed in box)
- **Ground**: Green/bare ground wire

**Note**: The fan switch receives continuous power from the circuit but sends switched power back to the fan location.

## Fan Control Configuration

**Important**: The exhaust fan is controlled by a switch located in the combined switch box downstream from the fan itself. Here's how this works:

1. **Continuous Hot Wire**: Runs from the main light → through the fan junction box → continues to the combined switch box
2. **Fan Location**: Between the main light and the combined switch box
3. **Fan Switch Location**: In the combined switch box with Main Switch 1 and Vanity Switch 2

### Combined Switch Box Benefits:
- **Convenient Control**: All three switches in one location
- **Simplified Wiring**: Shared neutral and ground connections
- **Standard Installation**: Common bathroom switch configuration
- **Proper Operation**: 3-way switches still function normally despite shared box
4. **Control Method**: Fan switch sends switched hot wire back to the fan

This configuration allows the fan switch to be grouped with other switches while the fan is positioned optimally in the ceiling.

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

## Detailed Documentation

For complete implementation details, see:

📋 **[Materials & Installation Guide](docs/materials-installation.md)**
- Complete materials list with specifications  
- Step-by-step installation instructions
- GFCI wiring details and safety procedures

🔧 **[Switch Wiring Guide](docs/switch-wiring-guide.md)**
- Detailed 3-way switch terminal connections
- Point-to-point wire routing
- Fixture installation steps
- Quick reference charts and troubleshooting

📊 **[Complete Layout Diagram](diagrams/complete-layout.md)**  
- Physical layout and wire routing
- Junction box details
- Switch box configurations

🔀 **[Mermaid Wiring Diagram](diagrams/mermaid-wiring-diagram.md)**
- Interactive flowchart diagram
- Visual circuit flow representation

---

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

### Corrected Circuit Flow Logic

**New Logical Path:**
```
Panel → GFCI → Vanity Switch 1 → Vanity Light (switched)
                     ↓
              Combined Switch Box → Main Switch 2 → Main Light → Fan → Back to Combined
```

**Key Improvements:**
1. **Simplified Vanity Light Wiring**: No red traveler wire passes through light fixture
2. **Standard 3-Way Operation**: VS1 directly switches hot to vanity light
3. **Cleaner Cable Routing**: Each fixture gets appropriate cable type (14-2 or 14-3)
4. **Logical Power Flow**: Power goes to switch first, then to controlled device

**Cable Types by Connection:**
- GFCI → Vanity Switch 1: **14-2** (hot, neutral, ground)
- Vanity Switch 1 → Vanity Light: **14-2** (switched hot, neutral, ground)  
- Vanity Switch 1 → Combined Box: **14-3** (hot continuation, travelers, neutral, ground)
- Combined Box → Main Switch 2: **14-3** (switched hot, travelers, neutral, ground)
- Main Switch 2 → Main Light: **14-2** (switched hot, neutral, ground)
- Main Light → Fan → Combined Box: **14-2** (pass-through + control)
