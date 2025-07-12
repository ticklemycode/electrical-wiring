# Materials List and Installation Guide

## Required Materials

### Electrical Wire
| Item | Quantity | Specification | Usage |
|------|----------|---------------|-------|
| 12-2 NM-B Cable | 50 feet | 12 AWG, 2 conductor + ground | Power feeds, simple connections |
| 12-3 NM-B Cable | 75 feet | 12 AWG, 3 conductor + ground | 3-way switch travelers |
| Wire Nuts | 1 box each | Yellow (small), Red (medium) | Wire connections |
| Electrical Tape | 2 rolls | 3/4" x 60' | Securing connections |

### Electrical Devices
| Item | Quantity | Specification | Notes |
|------|----------|---------------|-------|
| GFCI Outlet | 1 | 20A, 120V, Self-Test | Must be first device in circuit |
| 3-Way Switches | 4 | 15A, 120V | 2 for main light, 2 for vanity |
| Single Pole Switch | 1 | 15A, 120V | For exhaust fan |
| Switch Plates | 3 | 1-gang, 2-gang, 3-gang | Based on switch groupings |
| Outlet Cover | 1 | Standard GFCI cover | Weather-resistant if needed |

### Electrical Boxes
| Item | Quantity | Specification | Usage |
|------|----------|---------------|-------|
| Switch Boxes | 3 | 18-22 cubic inch capacity | Multiple switches per box |
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
- Wire strippers (12-14 AWG)
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

Circuit Capacity: 20A × 120V = 2400W
Load Percentage: 430W ÷ 2400W = 18% (Well within safe limits)
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
1. Panel → GFCI Outlet (12-2)
2. GFCI → Vanity Light (12-2)
3. Vanity Light → Switch Box 1 (12-3)
4. Switch Box 1 → Switch Box 2 (12-3)
5. Switch Box 2 → Main Light (12-3)
6. Main Light → Fan (12-2)
7. Switch Box 3 → Fan (12-2 control)

Notes:
- Leave 8" of cable at each box
- Secure cable every 4.5 feet
- Use cable staples within 12" of boxes
- Protect cable through framing
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

#### Step 5: Single Pole Fan Switch
```
Fan Switch Connections:
┌─────────────────┐
│  SINGLE POLE    │
│  Hot  Load  Gnd │
└───┬────┬────┬───┘
    │    │    └─ Ground to fan and box
    │    └────── Control wire to fan
    └─────────── Hot from power source
```

### Phase 3: Testing and Verification

#### Step 6: Circuit Testing
```
Testing Sequence:
1. Power OFF verification:
   - Test with non-contact voltage tester
   - Verify at panel and all devices

2. Continuity testing:
   - Test all wire connections
   - Verify 3-way switch travelers
   - Check ground continuity

3. Insulation testing:
   - Check for short circuits
   - Verify proper wire separation
   - Test GFCI function

4. Load testing:
   - Install fixtures temporarily
   - Test all switch operations
   - Verify proper control functions
```

#### Step 7: Final Connections
```
Connection Sequence:
1. Connect fixtures to boxes
2. Install switch and outlet devices
3. Install cover plates
4. Test GFCI with test/reset buttons
5. Verify all switches control correct fixtures
6. Check 3-way operation from both locations
```

## Safety Procedures

### Before Starting Work
- [ ] Turn OFF power at main breaker
- [ ] Verify power is off with voltage tester
- [ ] Post warning signs at electrical panel
- [ ] Have flashlight or battery-powered lighting ready
- [ ] Ensure proper ladder safety for ceiling work

### During Installation
- [ ] Double-check wire connections before energizing
- [ ] Use proper PPE (safety glasses, gloves)
- [ ] Never work on live circuits
- [ ] Test voltage before touching any wires
- [ ] Follow manufacturer instructions for all devices

### After Installation
- [ ] Test GFCI monthly with test/reset buttons
- [ ] Verify all connections are tight
- [ ] Keep circuit directory updated
- [ ] Schedule electrical inspection if required
- [ ] Provide operation instructions to users

## Troubleshooting Common Issues

### GFCI Won't Reset
**Possible Causes:**
- Ground fault in downstream wiring
- Reversed LINE/LOAD connections
- Damaged GFCI device
- Moisture in connections

**Solutions:**
1. Check all downstream connections
2. Verify LINE/LOAD wiring
3. Test with multimeter
4. Replace GFCI if faulty

### 3-Way Switches Don't Work Properly
**Possible Causes:**
- Incorrect traveler connections
- Wrong common terminal usage
- Crossed neutral wires

**Solutions:**
1. Verify traveler wire continuity
2. Check common terminal connections
3. Trace neutral path
4. Test switch operation sequence

### Fan Won't Turn On
**Possible Causes:**
- Loose switch connections
- Faulty fan motor
- Incorrect neutral connections
- Tripped GFCI upstream

**Solutions:**
1. Check switch wiring
2. Test voltage at fan
3. Verify neutral connections
4. Reset GFCI if tripped

## Code References

### National Electrical Code (NEC) Sections:
- **Article 210**: Branch Circuits
- **Article 250**: Grounding and Bonding  
- **Article 314**: Outlet, Device, Pull, and Junction Boxes
- **Article 404**: Switches
- **Article 406**: Receptacles, Cord Connectors, and Attachment Plugs

### Local Code Considerations:
- Check with local building department
- May require electrical permit
- Professional installation may be required
- Inspection requirements vary by location
