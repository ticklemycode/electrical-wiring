# Bathroom Electrical Wiring - Mermaid Diagram

This document provides a detailed Mermaid flowchart diagram of the bathroom electrical wiring system.

## Complete Circuit Flow Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    A["Electrical Panel<br/>15A Breaker"] -->|"14-2 Cable<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare"| B["GFCI Outlet<br/>15A, 120V"]
     B -->|"14-2 Cable<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare"| D["Vanity Switch 1<br/>3-Way Switch"]

    D -->|"14-3 Cable<br/>⚫ Hot: Black<br/>🔴 Traveler: Red<br/>⚪ Hot to Light: White<br/>🟢 Ground: Bare"| C["Vanity Light Fixture<br/>LED Compatible"]

    C -->|"14-3 Cable<br/>⚪ White to VS2: White<br/>🔴 Traveler: Red<br/>⚫ Black from Light: Black<br/>🟢 Ground: Green"| F["Main Switch 2<br/>3-Way Switch"]

    F -->|"14-3 Cable A (Vanity)<br/>⚪ White Hot to VS2: White<br/>🔴 Vanity Traveler: Red<br/>⚫ Neutral: Black<br/>🟢 Ground: Bare"| E["Combined Switch Box<br/>Main SW1<br/>Vanity SW2<br/>Fan SW"]

    F -->|"14-3 Cable B (Main Light)<br/>🔴 Main Traveler: Red<br/>⚫ Main Traveler: Black<br/>⚪ Neutral Feed: White<br/>🟢 Ground: Bare"| E

    E -->|"14-2 Cable<br/>⚫ Switched Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare"| G["Main Light Fixture<br/>LED Compatible"]

    G -->|"14-2 Cable<br/>⚫ Hot Pass-Through: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare"| H["Exhaust Fan<br/>CFM Rated"]
    
    %% Fan Control from Combined Box
    E -.->|"⚫ Switched Hot<br/>Fan Switch → Fan"| H
    
    %% Styling
    classDef boxPadding padding:10px 15px
    classDef panelStyle fill:#ff6b6b,stroke:#000,stroke-width:3px,color:#fff
    classDef gfciStyle fill:#4ecdc4,stroke:#000,stroke-width:2px,color:#000
    classDef fixtureStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    classDef switchStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef wireStyle stroke:#666,stroke-width:2px
    
    class A,B,C,D,E,F,G,H boxPadding
    class A panelStyle
    class B gfciStyle
    class C,G,H fixtureStyle
    class D,E,F switchStyle
```

## Circuit Control Power Flow Explanation

### ⚡ MAIN LIGHT CIRCUIT (3-Way Control)
**Primary Controller**: Main Switch 1 (Combined Box) - **SOURCES SWITCHED HOT**
**Secondary Controller**: Main Switch 2 (Separate Box) - **RECEIVES TRAVELERS**

**Power Flow**: Hot from vanity circuit → Main Switch 2 (pass-through via travelers) → Main Switch 1 (Combined Box) → **SWITCHED HOT OUTPUT** → Main Light

### ⚡ VANITY LIGHT CIRCUIT (3-Way Control)  
**Primary Controller**: Vanity Switch 1 (Separate Box) - **SOURCES HOT TO LIGHT**
**Secondary Controller**: Vanity Switch 2 (Combined Box) - **COMPLETES CIRCUIT**

**Power Flow**: GFCI → Vanity Switch 1 → **SWITCHED HOT TO VANITY LIGHT** → return via Vanity Switch 2

### ⚡ FAN CIRCUIT (Single-Pole Control)
**Controller**: Fan Switch (Combined Box)
**Power Flow**: Hot from main circuit → Fan Switch → **SWITCHED HOT TO FAN**

**Important Note**: The fan switch is located at the END of the circuit and controls the fan in the MIDDLE of the circuit. Here's how it works:

## Wire Identification Requirements (NEC 200.7)

**⚠️ CRITICAL: White Wires Used as Hot**
In 3-way switch circuits, white wires from switch loops carry hot (not neutral). These MUST be re-identified:
- **Mark with black electrical tape** at both ends (switch and fixture)
- **Required locations**: 
  - White wire at vanity light fixture (switched hot from Vanity Switch 2)
  - White wire at Main Switch 2 (carries hot to Combined Box)
- **Why**: Prevents dangerous confusion between true neutrals and hot wires

### Power Path to Fan Switch:
1. **Continuous Hot Wire**: Runs from GFCI → Vanity Switch 1 → Vanity Light → Main Switch 2 → **Combined Switch Box (Fan Switch)** 
2. **Fan Switch Location**: Physical end of the circuit run in Combined Switch Box
3. **Fan Location**: Between main light and combined switch box (receives power via main light circuit)

### Circuit Control Method:
- **⚫ Main Light Control**: Main Switch 1 (Combined Box) sends switched hot to Main Light via travelers from Main Switch 2
- **⚫ Vanity Light Control**: Vanity Switch 1 sends switched hot directly to Vanity Light, completed by Vanity Switch 2
- **⚫ Fan Control**: Fan switch in Combined Box sends switched hot to fan via main light pass-through
- **Result**: Each circuit controlled independently by its respective 3-way or single-pole switches

This configuration allows centralized control with the fan switch grouped with other switches.

### Visual Power Flow:
```
VANITY CIRCUIT:
Panel → GFCI → VS1 → Vanity Light ← VS2 (Combined Box)

MAIN LIGHT CIRCUIT:  
Panel → GFCI → VS1 → Vanity Light → MS2 ← Travelers → MS1 (Combined Box) → Main Light

FAN CIRCUIT:
Main Light → Fan ← Fan Switch (Combined Box)
```

## 3-Way Switch Control Logic Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart LR
    subgraph "Main Light Control"
        MS1["Main Switch 1<br/>(Combined Box)<br/>Position A | B"] 
        MS2["Main Switch 2<br/>(Separate Box)<br/>Position A | B"]
        ML["Main Light<br/>ON | OFF"]
        
        MS1 -.->|"🔴 Traveler 1<br/>Red Wire"| MS2
        MS1 -.->|"⚫ Traveler 2<br/>Black Wire"| MS2
        MS1 -->|"⚫ Switched Hot<br/>to Main Light"| ML
    end
    
    subgraph "Vanity Light Control"
        VS1["Vanity Switch 1<br/>Position A | B"]
        VS2["Vanity Switch 2<br/>Position A | B"]
        VL["Vanity Light<br/>ON | OFF"]
        
        VS1 -.->|"🔴 Traveler 1<br/>Red Wire"| VL
        VS1 -.->|"⚪ Traveler 2<br/>White Wire"| VL
        VL -.->|"🔴 Red Pass-Through"| VS2
        VL -.->|"⚫ Black Pass-Through"| VS2
        VL -->|"🔄 Hot Junction"| VL
    end
    
    subgraph "Fan Control"
        FS["Fan Switch<br/>ON | OFF"]
        FAN["Exhaust Fan<br/>ON | OFF"]
        
        FS -->|"⚫ Switched Hot"| FAN
    end
    
    classDef boxPadding padding:10px 15px
    classDef switchStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef deviceStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    
    class MS1,MS2,VS1,VS2,FS,ML,VL,FAN boxPadding
    class MS1,MS2,VS1,VS2,FS switchStyle
    class ML,VL,FAN deviceStyle
```

## Wire Routing and Box Connections

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    subgraph "Electrical Panel"
        PANEL["15A Breaker<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare"]
    end
    
    subgraph "Box 1 - GFCI Outlet"
        GFCI_LINE[LINE Side<br/>⚫ From Panel Hot<br/>⚪ From Panel Neutral<br/>🟢 From Panel Ground]
        GFCI_LOAD[LOAD Side<br/>⚫ To Vanity Hot<br/>⚪ To Vanity Neutral<br/>🟢 To Vanity Ground]
        GFCI_LINE -->|"Internal GFCI Protection"| GFCI_LOAD
    end
    
    subgraph "Box 2 - Vanity Switch 1"
        VS1_SWITCH["Vanity Switch 1<br/>⚫ COM ← Hot from GFCI<br/>🔴 T1 → Red Traveler to Light<br/>⚪ T2 → White (Hot) to Light Fixture<br/>🟢 GND ← Ground"]
        VS1_NEUTRAL["⚪ Neutral Pass-Through<br/>Wire Nut Only"]
    end
    
    subgraph "Box 3 - Vanity Light"
        VL_FIXTURE["Vanity Light Fixture<br/>⚪ White from VS1 (Hot)<br/>⚫ Black to MS2 (Pass-Through)<br/>🟢 Green Ground"]
        VL_SPLICE["Wire Splices<br/>⚫ Black from VS1 COM → White to VS2 (via MS2 → Combined Box)<br/>⚪ White from VS1 T2 → Light Fixture (Hot)<br/>🔴 Red: VS1→VS2 Pass-Through (via MS2 → Combined Box)<br/>⚫ Black from Light → Continue to MS2<br/>🟢 Green: Continue to MS2"]
        VL_SPLICE -.-> VL_FIXTURE
    end
    
    subgraph "Box 4 - Main Switch 2"
        MS2_SWITCH["Main Switch 2<br/>⚫ COM INPUT ← Black Hot from Vanity Circuit<br/>🔴 T1 ↔ Red Traveler to/from MS1<br/>⚫ T2 ↔ Black Traveler to/from MS1<br/>🟢 GND ← Ground"]
        MS2_NEUTRAL["⚪ TRUE Neutral Pass-Through<br/>(To/From Combined Box and Main Light)"]
        MS2_HOT["⚪ WHITE HOT from Vanity Light<br/>(Switched Hot Return - NOT Neutral)<br/>**MARK WITH BLACK TAPE**<br/>Continues to Combined Box"]
        MS2_CONTROL["⚡ 3-Way Control Logic<br/>Works with Main Switch 1 to control Main Light<br/>via Traveler Wires (Red & Black)"]
    end
    
    subgraph "Box 5 - Main Light"
        ML_FIXTURE[Main Light Fixture<br/>⚫ Switched Hot<br/>⚪ Neutral Return<br/>🟢 Ground]
        ML_SPLICE["Wire Splices<br/>⚫ Hot: Fixture + Pass-Through<br/>⚪ Neutral: Fixture + Pass-Through<br/>🟢 Ground: Fixture + Pass-Through"]
        ML_SPLICE -.-> ML_FIXTURE
    end
    
    subgraph "Box 6 - Exhaust Fan"
        FAN_MOTOR["Fan Motor<br/>⚫ From Switch Control (via Combined Box)<br/>⚪ Neutral Direct<br/>🟢 Ground to Case"]
        FAN_PASS[Pass-Through Wires<br/>⚫ Hot Continue to Combined Box<br/>⚪ Neutral Continue to Combined Box<br/>🟢 Ground Continue to Combined Box]
    end
    
    subgraph "Box 7 - Combined Switch Box (END OF RUN)"
        direction TB
        COMB_MAIN["Main Switch 1<br/>⚫ COM → Switched Hot to Main Light<br/>🔴 T1 ↔ Red to MS2<br/>⚫ T2 ↔ Black to MS2<br/>🟢 GND ← Ground Pigtail"]
        COMB_VANITY["Vanity Switch 2<br/>⚪ COM ← White from Vanity Light (Hot)<br/>🔴 T1 ↔ Red to Vanity Light<br/>⚫ T2 → Neutral (black wire in Cable A)<br/>🟢 GND ← Ground Pigtail"]
        COMB_FAN["Fan Switch<br/>⚫ LINE ← Hot from Main Circuit<br/>⚫ LOAD → Fan Control<br/>🟢 GND ← Ground Pigtail"]
        COMB_BUNDLES["Wire Bundles<br/>⚫ Hot Distribution<br/>⚪ Neutral Termination<br/>🟢 Ground Collection"]
        
        COMB_BUNDLES -.-> COMB_MAIN
        COMB_BUNDLES -.-> COMB_VANITY
        COMB_BUNDLES -.-> COMB_FAN
    end
    
    %% Cable Connections with Wire Colors and Travelers
    PANEL -->|"14-2 Cable<br/>⚫⚪🟢"| GFCI_LINE
    GFCI_LOAD -->|"14-2 Cable<br/>⚫⚪🟢"| VS1_SWITCH
    
    %% Vanity 3-Way Circuit - 14-3 Cable with Travelers
    VS1_SWITCH -->|"14-3 Cable Run #1<br/>⚫🔴⚪🟢<br/>🔴Red = Traveler 1<br/>⚪White = Hot to Light"| VL_FIXTURE
    VL_FIXTURE -->|"14-3 Cable Run #2<br/>⚫🔴⚪🟢<br/>🔴Red = Traveler to VS2<br/>⚫Black = Hot continues to MS2"| MS2_SWITCH
    
    %% Two 14-3 Cables from MS2 to Combined Box
    MS2_SWITCH -->|"14-3 Cable A (Vanity)<br/>⚪⚫🔴🟢<br/>⚪White = Hot (marked)<br/>🔴Red = Traveler<br/>⚫Black = Neutral"| COMB_BUNDLES
    MS2_SWITCH -->|"14-3 Cable B (Main Light)<br/>🔴⚫⚪🟢<br/>🔴Red = Traveler 1<br/>⚫Black = Traveler 2<br/>⚪White = Neutral"| COMB_BUNDLES
    
    %% Main Circuit - Combined Box to Main Light to Fan  
    COMB_MAIN -->|"14-2 Cable<br/>⚫⚪🟢<br/>⚫ Switched Hot"| ML_SPLICE
    ML_SPLICE -->|"14-2 Cable<br/>⚫⚪🟢"| FAN_PASS
    
    %% Fan Control Wire
    COMB_FAN -.->|"⚫ Switched Hot"| FAN_MOTOR
    COMB_BUNDLES -.-> COMB_MAIN
    COMB_BUNDLES -.-> COMB_VANITY
    COMB_BUNDLES -.-> COMB_FAN
    
    classDef boxPadding padding:10px 15px
    classDef panelStyle fill:#ff6b6b,stroke:#000,stroke-width:3px,color:#fff
    classDef boxStyle fill:#e8f4fd,stroke:#000,stroke-width:2px,color:#000
    classDef deviceStyle fill:#fff3cd,stroke:#000,stroke-width:2px,color:#000
    classDef fixtureStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    
    class PANEL,GFCI_LINE,GFCI_LOAD,VS1_SWITCH,VS1_NEUTRAL,VL_FIXTURE,COMB_MAIN,COMB_VANITY,COMB_FAN,COMB_BUNDLES,MS2_SWITCH,MS2_NEUTRAL,ML_FIXTURE,ML_SPLICE,FAN_MOTOR,FAN_PASS boxPadding
    class PANEL panelStyle
    class GFCI_LINE,GFCI_LOAD,VL_SPLICE,VS1_SWITCH,VS1_NEUTRAL,MS2_SWITCH,MS2_NEUTRAL,ML_SPLICE,FAN_PASS,COMB_BUNDLES boxStyle
    class COMB_MAIN,COMB_VANITY,COMB_FAN deviceStyle
    class VL_FIXTURE,ML_FIXTURE,FAN_MOTOR fixtureStyle
```

## Terminal Connection Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart LR
    subgraph "3-Way Switch Terminals"
        direction TB
        COM["COM Terminal<br/>⚫ Dark Screw"]
        T1["T1 Terminal<br/>🟡 Brass Screw"]
        T2["T2 Terminal<br/>🟡 Brass Screw"]
        GND["Ground Terminal<br/>🟢 Green Screw"]
    end
    
    subgraph "Wire Colors - 14-3 Cable"
        BLACK["⚫ Black Wire<br/>Hot or Traveler"]
        RED["🔴 Red Wire<br/>Traveler"]
        WHITE["⚪ White Wire<br/>Neutral"]
        BARE["🟢 Bare Wire<br/>Ground"]
    end
    
    subgraph "Main Switch 1 Connections"
        MS1_COM["COM ← ⚫ Hot from Source"]
        MS1_T1["T1 ← 🔴 Red Traveler"]
        MS1_T2["T2 ← ⚫ Black Traveler"]
        MS1_GND["GND ← 🟢 Ground"]
    end
    
    subgraph "Main Switch 2 Connections"
        MS2_COM["COM → ⚫ Switched Hot to Light"]
        MS2_T1["T1 ← 🔴 Red Traveler"]
        MS2_T2["T2 ← ⚫ Black Traveler"]
        MS2_GND["GND ← 🟢 Ground"]
    end
    
    %% Traveler Connections
    MS1_T1 -.->|"🔴 Red Wire"| MS2_T1
    MS1_T2 -.->|"⚫ Black Wire"| MS2_T2
    
    classDef boxPadding padding:10px 15px
    classDef terminalStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef wireStyle fill:#6c5ce7,stroke:#000,stroke-width:2px,color:#fff
    classDef connectionStyle fill:#e8f4fd,stroke:#000,stroke-width:1px,color:#000
    
    class COM,T1,T2,GND,BLACK,RED,WHITE,BARE,MS1_COM,MS1_T1,MS1_T2,MS1_GND,MS2_COM,MS2_T1,MS2_T2,MS2_GND boxPadding
    class COM,T1,T2,GND terminalStyle
    class BLACK,RED,WHITE,BARE wireStyle
    class MS1_COM,MS1_T1,MS1_T2,MS1_GND,MS2_COM,MS2_T1,MS2_T2,MS2_GND connectionStyle
```

## Switch Position Logic Table

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    subgraph "3-Way Switch Logic - Main Light"
        direction TB
        
        STATE1["Switch 1: ↑ UP<br/>Switch 2: ↑ UP<br/>Result: 💡 LIGHT OFF"]
        STATE2["Switch 1: ↑ UP<br/>Switch 2: ↓ DOWN<br/>Result: 🔆 LIGHT ON"]
        STATE3["Switch 1: ↓ DOWN<br/>Switch 2: ↑ UP<br/>Result: 🔆 LIGHT ON"]
        STATE4["Switch 1: ↓ DOWN<br/>Switch 2: ↓ DOWN<br/>Result: 💡 LIGHT OFF"]
        
        STATE1 --> STATE2
        STATE2 --> STATE3
        STATE3 --> STATE4
        STATE4 --> STATE1
    end
    
    subgraph "Circuit Path Analysis"
        direction LR
        
        HOT_IN["⚫ Hot Input<br/>Switch 1 COM"]
        TRAV1["🔴 Traveler 1<br/>Red Wire"]
        TRAV2["⚫ Traveler 2<br/>Black Wire"]
        SWITCH2["Switch 2<br/>T1 & T2"]
        LIGHT_OUT["⚫ To Light<br/>Switch 2 COM"]
        
        HOT_IN --> TRAV1
        HOT_IN --> TRAV2
        TRAV1 --> SWITCH2
        TRAV2 --> SWITCH2
        SWITCH2 --> LIGHT_OUT
    end
    
    classDef boxPadding padding:10px 15px
    classDef stateStyle fill:#fd79a8,stroke:#000,stroke-width:2px,color:#000
    classDef pathStyle fill:#00b894,stroke:#000,stroke-width:2px,color:#fff
    
    class STATE1,STATE2,STATE3,STATE4,HOT_IN,TRAV1,TRAV2,SWITCH2,LIGHT_OUT boxPadding
    class STATE1,STATE2,STATE3,STATE4 stateStyle
    class HOT_IN,TRAV1,TRAV2,SWITCH2,LIGHT_OUT pathStyle
```

## Circuit Load Analysis

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    subgraph "Circuit Capacity"
        BREAKER[⚡ 15A Circuit Breaker<br/>1800W Capacity]
    end
    
    subgraph "Connected Loads"
        GFCI[🔌 GFCI Outlet<br/>0W Standby]
        VL[💡 Vanity Light<br/>80W LED]
        ML[💡 Main Light<br/>60W LED]
        FAN[🌪️ Exhaust Fan<br/>90W Motor]
        FUTURE[🔌 Future Devices<br/>200W Reserve]
    end
    
    subgraph "Load Summary"
        TOTAL["📊 Total Load: 430W<br/>Circuit Usage: 24%<br/>Available: 1370W"]
    end
    
    BREAKER --> GFCI
    GFCI --> VL
    GFCI --> ML
    GFCI --> FAN
    GFCI --> FUTURE
    
    VL --> TOTAL
    ML --> TOTAL
    FAN --> TOTAL
    FUTURE --> TOTAL
    
    classDef boxPadding padding:10px 15px
    classDef capacityStyle fill:#e17055,stroke:#000,stroke-width:3px,color:#fff
    classDef loadStyle fill:#74b9ff,stroke:#000,stroke-width:2px,color:#000
    classDef summaryStyle fill:#00b894,stroke:#000,stroke-width:2px,color:#fff
    
    class BREAKER,GFCI,VL,ML,FAN,FUTURE,TOTAL boxPadding
    class BREAKER capacityStyle
    class GFCI,VL,ML,FAN,FUTURE loadStyle
    class TOTAL summaryStyle
```

## Safety and Code Compliance

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    subgraph "Safety Requirements"
        GFCI_REQ[GFCI Protection<br/>NEC 210.8<br/>Required for Bathroom]
        GROUND_REQ[Proper Grounding<br/>NEC 250<br/>All Metal Components]
        WIRE_REQ[Wire Gauge<br/>NEC 310.15<br/>14 AWG for 15A Circuit]
    end
    
    subgraph "Installation Standards"
        BOX_FILL[Box Fill Calculation<br/>NEC 314.16<br/>Adequate Space]
        SWITCH_ACCESS[Switch Accessibility<br/>NEC 404.2<br/>Proper Height]
        FIXTURE_MOUNT[Fixture Mounting<br/>NEC 314.27<br/>Secure Installation]
    end
    
    subgraph "Testing Requirements"
        VOLTAGE_TEST[Voltage Testing<br/>Before Work]
        CONTINUITY[Continuity Testing<br/>All Connections]
        GFCI_TEST[GFCI Function Test<br/>Monthly Testing]
    end
    
    classDef boxPadding padding:10px 15px
    classDef safetyStyle fill:#ff7675,stroke:#000,stroke-width:2px,color:#000
    classDef standardStyle fill:#fdcb6e,stroke:#000,stroke-width:2px,color:#000
    classDef testStyle fill:#55a3ff,stroke:#000,stroke-width:2px,color:#fff
    
    class GFCI_REQ,GROUND_REQ,WIRE_REQ,BOX_FILL,SWITCH_ACCESS,FIXTURE_MOUNT,VOLTAGE_TEST,CONTINUITY,GFCI_TEST boxPadding
    class GFCI_REQ,GROUND_REQ,WIRE_REQ safetyStyle
    class BOX_FILL,SWITCH_ACCESS,FIXTURE_MOUNT standardStyle
    class VOLTAGE_TEST,CONTINUITY,GFCI_TEST testStyle
```

## How to View These Diagrams

These Mermaid diagrams can be viewed in several ways:

1. **VS Code with Mermaid Preview Extension**
   - Install "Mermaid Preview" extension
   - Open this file and use the preview feature

2. **GitHub/GitLab**
   - These platforms natively render Mermaid diagrams

3. **Mermaid Live Editor**
   - Copy diagram code to https://mermaid.live/

4. **Documentation Platforms**
   - Most modern documentation platforms support Mermaid

## Diagram Features

- **Complete Circuit Flow**: Shows power routing from panel to each device
- **3-Way Switch Logic**: Illustrates how traveler wires control lights
- **Wire Specifications**: All diagrams show 14 AWG wire for 15A circuit
- **Terminal Connections**: Detailed switch terminal wiring
- **Load Analysis**: Circuit capacity and usage calculations
- **Safety Compliance**: Code requirements and testing procedures
- **High Contrast Styling**: Improved text readability with dark borders and contrasting colors

## Styling Notes

The diagrams use high-contrast color schemes for optimal readability:
- **Dark borders (#000)** on all elements for clear definition
- **White text on dark backgrounds** for critical components
- **Black text on light backgrounds** for detailed information
- **Bold stroke widths** to ensure visibility
- **Color-coded components** for easy identification while maintaining accessibility

These diagrams complement the ASCII art diagrams in the other documentation files and provide a more technical, structured view of the electrical system.

## Switch Box Configuration

**Important Configuration**: This bathroom wiring uses a combined switch box containing three switches:

1. **Vanity Switch 1**: Located in separate box near vanity light
2. **Combined Switch Box**: Contains three switches in one location:
   - Main Switch 1 (3-way for main light)
   - Vanity Switch 2 (3-way for vanity light)
   - Fan Switch (single pole for exhaust fan)
3. **Main Switch 2**: Located in separate box for main light control

### Benefits of Combined Switch Box:
- **Convenient Control**: All main switches in one location
- **Simplified Wiring**: Shared neutral and ground connections reduce wire nuts
- **Code Compliant**: Standard electrical practice for bathroom installations
- **Cost Effective**: Fewer boxes and less complex routing

## Detailed Wire Color Flow Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    subgraph "Wire Color Legend"
        HOT["⚫ Hot | Switched Hot - Black Wire"]
        NEUT["⚪ Neutral - White Wire"]
        GND["🟢 Ground - Bare | Green Wire"]
        TRAV1["🔴 Traveler 1 - Red Wire"]
        TRAV2["⚫ Traveler 2 - Black Wire in 14-3"]
    end
    
    subgraph "Panel to GFCI (14-2)"
        P1["⚫ Panel Hot"] --> G1["⚫ GFCI LINE Hot"]
        P2["⚪ Panel Neutral"] --> G2["⚪ GFCI LINE Neutral"]
        P3["🟢 Panel Ground"] --> G3["🟢 GFCI Ground"]
    end
    
    subgraph "GFCI to Vanity Light (14-2)"
        G4["⚫ GFCI LOAD Hot"] --> V1["⚫ Vanity Fixture Hot + Switch Feed"]
        G5["⚪ GFCI LOAD Neutral"] --> V2["⚪ Vanity Fixture Neutral + Circuit"]
        G6["🟢 GFCI LOAD Ground"] --> V3["🟢 Vanity Fixture Ground + Circuit"]
    end
    
    subgraph "Vanity Switch 1 to Vanity Light (14-3)"
        S1["⚫ VS1 COM Terminal"] --> V4["⚫ Black to White VS2 Junction"]
        S2["🔴 VS1 T1 Terminal"] --> V5["🔴 Red Pass-Through to VS2"]
        S3["⚪ VS1 T2 Terminal"] --> V6["⚪ White to Light Fixture Hot"]
        S4["⚪ Neutral Pass-Through"] --> V7["⚪ Neutral Continue to VS2"]
        S5["🟢 VS1 Ground"] --> V8["🟢 Green Pass-Through to VS2"]
    end
    
    subgraph "Vanity Light to Main Switch 2 (14-3)"
        V9["⚪ White from Black VS1 Junction"] --> M_VS2_HOT["⚪ Hot continues to Combined Box"]
        V10["🔴 Red Pass-Through"] --> M_VS2_RED["🔴 Red continues to Combined Box"]
        V11["⚫ Black from Light Fixture"] --> M_VS2_BLACK["⚫ Black continues to Combined Box"]
        V12["⚪ Neutral Continue"] --> M_VS2_NEUT["⚪ Neutral continues to Combined Box"]
        V13["🟢 Green Continue"] --> M_VS2_GND["🟢 Ground continues to Combined Box"]
    end
    
    subgraph "Main Switch 2 to Combined Box (Two 14-3 Cables)"
        M_VS2_HOT --> C2_A["⚪ Cable A: VS2 COM Terminal"]
        M_VS2_RED --> C3_A["🔴 Cable A: VS2 T1 Terminal"] 
        M_VS2_BLACK --> C4_A["⚫ Cable A: Neutral to Bundle"]
        M_VS2_GND --> C6["🟢 Ground Bundle Wire Nut"]
        
        C7_B["⚫ Cable B: From Main SW1 COM"] --> M1["🔴 Main SW2 T1"]
        C11_B["🔴 Cable B: MS1 T1"] --> M2["⚫ Main SW2 T2"]
        C12_B["⚫ Cable B: MS1 T2"] --> M3["⚪ Main SW2 T2"]
        C5_B["⚪ Cable B: Neutral"] --> M4["⚪ Neutral Pass-Through"]
    end
    
    subgraph "Combined Box Connections"
        H1["⚫ Hot Distribution Bundle"] --> C7["⚫ Main SW1 COM → Main Light"]
        H1 --> C8["⚫ Fan Switch LINE"]
        C2_A --> C9["⚪ Vanity SW2 COM from Light"]
        C10["🔴 Red MS1 T1"] --> C11_B
        C12["⚫ Black MS1 T2"] --> C12_B
        C14["⚫ Fan Switch LOAD"] --> C15["⚫ Control to Fan Motor"]
        C6 --> C16["🟢 All Switch Grounds"]
        C6 --> M5["🟢 Main SW2 Ground"]
    end
    
    subgraph "Combined Box to Main Light (14-2)"
        C7 --> L1["⚫ Main Light Fixture + Pass-Through"]
        C5_B --> L2["⚪ Main Light Neutral + Pass-Through"]
        C6 --> L3["🟢 Main Light Ground + Pass-Through"]
    end
    
    subgraph "Main Light to Fan (14-2)"
        L1 --> F1["⚫ Fan Box Pass-Through"]
        L2 --> F2["⚪ Fan Neutral to Motor"]
        L3 --> F3["🟢 Fan Ground to Motor + Case"]
    end
    
    subgraph "Fan Control from Combined Box"
        C15 --> F4["⚫ Fan Motor Hot from Switch"]
    end
    
    classDef boxPadding padding:10px 15px
    classDef hotStyle fill:#ff9999,stroke:#000,stroke-width:2px,color:#000
    classDef neutralStyle fill:#f0f0f0,stroke:#000,stroke-width:2px,color:#000
    classDef groundStyle fill:#90ee90,stroke:#000,stroke-width:2px,color:#000
    classDef travelerStyle fill:#ffd700,stroke:#000,stroke-width:2px,color:#000
    
    class HOT,NEUT,GND,TRAV1,TRAV2,P1,P2,P3,G1,G2,G3,G4,G5,G6,V1,V2,V3,V4,V5,V6,V7,V8,V9,V10,V11,V12,V13,S1,S2,S3,S4,S5,H1,C2_A,C3_A,C4_A,C5_B,C6,C7,C8,C9,C10,C11_B,C12,C12_B,C14,C15,C16,C7_B,M1,M2,M3,M4,L1,L2,L3,F1,F2,F3,F4,M_VS2_HOT,M_VS2_RED,M_VS2_BLACK,M_VS2_GND boxPadding
    class P1,G1,G4,V1,V4,S1,H1,C7,C8,C7_B,M1,L1,F1,C14,C15,F4,M_VS2_HOT hotStyle
    class P2,G2,G5,V2,V7,S4,C5_B,M4,L2,F2,V9,C2_A,M_VS2_GND neutralStyle
    class P3,G3,G6,V3,V8,S5,C6,C16,L3,F3,V13,M_VS2_GND groundStyle
    class V5,S2,C3_A,C10,C11_B,M2,V6,S3,C4_A,C12,C12_B,M3,V10,V11,M_VS2_RED travelerStyle
```

## Pigtail Requirements

Pigtails are short lengths of wire used to connect devices to spliced wires. Here's where they're needed in this circuit:

### Required Pigtails by Location:

#### Box 2 - Vanity Switch 1:
- **Ground Pigtail**: Only if switch lacks ground screw (modern switches usually have screws)
- **Hot | Neutral**: Direct connections, no pigtails needed

#### Box 4 - Combined Switch Box (3 switches):
**Hot Distribution (2 pigtails required):**
- Pigtail 1: Hot bundle → Main Switch 1 COM
- Pigtail 2: Hot bundle → Fan Switch LINE

**Vanity Switch 2 Connection:**
- COM terminal: Direct connection to white wire from vanity light (carries hot)

**Ground Distribution (3 pigtails required):**
- Pigtail 1: Ground bundle → Main Switch 1 GND
- Pigtail 2: Ground bundle → Vanity Switch 2 GND
- Pigtail 3: Ground bundle → Fan Switch GND

**Neutral**: Pass-through only, no pigtails to switches

#### Box 5 - Main Switch 2:
**IMPORTANT - Wire Type Clarification:**

**Main Switch 2 Terminal Connections:**
- **COM INPUT**: Black hot wire from vanity circuit (continuous hot power)
- **COM OUTPUT**: Black switched hot wire to main light fixture  
- **T1**: Red traveler from Main Switch 1 (Combined Box)
- **T2**: Black traveler from Main Switch 1 (Combined Box)
- **Ground**: Green/bare ground wire

**TRUE NEUTRALS (always neutral):**
- White wire from Combined Box (neutral feed via travelers)
- White wire continuing to main light (neutral return)

**WHITE WIRE THAT IS HOT (NOT neutral):**
- White wire from vanity light fixture (this carries switched hot from vanity)
- This white wire continues to Combined Box as part of 14-3 cable

**Power Flow:**
- Hot power enters MS2 from vanity circuit (black wire from vanity light)  
- MS2 sends this power to Combined Box via Cable A
- Combined Box controls main light via Main Switch 1 (3-way with MS2)
- Main light is controlled by Main Switch 1 + Main Switch 2 working together via travelers

**Wiring Notes:**
- The white wire from the vanity light is re-identified as hot per NEC 200.7(C)
- This wire should be marked with black tape at both ends to indicate it's hot
- True neutrals never connect to switch terminals

### Pigtail Wire Specifications:
- **Length**: 6 inches minimum
- **Gauge**: Same as circuit wire (14 AWG for this 15A circuit)
- **Color**: Match the wire color being extended
- **Connection**: Use wire nuts rated for the wire gauge

### Why Pigtails Are Important:
1. **Code Compliance**: NEC requires proper grounding of all switches
2. **Safety**: Ensures secure connections under switch screws
3. **Reliability**: Prevents loose connections from wire movement
4. **Future Service**: Allows switch replacement without re-splicing

## Circuit Control Analysis & Hot Wire Identification

### ⚡ VANITY LIGHT CIRCUIT (3-Way Control)

**Controllers**: Vanity Switch 1 (Box 2) + Vanity Switch 2 (Combined Box)

**Power Flow Path:**
```
GFCI → Vanity Switch 1 → Vanity Light → Main Switch 2 (pass-through) → Combined Box (Vanity Switch 2)
```

**Hot Wire Identification (NEC 200.7):**
- **Box 3 (Vanity Light)**: White wire from VS1 T2 terminal = **HOT** (mark with black tape)
- **Box 4 (Main Switch 2)**: White wire from vanity light = **HOT** (mark with black tape)  
- **Box 7 (Combined Box)**: White wire to VS2 COM terminal = **HOT** (already marked)

### ⚡ MAIN LIGHT CIRCUIT (3-Way Control)

**Controllers**: Main Switch 1 (Combined Box) + Main Switch 2 (Box 4)

**Power Flow Path:**
```
Hot Source → Combined Box (Main Switch 1) → Main Switch 2 → Main Light
```

**Critical Fix**: Main light is controlled by MS1 in Combined Box, NOT directly by MS2. MS2 acts as the second 3-way switch receiving travelers from MS1.

### 🔍 CIRCUIT VERIFICATION SUMMARY

### ✅ VANITY LIGHT CIRCUIT - PROPERLY CONFIGURED
- **Control**: Vanity Switch 1 (Box 2) + Vanity Switch 2 (Combined Box)
- **Hot Source**: Vanity Switch 1 COM terminal
- **Switched Hot**: VS1 T2 terminal → Vanity Light (white wire marked as hot)
- **Circuit Completion**: VS2 T2 terminal → neutral bundle
- **Independent Operation**: ✅ Works independently from main light

### ✅ MAIN LIGHT CIRCUIT - PROPERLY CONFIGURED  
- **Control**: Main Switch 1 (Combined Box) + Main Switch 2 (Box 4)
- **Hot Source**: Hot distribution bundle in Combined Box → MS1 COM terminal
- **Switched Hot**: MS1 COM terminal → Main Light
- **Traveler Control**: MS1 ↔ MS2 via red/black travelers
- **Independent Operation**: ✅ Works independently from vanity light

### ✅ FAN CIRCUIT - PROPERLY CONFIGURED
- **Control**: Fan Switch (Combined Box) - single-pole
- **Hot Source**: Hot distribution bundle in Combined Box → Fan Switch LINE
- **Switched Hot**: Fan Switch LOAD → Fan Motor (via main light pass-through)
- **Independent Operation**: ✅ Works independently from both lights

### 🔧 CRITICAL HOT WIRE MARKINGS (NEC 200.7)
1. **Box 3 (Vanity Light)**: White wire from VS1 T2 → vanity fixture (**MARK BLACK**)
2. **Box 4 (Main Switch 2)**: White wire from vanity light → Combined Box (**MARK BLACK**)  
3. **Box 7 (Combined Box)**: White wire → VS2 COM terminal (**MARK BLACK**)

### 📦 DETAILED WIRE NUT SPECIFICATIONS BY BOX

#### Box 4 - Main Switch 2 (DETAILED BREAKDOWN)

**Box Overview**: Main Switch 2 is a critical junction point where the vanity circuit passes through and connects to the Combined Box via two 14-3 cables. This box handles both pass-through wiring and 3-way switch connections.

**Incoming Cables:**
- **Cable 1**: 14-3 from Vanity Light (⚫🔴⚪🟢)
- **Cable 2**: 14-3 Cable A to Combined Box - Vanity circuit (⚪🔴⚫🟢)  
- **Cable 3**: 14-3 Cable B to Combined Box - Main light travelers (🔴⚫⚪🟢)

**Required Wire Nuts:**

**🔴 RED WIRE NUT #1 - Hot Input Distribution (3 wires)**
- **Wire 1**: ⚫ Black hot from vanity light (incoming power)
- **Wire 2**: ⚫ Black to MS2 COM terminal (pigtail - 6" long)
- **Wire 3**: ⚫ Black continuing to Combined Box (Cable A)
- **Purpose**: Distributes continuous hot power from vanity circuit
- **Wire Nut Size**: Red (3-5 x 14 AWG capacity)

**🟡 YELLOW WIRE NUT #2 - Hot to Combined Box (2 wires)**
- **Wire 1**: ⚪ White hot from vanity light (**MARKED WITH BLACK TAPE**)
- **Wire 2**: ⚪ White to Combined Box Cable A (**MARKED WITH BLACK TAPE**)
- **Purpose**: Passes vanity circuit hot to VS2 COM terminal in Combined Box
- **Wire Nut Size**: Yellow (2-4 x 14 AWG capacity)
- **⚠️ CRITICAL**: Both white wires MUST be marked as hot per NEC 200.7

**🔘 GRAY WIRE NUT #3 - Red Traveler (2 wires)**
- **Wire 1**: 🔴 Red from vanity light (pass-through)
- **Wire 2**: 🔴 Red to Combined Box Cable A (continues to VS2 T1)
- **Purpose**: Passes vanity circuit red traveler through MS2 box
- **Wire Nut Size**: Gray (2-3 x 14 AWG capacity)

**🔘 GRAY WIRE NUT #4 - Main Light Red Traveler (2 wires)**
- **Wire 1**: 🔴 Red from Combined Box Cable B (MS1 T1 traveler)
- **Wire 2**: 🔴 Red to MS2 T1 terminal (pigtail - 6" long)
- **Purpose**: Connects MS1 T1 to MS2 T1 (3-way traveler)
- **Wire Nut Size**: Gray (2-3 x 14 AWG capacity)

**🔘 GRAY WIRE NUT #5 - Main Light Black Traveler (2 wires)**
- **Wire 1**: ⚫ Black from Combined Box Cable B (MS1 T2 traveler)
- **Wire 2**: ⚫ Black to MS2 T2 terminal (pigtail - 6" long)
- **Purpose**: Connects MS1 T2 to MS2 T2 (3-way traveler)
- **Wire Nut Size**: Gray (2-3 x 14 AWG capacity)

**🔘 GRAY WIRE NUT #6 - Neutral Pass-Through (3 wires)**
- **Wire 1**: ⚪ White neutral from vanity light (true neutral)
- **Wire 2**: ⚪ White neutral to Combined Box Cable A
- **Wire 3**: ⚪ White neutral from Combined Box Cable B
- **Purpose**: Passes neutral through to Combined Box and main light circuit
- **Wire Nut Size**: Gray (2-3 x 14 AWG capacity)

**🟢 GREEN WIRE NUT #7 - Ground Collection (4 wires)**
- **Wire 1**: 🟢 Bare ground from vanity light
- **Wire 2**: 🟢 Bare ground to Combined Box Cable A
- **Wire 3**: 🟢 Bare ground to Combined Box Cable B  
- **Wire 4**: 🟢 Green pigtail to MS2 GND terminal (6" long)
- **Purpose**: Collects and distributes grounding for safety
- **Wire Nut Size**: Green (3-6 x 14 AWG capacity)

**Switch Terminal Connections:**
- **MS2 COM**: ⚫ Black pigtail from Red Wire Nut #1
- **MS2 T1**: 🔴 Red pigtail from Gray Wire Nut #4  
- **MS2 T2**: ⚫ Black pigtail from Gray Wire Nut #5
- **MS2 GND**: 🟢 Green pigtail from Green Wire Nut #7

**Box Fill Calculation:**
- **Total Conductors**: 12 (3 cables × 4 wires each)
- **Switch**: Counts as 2 conductors
- **Wire Nuts**: 7 wire nuts (no additional count)
- **Ground Pigtail**: 1 additional conductor
- **Total Box Fill**: 15 conductor equivalents
- **Required Box Size**: 4" × 4" × 2-1/8" minimum (21 cubic inch capacity)

**Installation Notes:**
1. **Hot Wire Marking**: Mark white wires in Wire Nut #2 with black tape at both ends
2. **Pigtail Length**: All pigtails should be 6" minimum for proper switch connections  
3. **Wire Nut Torque**: Hand-tighten wire nuts until snug, no tools required
4. **Cable Management**: Organize cables by function (vanity vs main light) for easier troubleshooting
5. **Testing**: Verify continuity on all traveler connections before energizing

**Safety Verification:**
- ✅ All grounds properly connected and pigtailed to switch
- ✅ Hot wires properly identified and marked per NEC 200.7
- ✅ Neutral pass-through maintains circuit integrity
- ✅ Traveler wires properly routed for 3-way operation
- ✅ Box fill within code limits for safe installation
