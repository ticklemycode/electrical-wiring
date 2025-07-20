# Bathroom Electrical Wiring Diagram - Linear Feed-Through Design

[![Code Compliant](https://img.shields.io/badge/NEC-Compliant-green.svg)](https://www.nfpa.org/codes-and-standards/all-codes-and-standards/list-of-codes-and-standards/detail?code=70)
[![Safety](https://img.shields.io/badge/Safety-GFCI_Protected-blue.svg)](#safety-considerations)
[![Design](https://img.shields.io/badge/Design-Linear_Feed_Through-orange.svg)](#design-overview)

## 🏠 Project Overview

This project documents a **complete bathroom electrical wiring system** using a **linear feed-through design** that provides:

- ⚡ **GFCI Protection** for the entire bathroom circuit
- 💡 **Main Light** with 3-way switch control (2 locations)  
- 🪩 **Vanity Light** with 3-way switch control (2 locations)
- 🌀 **Exhaust Fan** with single-pole switch control
- 🔌 **GFCI Outlet** for bathroom electrical needs

## 🎯 System Features

### **Linear Power Flow**
Power flows efficiently through the physical box layout:
```
Box 1 (GFCI) → Box 2 (Vanity SW) → Box 4 (Main SW) → Box 7 (Control Center)
```

### **Smart Control Layout**
- **Box 2**: Vanity Light Switch 1 (3-way)
- **Box 4**: Main Light Switch 1 (3-way) 
- **Box 7**: Control Center with all secondary switches:
  - Main Light Switch 2 (3-way)
  - Vanity Light Switch 2 (3-way)
  - Fan Switch (single-pole)

### **Code-Compliant Design**
✅ All white wires used only as neutrals  
✅ Proper GFCI protection throughout  
✅ Standard 14 AWG wire for 15A circuit  
✅ Equipment grounding for all devices  
✅ NEC-compliant box fill calculations  

## 📁 Project Structure

```
bathroom-wire-diagram/
├── README.md                           # Project overview (this file)
├── diagrams/
│   └── linear-design-mermaid.md        # Complete wiring diagram with Mermaid
├── docs/
│   └── switch-wiring-guide.md          # Box-by-box wiring instructions
├── LINEAR-INSTALLATION-MATERIALS.md    # Materials list & installation guide
├── 3WAY-SWITCH-VERIFICATION.md         # 3-way switch operation verification
├── COMPLETE-SYSTEM-VERIFICATION.md     # Comprehensive electrical flow analysis
└── PROJECT-COMPLETION.md               # Final project summary
```

## 🚀 Quick Start

### **1. View the Complete Wiring Diagram**
📄 **[Linear Design Mermaid Diagram](diagrams/linear-design-mermaid.md)**
- Visual flowchart showing all connections
- Color-coded cable specifications  
- Wire-by-wire breakdown
- System operation explanation

### **2. Get Materials & Installation Guide**  
📄 **[Linear Installation Materials](LINEAR-INSTALLATION-MATERIALS.md)**
- Complete materials list with quantities
- Cable run specifications table
- Step-by-step installation sequence
- Box fill calculations

### **3. Wire the Switches**
📄 **[Switch Wiring Guide](docs/switch-wiring-guide.md)**
- Box-by-box connection instructions
- Wire nut groupings for each box
- Device terminal connections
- Testing procedures

### **4. Verify 3-Way Switch Operation**
📄 **[3-Way Switch Verification](3WAY-SWITCH-VERIFICATION.md)**
- Circuit analysis for vanity and main light controls
- Visual diagrams showing traveler wire paths
- Truth tables for all switch positions
- Verification that switches work as expected

### **5. Complete System Analysis**
📄 **[Complete System Verification](COMPLETE-SYSTEM-VERIFICATION.md)**
- Comprehensive hot and neutral flow analysis
- Every switch position combination tested
- Complete electrical path verification
- System-wide state matrix with all operating conditions

## 🔧 System Specifications

| Component | Specification | Notes |
|-----------|---------------|-------|
| **Circuit** | 15A, 120V | Standard bathroom circuit |
| **Wire Gauge** | 14 AWG | NM-B cable throughout |
| **GFCI Protection** | Box 1 LINE/LOAD | Protects entire circuit |
| **Total Cables** | 8 cables | 6 × 14-2 + 2 × 14-3 |
| **Total Boxes** | 7 boxes | 4 switches + 1 outlet + 2 fixtures |
| **Switch Types** | 4 × 3-way, 1 × single-pole | All 15A rated |

## 🎮 How It Works

### **Power Distribution**
1. **Panel** → **Box 1**: Main 15A feed to GFCI outlet
2. **Box 1** → **Box 2**: Protected power continues to vanity switch  
3. **Box 2** → **Box 4**: Power continues to main light switch
4. **Box 4** → **Box 7**: Final power feed to control center

### **3-Way Switch Operation**

#### **Vanity Light Control**
- **Switch 1** (Box 2): Controls vanity light via travelers to Box 7
- **Switch 2** (Box 7): Receives travelers, sends switched hot back to vanity

#### **Main Light Control**  
- **Switch 1** (Box 4): Controls main light via travelers to Box 7
- **Switch 2** (Box 7): Receives travelers, sends switched hot back to main light

### **Fan Control**
- **Single Switch** (Box 7): Direct control of exhaust fan

## 🛡️ Safety Considerations

⚠️ **ELECTRICAL WORK WARNING**: This project involves electrical wiring that can cause serious injury or death if performed incorrectly. 

### **Before Starting**
- ✋ **Hire a Licensed Electrician** if you're not qualified
- 🔌 **Turn OFF power** at the breaker before any work
- 🧪 **Test circuits** with a non-contact voltage tester
- 📖 **Check local codes** - requirements may vary by location

### **GFCI Requirements**
- 🛡️ **GFCI protection required** for all bathroom outlets (NEC 210.8)
- 🔄 **Monthly testing recommended** using TEST/RESET buttons
- ⚡ **Replace immediately** if GFCI fails to trip or reset

### **Bathroom-Specific Codes**
- 📏 **Box placement**: Follow height and clearance requirements  
- 💧 **Moisture protection**: Use appropriate boxes and covers
- 🌡️ **Ventilation**: Exhaust fan required in bathrooms without windows

## 🎨 Design Advantages

### **Why Linear Feed-Through?**
✅ **Follows Natural Flow**: Power moves in logical box order  
✅ **Simple GFCI Wiring**: Only 2 cables at GFCI (LINE/LOAD)  
✅ **Standard Practice**: Most common residential approach  
✅ **Easy Troubleshooting**: Clear power path to follow  
✅ **Efficient Installation**: Install boxes in sequence  

### **User Benefits**
✅ **Convenient Control**: All primary switches in Box 7  
✅ **Full 3-Way Function**: Control lights from 2 locations each  
✅ **Logical Layout**: Switch locations match room usage  
✅ **Future Maintenance**: Easy to trace and service  

## 📞 Support & Resources

### **Documentation**
- 🔗 **[National Electrical Code (NEC)](https://www.nfpa.org/codes-and-standards/all-codes-and-standards/list-of-codes-and-standards/detail?code=70)** - Official electrical code
- 🏠 **Local Building Department** - Permit and inspection requirements
- 👷 **Licensed Electrician** - Professional installation and consultation

### **Tools Required**
- Wire strippers and cutters
- Non-contact voltage tester  
- Drill with bits for box installation
- Fish tape or wire pulling system
- Screwdrivers (flathead and Phillips)
- Wire nuts and electrical tape

## ⚖️ Legal Disclaimer

This documentation is for educational and planning purposes only. Electrical work must comply with local codes and regulations. Installation should be performed by qualified individuals or licensed electricians. The authors assume no responsibility for improper installation or code violations.

---

**📧 Questions?** Review the detailed documentation in the `diagrams/` and `docs/` folders, or consult with a licensed electrician for your specific installation requirements.
