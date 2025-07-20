# Linear Design - Installation Materials & Guide

## Project Overview
This document provides the complete materials list and installation guide for the **linear feed-through bathroom electrical system**. This design follows the physical box layout with power flowing linearly from Box 1 → Box 2 → Box 4 → Box 7.

## ⚡ System Specifications
- **Circuit**: 15A, 120V bathroom circuit with GFCI protection
- **Design Type**: Linear feed-through with 3-way switching
- **Power Flow**: Box 1 (GFCI) → Box 2 (Vanity SW 1) → Box 4 (Main SW 1) → Box 7 (Control Center)
- **Total Cables**: 6 × 14-2 NM-B + 2 × 14-3 NM-B = 8 cables

## 📋 Required Materials

### Electrical Wire & Cable
| Item | Quantity | Specification | Usage |
|------|----------|---------------|-------|
| 14-2 NM-B Cable | 200 feet | 14 AWG, 2 conductor + ground | Power feeds and fixture connections |
| 14-3 NM-B Cable | 100 feet | 14 AWG, 3 conductor + ground | 3-way traveler circuits |
| Wire Nuts (Red) | 1 box | 12-14 AWG capacity | Hot and neutral splicing |
| Wire Nuts (Yellow) | 1 box | 14-16 AWG capacity | Ground splicing |
| Electrical Tape | 2 rolls | Black, 3/4" × 60' | Securing connections |
| Cable Staples | 1 box | For 14 AWG NM-B | Securing cable runs |

### Electrical Devices
| Item | Quantity | Specification | Notes |
|------|----------|---------------|-------|
| GFCI Outlet | 1 | 15A, 120V, Self-Test | Must be tamper-resistant for bathroom |
| 3-Way Switches | 4 | 15A, 120V, Grounding | 2 for main light, 2 for vanity light |
| Single-Pole Switch | 1 | 15A, 120V, Grounding | For exhaust fan |
| Switch Plates | 3 | 1-gang (2), 3-gang (1) | Box 2, Box 4, Box 7 |
| GFCI Cover Plate | 1 | Standard single-gang | Box 1 |

### Electrical Boxes
| Item | Quantity | Specification | Usage |
|------|----------|---------------|-------|
| Single Gang Box | 2 | 18 cubic inch minimum | Box 2 (Vanity SW 1), Box 4 (Main SW 1) |
| Triple Gang Box | 1 | 45 cubic inch minimum | Box 7 (Control Center - 3 switches) |
| GFCI Outlet Box | 1 | Standard single gang, 18 cubic inch | Box 1 (GFCI Outlet) |
| Fixture Boxes | 3 | Appropriate for fixture type | Box 3, Box 5, Box 6 |

### Hardware & Accessories
| Item | Quantity | Specification | Notes |
|------|----------|---------------|-------|
| Cable Connectors | 16 | 1/2" NM-B clamps | 2 per box entry |
| Box Screws | 1 box | #6-32 × 1" | Mounting devices |
| Grounding Pigtails | 10 | 12" × 14 AWG green | Device grounding |
| Cable Labels | 1 roll | Self-adhesive | Identifying cable runs |

## 🔌 Cable Run Specifications

### Power Feed Cables (14-2 NM-B)
| Run # | Cable Route | Length Est. | Black Wire | White Wire | Purpose |
|-------|-------------|-------------|------------|------------|---------|
| 1 | Panel → Box 1 | 25 feet | Hot (120V) | Neutral | Main power supply |
| 2 | Box 1 → Box 2 | 15 feet | Protected Hot | Protected Neutral | Power to vanity circuit |
| 3 | Box 2 → Box 4 | 20 feet | Hot (continues) | Neutral (continues) | Power continuation |
| 4 | Box 4 → Box 7 | 25 feet | Hot (end of feed) | Neutral (end of feed) | Final power feed |
| 5 | Box 2 → Box 3 | 10 feet | Switched Hot | Neutral | Vanity light feed |
| 6 | Box 4 → Box 5 | 15 feet | Switched Hot | Neutral | Main light feed |
| 7 | Box 7 → Box 6 | 10 feet | Switched Hot | Neutral | Fan feed |

### 3-Way Control Cables (14-3 NM-B)
| Run # | Cable Route | Length Est. | Black Wire | Red Wire | White Wire | Purpose |
|-------|-------------|-------------|------------|----------|------------|---------|
| 8 | Box 2 ↔ Box 7 | 30 feet | Traveler 1 | Traveler 2 | **CAPPED OFF** | Vanity 3-way control |
| 9 | Box 4 ↔ Box 7 | 20 feet | Traveler 1 | Traveler 2 | **CAPPED OFF** | Main 3-way control |

**Total Cable Required: ~170 feet of 14-2 + ~50 feet of 14-3**

## 🔧 Installation Sequence

### Phase 1: Planning & Preparation
1. **Obtain Permits**: Check local requirements for electrical work
2. **Turn Off Power**: De-energize circuit at main panel
3. **Verify Power Off**: Use non-contact voltage tester
4. **Plan Cable Routes**: Mark all box locations and cable paths

### Phase 2: Box Installation
1. **Install Box 1**: GFCI outlet location (power entry point)
2. **Install Box 2**: Vanity switch location (single gang)
3. **Install Box 4**: Main switch location (single gang)
4. **Install Box 7**: Control center location (triple gang)
5. **Install Fixture Boxes**: Box 3 (vanity), Box 5 (main), Box 6 (fan)

### Phase 3: Cable Installation
**Install in this order to follow power flow:**
1. **Run Cable 1**: Panel → Box 1 (main power feed)
2. **Run Cable 2**: Box 1 → Box 2 (first power segment)
3. **Run Cable 3**: Box 2 → Box 4 (power continuation)
4. **Run Cable 4**: Box 4 → Box 7 (final power segment)
5. **Run Cable 5**: Box 2 → Box 3 (vanity light)
6. **Run Cable 6**: Box 4 → Box 5 (main light)
7. **Run Cable 7**: Box 7 → Box 6 (fan)
8. **Run Cable 8**: Box 2 ↔ Box 7 (vanity 3-way travelers)
9. **Run Cable 9**: Box 4 ↔ Box 7 (main 3-way travelers)

### Phase 4: Device Installation
**Wire devices in this order:**
1. **Box 1**: GFCI outlet (simplest - LINE/LOAD only)
2. **Box 2**: Vanity Switch 1 + power distribution
3. **Box 4**: Main Switch 1 + power distribution
4. **Box 7**: All three switches (most complex)
5. **Fixture Boxes**: Connect all lights and fan

### Phase 5: Testing & Commissioning
1. **Visual Inspection**: Check all connections and wire nuts
2. **Continuity Testing**: Test all circuits before energizing
3. **Power On**: Restore power at main panel
4. **GFCI Testing**: Test and reset GFCI outlet
5. **Switch Testing**: Test all switch combinations
6. **Final Testing**: Verify all fixtures operate correctly

## ⚠️ Critical Safety Notes

### GFCI Requirements
- **Bathroom Code**: All bathroom outlets must be GFCI protected
- **Circuit Protection**: GFCI protects entire downstream circuit
- **Monthly Testing**: Test GFCI monthly using TEST/RESET buttons
- **Proper Wiring**: LINE (from panel) and LOAD (to circuit) must be correct

### Wire Management
- **Box Fill**: Do not exceed NEC 314.16 box fill calculations
- **Wire Nuts**: Use proper size for conductor count and gauge
- **Grounding**: All devices and boxes must be properly grounded
- **Cable Support**: Secure cables within 12" of boxes

### Code Compliance
- **NEC Compliance**: All work must meet National Electrical Code
- **Local Codes**: Check local amendments and requirements
- **Permit Requirements**: Some jurisdictions require permits for electrical work
- **Professional Installation**: Consider hiring licensed electrician if uncertain

---
*This linear design provides the most efficient and standard approach for bathroom electrical installation while ensuring full code compliance and safety.*
