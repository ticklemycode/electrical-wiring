# Power Flow Visualization Diagrams

## 🔌 Visual Power Flow Analysis

This document provides visual diagrams showing exactly how electrical power flows through the bathroom wiring system when switches are in various positions.

---

## ⚡ Linear Power Feed (Always Present)

### **Base Power Distribution**
```
[*] ELECTRICAL PANEL (15A Breaker)
    ║ 120V Hot (Black)
    ║ Neutral (White)  
    ║ Ground (Bare)
    ↓
[1] BOX 1: GFCI OUTLET
    ║ Protected 120V Hot <-> GFCI LINE/LOAD
    ║ Protected Neutral
    ║ Ground
    ↓
[2] BOX 2: VANITY SWITCH 1
    ║ 120V Hot (continues) <-> Power Distribution
    ║ Neutral (continues)
    ║ Ground
    ↓
[4] BOX 4: MAIN SWITCH 1  
    ║ 120V Hot (continues) <-> Power Distribution
    ║ Neutral (continues)
    ║ Ground
    ↓
[7] BOX 7: CONTROL CENTER
    * 120V Hot (end of feed) <-> Fan Switch & 3-way switches
    * Neutral (end of feed)
    * Ground
```

**Note**: This linear power feed is **always present** regardless of switch positions.

---

## 💡 Vanity Light Circuit - Power Flow When ON

### **Switch Position: Both Vanity Switches UP (Light ON)**

```
[*] ELECTRICAL PANEL
    ↓ 120V Hot
[1] BOX 1 (GFCI)
    ↓ 120V Protected Hot
[2] BOX 2 (VANITY SW 1) <-<-<-<-<-<-<-<-<-<-<-<-<-<- Switched Hot Returns
    ↓ 120V Hot (continues)         ^
    ├─ VANITY SW 1 (UP Position)   ║ 14-3 Cable
    │  COM <- 120V Hot             ║ Black Wire
    │  T1 -> Black Traveler ───────╫──────────────────┐
    │                             ║                  │
    ├─ TO BOX 3 (VANITY LIGHT) <-<-╫<- 120V Switched Hot
    │  [*] LIGHT ON (120V)         ║                  │
    │  (-) Neutral (direct)        ║                  │
    │                             ║                  ↓
[4] BOX 4 (MAIN SW 1)              ║         [7] BOX 7 (VANITY SW 2)
    ↓ 120V Hot (continues)        ║            VANITY SW 2 (UP Position)
[7] BOX 7 (CONTROL CENTER)         ║            T1 <- Black Traveler
    * 120V Hot (end of feed)      ║            COM -> Switched Hot ────╜
                                  ║
    [+] POWER PATH: Panel -> GFCI -> Box 2 SW1-COM -> T1(Black) -> Box 7 SW2-T1 -> SW2-COM -> Back to Box 2 -> Box 3 ([*] ON)
    (-) NEUTRAL PATH: Panel -> GFCI -> Box 2 -> Box 3 (Direct neutral feed)
```

---

## 💡 Main Light Circuit - Power Flow When ON

### **Switch Position: Both Main Switches UP (Light ON)**

```
[*] ELECTRICAL PANEL
    ↓ 120V Hot
[1] BOX 1 (GFCI)
    ↓ 120V Protected Hot
[2] BOX 2 (VANITY SW 1)
    ↓ 120V Hot (continues)
[4] BOX 4 (MAIN SW 1) <-<-<-<-<-<-<-<-<-<-<-<-<-<-<-<- Switched Hot Returns
    ↓ 120V Hot (continues)           ^
    ├─ MAIN SW 1 (UP Position)       ║ 14-3 Cable
    │  COM <- 120V Hot               ║ Black Wire
    │  T1 -> Black Traveler ─────────╫──────────────────┐
    │                               ║                  │
    ├─ TO BOX 5 (MAIN LIGHT) <-<-<-<-╫<- 120V Switched Hot
    │  [*] LIGHT ON (120V)           ║                  │
    │  (-) Neutral (direct)          ║                  │
    │                               ║                  ↓
[7] BOX 7 (CONTROL CENTER)           ║         [7] BOX 7 (MAIN SW 2)
    * 120V Hot (end of feed)        ║            MAIN SW 2 (UP Position)
                                    ║            T1 <- Black Traveler
                                    ║            COM -> Switched Hot ────╜

    [+] POWER PATH: Panel -> GFCI -> Box 2 -> Box 4 SW1-COM -> T1(Black) -> Box 7 SW2-T1 -> SW2-COM -> Back to Box 4 -> Box 5 ([*] ON)
    (-) NEUTRAL PATH: Panel -> GFCI -> Box 2 -> Box 4 -> Box 5 (Direct neutral feed)
```

---

## 🌀 Fan Circuit - Power Flow When ON

### **Switch Position: Fan Switch ON**

```
[*] ELECTRICAL PANEL
    ↓ 120V Hot
[1] BOX 1 (GFCI)
    ↓ 120V Protected Hot
[2] BOX 2 (VANITY SW 1)
    ↓ 120V Hot (continues)
[4] BOX 4 (MAIN SW 1)
    ↓ 120V Hot (continues)
[7] BOX 7 (CONTROL CENTER)
    ├─ 120V Hot (end of feed)
    ├─ FAN SWITCH (ON Position)
    │  Hot Terminal <- 120V
    │  Load Terminal -> 120V Switched Hot ────────────┐
    │                                                ↓
    └─ TO BOX 6 (EXHAUST FAN)                 [6] BOX 6
       [~] FAN RUNNING (120V)                     [~] EXHAUST FAN ON
       (-) Neutral (direct from Box 7)            (-) Neutral

    [+] POWER PATH: Panel -> GFCI -> Box 2 -> Box 4 -> Box 7 Fan-SW -> Box 6 ([~] ON)
    (-) NEUTRAL PATH: Panel -> GFCI -> Box 2 -> Box 4 -> Box 7 -> Box 6 (Direct neutral feed)
```

---

## 🎯 All Lights and Fan ON - Complete Power Flow

### **Switch Positions: All switches in ON positions**

```
[*] ELECTRICAL PANEL (15A Breaker - 120V Source)
    ║
    ║ [+] Hot (120V) (-) Neutral [G] Ground
    ↓
[1] BOX 1: GFCI OUTLET
    ║ GFCI Protection Active
    ║ [+] Protected Hot (-) Protected Neutral [G] Ground
    ↓
[2] BOX 2: VANITY SWITCH 1 + POWER HUB
    ║ [+] Hot (continues to Box 4)
    ║ (-) Neutral (continues to Box 4)
    ├─ VANITY SW 1 [ON] ──┐ 14-3 Travelers ┌── BOX 7 VANITY SW 2 [ON]
    │  120V -> COM    T1,T2 <─────────────-> T1,T2    COM -> 120V
    │                      └──────────────────────────────┘
    │                                                      ↓
    └─ TO BOX 3: [*] VANITY LIGHT ON (120V + Neutral) <-<-<-┘
    ↓
[4] BOX 4: MAIN SWITCH 1 + POWER HUB  
    ║ [+] Hot (continues to Box 7)
    ║ (-) Neutral (continues to Box 7)
    ├─ MAIN SW 1 [ON] ──┐ 14-3 Travelers ┌── BOX 7 MAIN SW 2 [ON]
    │  120V -> COM  T1,T2 <─────────────-> T1,T2    COM -> 120V
    │                    └────────────────────────────────┘
    │                                                    ↓
    └─ TO BOX 5: [*] MAIN LIGHT ON (120V + Neutral) <-<-<-┘
    ↓
[7] BOX 7: CONTROL CENTER (End of Linear Feed)
    ├─ [+] Hot (120V) (-) Neutral [G] Ground
    ├─ VANITY SW 2 [ON] ────-> Switched Hot returns to Box 2
    ├─ MAIN SW 2 [ON] ──────-> Switched Hot returns to Box 4
    └─ FAN SWITCH [ON] ─────-> TO BOX 6: [~] FAN ON (120V + Neutral)

[>] COMPLETE SYSTEM STATUS:
   [*] Box 3: VANITY LIGHT ON
   [*] Box 5: MAIN LIGHT ON  
   [~] Box 6: EXHAUST FAN ON
   [G] Box 1: GFCI OUTLET PROTECTED
```

---

## 🔄 3-Way Switch Logic Visualization

### **How 3-Way Switches Create/Break Circuits**

#### **Vanity Light 3-Way Circuit States**

```
SWITCHES BOTH UP (Light ON):
Box 2 SW1: COM─UP─T1(Black) ═══════════ T1(Black)─UP─COM Box 7 SW2
                                CONNECTED              ↓
                                                    Switched Hot

SWITCHES MISMATCHED (Light OFF):  
Box 2 SW1: COM─UP─T1(Black) ═════════════ T1(Black)─DOWN─O Box 7 SW2
                                NO CONNECTION         T2(Red)─UP─COM
                                                            ↓
                                                      No Power

SWITCHES BOTH DOWN (Light ON):
Box 2 SW1: COM─DOWN─T2(Red) ═══════════ T2(Red)─DOWN─COM Box 7 SW2  
                                CONNECTED               ↓
                                                    Switched Hot
```

#### **Visual Truth Table**
```
┌────────────┬────────────┬──────────────┬─────────────────┐
│ Box 2 SW1  │ Box 7 SW2  │ Connection   │ Vanity Light    │
├────────────┼────────────┼──────────────┼─────────────────┤
│     UP     │     UP     │ Via T1(Blk)  │ [*] ON (120V)   │
│     UP     │    DOWN    │ No Circuit   │ [ ] OFF (0V)    │
│    DOWN    │     UP     │ No Circuit   │ [ ] OFF (0V)    │
│    DOWN    │    DOWN    │ Via T2(Red)  │ [*] ON (120V)   │
└────────────┴────────────┴──────────────┴─────────────────┘
```

---

## 📊 Power Flow Summary

### **Key Power Flow Characteristics**

#### **✅ Linear Feed Advantages**
- **Constant Power**: Hot and neutral always available at each box
- **Sequential Distribution**: Power flows naturally through physical layout
- **Simple Troubleshooting**: Easy to trace power path
- **Standard Wiring**: No unusual connections or wire re-identification

#### **✅ 3-Way Switch Benefits**
- **Standard Operation**: Uses traditional traveler wire method
- **Reliable Switching**: Either switch can control the light
- **Return Path Logic**: Switched hot properly returns to fixture feed box
- **Code Compliant**: All connections follow NEC standards

#### **✅ System Integration**
- **Independent Circuits**: Each light circuit operates independently
- **Shared Resources**: Common power feed and neutral distribution  
- **Centralized Control**: Box 7 provides convenient primary control location
- **Safety First**: GFCI protection covers entire bathroom circuit

### **Power Flow Verification**
- **[+] Hot Paths**: All verified correct with proper switching logic  
- **(-) Neutral Paths**: All continuous and never switched (code compliant)  
- **[G] Ground Paths**: Complete equipment grounding throughout system  
- **[>] System Status**: Ready for installation with confidence

---

## 🎨 Advanced Power Flow Visualization

### **Master System Diagram - All Devices Active**

This comprehensive diagram shows power flowing through the entire system when all switches are in their ON positions.

```
                    [*] ELECTRICAL PANEL
                    ┌─────────────────────┐
                    │   15A BREAKER       │
                    │   [+] HOT (120V)    │
                    │   (-) NEUTRAL       │
                    │   [G] GROUND        │
                    └─────────┬───────────┘
                              │ 14-2 Cable
                              ▼
        ┌─────────────────────────────────────────┐
        │           [1] BOX 1: GFCI OUTLET        │
        │         [G] GFCI Receptacle             │
        │    ┌─────────────────────────────────┐  │
        │    │ LINE │ [+](-)[G] │ LOAD │ [+](-)[G] │  │
        │    └─────────────────────────────────┘  │
        │         ^                     ↓         │
        │    Panel Power         Protected Power  │
        └─────────────────────────┬───────────────┘
                                  │ 14-2 Cable  
                                  ▼
        ┌─────────────────────────────────────────┐
        │      [2] BOX 2: VANITY SWITCH 1         │
        │       [S] 3-Way Switch (UP=ON)          │
        │                                         │
        │   POWER IN      VANITY SW 1             │<─┐
        │   [+] Hot ────▶ COM <- 120V             │  │ 14-3 
        │   (-) Neutral   T1 ──┐                  │  │ Travelers
        │   [G] Ground    T2 ──┼─┐                │  │
        │                      │ │                │  │
        │   14-2 Continues     │ │                │  │
        │   ▼                  │ │                │  │
        │   TO BOX 3           │ │                │  │
        │   [*] VANITY LIGHT   │ │                │  │
        │   [+] 120V ON     <──┼─┘                │  │
        │   (-) Neutral        │                  │  │
        │   [G] Ground         │                  │  │
        └──────────────┬───────┼──────────────────┘  │
                       │       │                     │
                       ▼       │                     │
        ┌─────────────────────────────────────────┐  │
        │      [4] BOX 4: MAIN SWITCH 1           │  │
        │       [S] 3-Way Switch (UP=ON)          │  │
        │                                         │  │
        │   POWER IN      MAIN SW 1               │<─┼─┐
        │   [+] Hot ────▶ COM <- 120V             │  │ │ 14-3
        │   (-) Neutral   T1 ──┐                  │  │ │ Travelers  
        │   [G] Ground    T2 ──┼─┐                │  │ │
        │                      │ │                │  │ │
        │   14-2 Continues     │ │                │  │ │
        │   ▼                  │ │                │  │ │
        │   TO BOX 5           │ │                │  │ │
        │   [*] MAIN LIGHT     │ │                │  │ │
        │   [+] 120V ON     <──┼─┘                │  │ │
        │   (-) Neutral        │                  │  │ │
        │   [G] Ground         │                  │  │ │
        └──────────────┬───────┼──────────────────┘  │ │
                       │       │                     │ │
                       ▼       │                     │ │
        ┌─────────────────────────────────────────┐  │ │
        │     [7] BOX 7: CONTROL CENTER           │  │ │
        │    [S][S][S] Triple Gang (All ON)       │  │ │
        │                                         │  │ │
        │  VANITY SW2    MAIN SW2     FAN SW      │  │ │
        │  T1<──────┐    T1<─────┐   [+]120V     │  │ │
        │  T2<──────┼┐   T2<─────┼┐    ↓         │  │ │
        │  COM ─────┼┼┐  COM ────┼┼┐   TO BOX 6   │  │ │
        │           ↓││          ↓││   [~] FAN    │  │ │
        │    Returns││└─Returns──┘││   120V ON    │  │ │
        │    to Box ││  to Box 4  ││              │  │ │
        │    2      ▼│            ▼│              │  │ │
        │   120V     │   120V      │              │  │ │
        │   Switch   │   Switch    │              │  │ │
        │   Hot to   │   Hot to    │              │  │ │
        │   Vanity   │   Main      │              │  │ │
        └───────────────────────────────────────────┘  │ │
                                                       │ │
        [<->] TRAVELER CONNECTIONS                     │ │
        Vanity: Box 2 <──14-3 Cable──────────────────▶┘ │
        Main:   Box 4 <──14-3 Cable────────────────────▶┘
```

```
                    🏠 ELECTRICAL PANEL
                    ┌─────────────────────┐
                    │   15A BREAKER       │
                    │   🔴 HOT (120V)     │
                    │   ⚪ NEUTRAL        │
                    │   🟢 GROUND         │
                    └─────────┬───────────┘
                              │ 14-2 Cable
                              ▼
        ┌─────────────────────────────────────────┐
        │           📦 BOX 1: GFCI OUTLET         │
        │         🔌 GFCI Receptacle              │
        │    ┌─────────────────────────────────┐  │
        │    │ LINE │ 🔴⚪🟢 │ LOAD │ 🔴⚪🟢 │  │
        │    └─────────────────────────────────┘  │
        │         ↑                     ↓         │
        │    Panel Power         Protected Power  │
        └─────────────────────────┬───────────────┘
                                  │ 14-2 Cable  
                                  ▼
        ┌─────────────────────────────────────────┐
        │      📦 BOX 2: VANITY SWITCH 1          │
        │       🔘 3-Way Switch (UP=ON)           │
        │   ┌─────────────┐     ┌───────────────┐ │
        │   │ POWER IN    │     │ VANITY SW 1   │ │
        │   │ 🔴 Hot      │────▶│ COM ← 120V    │ │
        │   │ ⚪ Neutral  │     │ T1 ──┐       │ │◄─┐
        │   │ 🟢 Ground   │     │ T2 ──┼─┐     │ │  │ 14-3 
        │   └─────────────┘     └──────┼─┼─────┘ │  │ Travelers
        │           │                  │ │       │  │
        │           │ 14-2 Continues   │ │       │  │
        │           ▼                  │ │       │  │
        │   ┌───────────────────┐      │ │       │  │
        │   │   TO BOX 3        │      │ │       │  │
        │   │ 💡 VANITY LIGHT   │◄─────┼─┘       │  │
        │   │   🔴 120V ON      │      │         │  │
        │   │   ⚪ Neutral      │      │         │  │
        │   │   🟢 Ground      │      │         │  │
        │   └───────────────────┘      │         │  │
        └──────────────┬───────────────┼─────────┘  │
                       │ 14-2 Cable    │            │
                       ▼               │            │
        ┌─────────────────────────────────────────┐  │
        │      📦 BOX 4: MAIN SWITCH 1            │  │
        │       🔘 3-Way Switch (UP=ON)           │  │
        │   ┌─────────────┐     ┌───────────────┐ │  │
        │   │ POWER IN    │     │ MAIN SW 1     │ │  │
        │   │ 🔴 Hot      │────▶│ COM ← 120V    │ │◄─┼─┐
        │   │ ⚪ Neutral  │     │ T1 ──┐       │ │  │ │ 14-3
        │   │ 🟢 Ground   │     │ T2 ──┼─┐     │ │  │ │ Travelers  
        │   └─────────────┘     └──────┼─┼─────┘ │  │ │
        │           │                  │ │       │  │ │
        │           │ 14-2 Continues   │ │       │  │ │
        │           ▼                  │ │       │  │ │
        │   ┌───────────────────┐      │ │       │  │ │
        │   │    TO BOX 5       │      │ │       │  │ │
        │   │ 💡 MAIN LIGHT     │◄─────┼─┘       │  │ │
        │   │   🔴 120V ON      │      │         │  │ │
        │   │   ⚪ Neutral      │      │         │  │ │
        │   │   🟢 Ground      │      │         │  │ │
        │   └───────────────────┘      │         │  │ │
        └──────────────┬───────────────┼─────────┘  │ │
                       │ 14-2 Cable    │            │ │
                       ▼               │            │ │
        ┌─────────────────────────────────────────┐  │ │
        │     📦 BOX 7: CONTROL CENTER            │  │ │
        │    🔘🔘🔘 Triple Gang (All ON)          │  │ │
        │                                         │  │ │
        │  ┌──────────┐ ┌──────────┐ ┌──────────┐│  │ │
        │  │VANITY SW2│ │ MAIN SW2 │ │ FAN SW   ││  │ │
        │  │ T1◄──────┼─┼─────────▶┼─┼──┐      ││  │ │
        │  │ T2◄──────┼─┼───────┐  │ │  │ 120V ││  │ │
        │  │ COM ─────┼─┼────┐  │  │ │  ▼      ││  │ │
        │  └────┬─────┘ └──┬─┼──┘  │ │ ┌──────┐││  │ │
        │       │          │ │     │ │ │TO B6 │││  │ │
        │       │ Returns  │ │     │ │ │🌀 FAN│││  │ │
        │       │ to Box 2 │ │     │ │ │120V │││  │ │
        │       ▼          │ │     │ │ │ON   │││  │ │
        │   ┌─────────────┐│ │     │ │ └──────┘││  │ │
        │   │Return Path  ││ │     │ │          ││  │ │
        │   │120V Switch  ││ │     │ │          ││  │ │
        │   │Hot to Vanity││ │     │ │          ││  │ │
        │   └─────────────┘│ │     │ │          ││  │ │
        │                  │ │Returns to Box 4 ││  │ │
        │                  │ ▼                 ││  │ │
        │              ┌─────────────────┐     ││  │ │
        │              │Return Path      │     ││  │ │
        │              │120V Switch Hot  │     ││  │ │
        │              │to Main Light    │     ││  │ │
        │              └─────────────────┘     ││  │ │
        └─────────────────────────────────────────┘  │ │
                                                     │ │
        🔄 TRAVELER CONNECTIONS                      │ │
        Vanity Travelers: Box 2 ◄──14-3 Cable──────▶┘ │
        Main Travelers: Box 4 ◄────14-3 Cable────────▶┘
```

### **Power Flow Legend**
- **[+] Hot (120V)**: Active power conductor
- **(-) Neutral (0V)**: Return path conductor  
- **[G] Ground**: Safety/equipment grounding conductor
- **─── Solid Lines**: Power carrying conductors
- **┈┈┈ Dashed Lines**: Traveler signal wires
- **▶◀ Arrows**: Direction of power flow
- **[*] Light Symbols**: Fixtures receiving power
- **[~] Fan Symbol**: Exhaust fan receiving power

---

*These diagrams demonstrate that the linear feed-through design provides reliable, code-compliant power distribution with intuitive 3-way switch operation.*
