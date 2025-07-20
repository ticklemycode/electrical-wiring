# REVISED DESIGN ANALYSIS - Code Compliance Check

## Current Physical Layout (Confirmed)
- Box 1: GFCI Outlet
- Box 2: Vanity Switch 1 (single gang)
- Box 3: Vanity Light Fixture
- Box 4: Main Switch 1 (single gang)
- Box 5: Main Light Fixture
- Box 6: Fan
- Box 7: Control Center - Main Switch 2 + Vanity Switch 2 + Fan Switch (triple gang)

## PROBLEM IDENTIFIED: GFCI Distribution

The current design has Box 1 (GFCI) feeding power to three separate locations:
- Box 1 → Box 2 (14-2)
- Box 1 → Box 4 (14-2)  
- Box 1 → Box 7 (14-2)

**Issue**: A GFCI outlet only has one LINE input and one LOAD output. It cannot directly feed three separate circuits without additional splicing.

## CORRECTED POWER DISTRIBUTION OPTIONS

### Option A: Linear Feed-Through
```
Panel → Box 1 (GFCI) → Box 7 (Control Center) → Box 2 & Box 4
```

Power flows: Panel → GFCI → Control Center → Individual switches
- Box 7 becomes power distribution point AND control center
- Requires more complex wiring in Box 7

### Option B: GFCI with Junction Box
```
Panel → Box 1 (GFCI) → Junction → Box 2, Box 4, Box 7
```

Add a separate junction box after GFCI to split power
- Requires additional box
- More complex installation

### Option C: Hub at Control Center (RECOMMENDED)
```
Panel → Box 1 (GFCI) → Box 7 (Control Center) → distribute to Box 2 & Box 4
```

Box 7 serves dual purpose:
1. Control center (3 switches)
2. Power distribution hub

## RECOMMENDED SOLUTION: Option C

### Cable Layout:
1. **Panel → Box 1**: 14-2 (Hot/Neutral/Ground)
2. **Box 1 → Box 7**: 14-2 (Hot/Neutral/Ground) - Main power feed
3. **Box 7 → Box 2**: 14-3 (Hot + 2 Travelers + Neutral/Ground)
4. **Box 7 → Box 4**: 14-3 (Hot + 2 Travelers + Neutral/Ground)
5. **Box 7 → Box 3**: 14-2 (Switched Hot/Neutral/Ground) - to Vanity Light
6. **Box 7 → Box 5**: 14-2 (Switched Hot/Neutral/Ground) - to Main Light  
7. **Box 7 → Box 6**: 14-2 (Switched Hot/Neutral/Ground) - to Fan

**Total**: 5 × 14-2 + 2 × 14-3 cables

### Neutral Flow Verification:
- **Source**: Panel neutral → GFCI → Box 7
- **Vanity Light**: Box 7 → Box 2 (via 14-3) → back to Box 7 → to Box 3 (fixture)
- **Main Light**: Box 7 → Box 4 (via 14-3) → back to Box 7 → to Box 5 (fixture)  
- **Fan**: Box 7 → Box 6 (direct via 14-2)

### Hot Flow Verification:
- **Power**: Panel → GFCI → Box 7 (distribution)
- **Vanity 3-way**: Box 7 hot → Box 2 (SW1) ←→ Box 7 (SW2) → Box 3 (fixture)
- **Main 3-way**: Box 7 hot → Box 4 (SW1) ←→ Box 7 (SW2) → Box 5 (fixture)
- **Fan**: Box 7 hot → Fan Switch → Box 6 (fixture)

### Code Compliance:
✅ **GFCI Protection**: Single feed from GFCI protects all circuits
✅ **Standard Cables**: Only 14-2 and 14-3 used
✅ **Proper Neutrals**: All white wires function as neutrals
✅ **Box Fill**: Box 7 will need large capacity (triple gang + wire nuts)
✅ **Grounding**: Continuous ground path to all devices

## ISSUE: Box 7 Complexity

Box 7 becomes very complex with:
- 3 switches
- 2 incoming 14-3 cables (from Box 2 & 4)
- 1 incoming 14-2 cable (from GFCI)
- 3 outgoing 14-2 cables (to fixtures)
- Multiple wire nuts for hot, neutral, ground distribution

**Total wires in Box 7**: ~18-20 wires + 3 switches
This requires a very large box and careful wire management.

## ALTERNATIVE: Simplified Single-Pole Design

Consider making vanity light single-pole only (controlled from Box 7 only):
- Eliminates Box 2 entirely
- Reduces Box 7 complexity significantly
- Still provides 3-way control for main light (Box 4 ↔ Box 7)
- Much simpler installation and maintenance

Would this be acceptable?
