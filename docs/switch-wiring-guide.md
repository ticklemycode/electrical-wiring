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
INCOMING POWER → 12-3 Cable to Switch 2 → 12-3 Cable to Light

Power Source (12-2):          To Switch 2 (12-3):         To Light (12-3):
- Hot (Black)    →  COM       - Traveler 1 (Red)   →  T1  - Switched Hot → COM
- Neutral (White) → Pigtail   - Traveler 2 (Black) →  T2  - Neutral     → Light
- Ground (Bare)   → Switch    - Ground (Bare)      →  GND - Ground      → GND
```

### Switch Box 2 (Main Switch 2):
```
From Switch 1 (12-3):         To Light Fixture (12-2):
- Traveler 1 (Red)   →  T1    - Switched Hot (Black) →  COM
- Traveler 2 (Black) →  T2    - Neutral (White)      →  Pigtail
- Ground (Bare)      →  GND   - Ground (Bare)        →  Switch
```

## Vanity Light 3-Way Wiring Configuration

### Vanity Switch 1:
```
From Main Circuit (12-3):     To Vanity Switch 2 (12-3):  To Vanity Light:
- Hot (Black)     →  COM      - Traveler 1 (Red)   →  T1  - Switched Hot
- Neutral (White) →  Pigtail  - Traveler 2 (Black) →  T2  - Neutral
- Ground (Bare)   →  Switch   - Ground (Bare)      →  GND - Ground
```

### Vanity Switch 2:
```
From Vanity Switch 1 (12-3):  To Vanity Light Fixture:
- Traveler 1 (Red)   →  T1    - Switched Hot (Black) →  COM
- Traveler 2 (Black) →  T2    - Neutral (White)      →  Light
- Ground (Bare)      →  GND   - Ground (Bare)        →  Light & Switch
```

## Wire Color Code Standards

### 12-2 Cable:
- **Black**: Hot (Line/Load)
- **White**: Neutral
- **Bare/Green**: Ground

### 12-3 Cable:
- **Black**: Hot or Traveler
- **Red**: Traveler
- **White**: Neutral (sometimes used as traveler when properly marked)
- **Bare/Green**: Ground

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
│  12-2 FROM PANEL    12-3 TO SWITCH2│
│  ┌─ Black (Hot)  ────── COM         │
│  │  White (Neutral) ── Splice ──┐   │
│  │  Ground ─────────── GND ──┐  │   │
│  │                           │  │   │
│  │  12-3 TO LIGHT            │  │   │
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
│  12-3 FROM SWITCH1  12-2 TO LIGHT  │
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
