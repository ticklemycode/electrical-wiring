# Bathroom Electrical Wiring - Mermaid Diagram

This document provides a detailed Mermaid flowchart diagram of the bathroom electrical wiring system.

## Complete Circuit Flow Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart TD
    A&#91;Electrical Panel<br/>15A Breaker&#93; -->|14-2 Cable<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| B&#91;GFCI Outlet<br/>15A, 120V&#93;
     B -->|14-2 Cable<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| D&#91;Vanity Switch 1<br/>3-Way Switch&#93;

    D -->|14-2 Cable<br/>⚫ Switched Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| C&#91;Vanity Light Fixture<br/>LED Compatible&#93;

    D -->|14-3 Cable<br/>⚫ Hot: Black<br/>🔴 Traveler: Red<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| E&#91;Combined Switch Box<br/>Main SW1<br/>Vanity SW2<br/>Fan SW&#93;

    E -->|14-3 Cable<br/>⚫ Switched Hot: Black<br/>🔴 Traveler: Red<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| F&#91;Main Switch 2<br/>3-Way Switch&#93;

    F -->|14-2 Cable<br/>⚫ Switched Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| G&#91;Main Light Fixture<br/>LED Compatible&#93;

    G -->|14-2 Cable<br/>⚫ Hot Pass-Through: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| H&#91;Exhaust Fan<br/>CFM Rated&#93;
    
    H -->|14-2 Cable<br/>⚫ Hot Continuous: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare| E
    
    %% Fan Control Wire
    E -.->|⚫ Switched Hot<br/>Fan Switch → Fan| H
    
    %% 3-Way Traveler Wires - 14-3 Cable Note
    D -.->|14-3 Cable:<br/>🔴 Red: VS1↔VS2<br/>⚫ Black: VS1↔VS2| E
    E -.->|14-3 Cable:<br/>🔴 Red: MS1↔MS2<br/>⚫ Black: MS1↔MS2| F
    
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

## Fan Control Power Flow Explanation

**Important Note**: The fan switch is located at the END of the circuit but controls the fan in the MIDDLE of the circuit. Here's how it works:

### Power Path to Fan Switch:
1. **Continuous Hot Wire**: Runs from GFCI → Vanity Light → Switch Box 1 → Main Light → **Fan (passes through)** → Switch Box 2 → Fan Switch
2. **Fan Switch Location**: Physical end of the circuit run  
3. **Fan Location**: Middle of the circuit (between main light and switch box 2)

### Fan Control Method:
- **⚫ Hot Wire**: Continues past the fan to reach the fan switch
- **⚫ Switched Hot**: Fan switch sends control signal BACK to fan via separate wire
- **Result**: Fan switch can turn fan ON | OFF even though it's downstream

This is a common electrical configuration where the switch controlling a device is not physically adjacent to that device.

### Visual Flow:
```
Panel → GFCI → VS1 → Vanity Light → Combined Box → MS2 → Main Light → Fan → Combined Box
                                                                      ↑        ↓
                                                                  Pass-Through  Control Wire
                                                                      ↑        ↓  
                                                                 Fan Switch ←──┘
```

## 3-Way Switch Control Logic Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart LR
    subgraph "Main Light Control"
        MS1&#91;Main Switch 1<br/>Position A | B&#93; 
        MS2&#91;Main Switch 2<br/>Position A | B&#93;
        ML&#91;Main Light<br/>ON | OFF&#93;
        
        MS1 -.->|🔴 Traveler 1<br/>Red Wire| MS2
        MS1 -.->|⚫ Traveler 2<br/>Black Wire| MS2
        MS2 -->|⚫ Switched Hot| ML
    end
    
    subgraph "Vanity Light Control"
        VS1&#91;Vanity Switch 1<br/>Position A | B&#93;
        VS2&#91;Vanity Switch 2<br/>Position A | B&#93;
        VL&#91;Vanity Light<br/>ON | OFF&#93;
        
        VS1 -.->|🔴 Traveler 1<br/>Red Wire| VS2
        VS1 -.->|⚫ Traveler 2<br/>Black Wire| VS2
        VS2 -->|⚫ Switched Hot| VL
    end
    
    subgraph "Fan Control"
        FS&#91;Fan Switch<br/>ON | OFF&#93;
        FAN&#91;Exhaust Fan<br/>ON | OFF&#93;
        
        FS -->|⚫ Switched Hot| FAN
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
        PANEL&#91;15A Breaker<br/>⚫ Hot: Black<br/>⚪ Neutral: White<br/>🟢 Ground: Bare&#93;
    end
    
    subgraph "Box 1 - GFCI Outlet"
        GFCI_LINE&#91;LINE Side<br/>⚫ From Panel Hot<br/>⚪ From Panel Neutral<br/>🟢 From Panel Ground&#93;
        GFCI_LOAD&#91;LOAD Side<br/>⚫ To Vanity Hot<br/>⚪ To Vanity Neutral<br/>🟢 To Vanity Ground&#93;
        GFCI_LINE -->|Internal GFCI Protection| GFCI_LOAD
    end
    
    subgraph "Box 2 - Vanity Switch 1"
        VS1_SWITCH&#91;Vanity Switch 1<br/>⚫ COM ← Hot from GFCI<br/>🔴 T1 → Red Traveler<br/>⚫ T2 → Black Traveler<br/>🟢 GND ← Ground&#93;
        VS1_NEUTRAL&#91;⚪ Neutral Pass-Through<br/>Wire Nut Only&#93;
    end
    
    subgraph "Box 3 - Vanity Light"
        VL_FIXTURE&#91;Vanity Light Fixture<br/>⚫ Switched Hot from VS1<br/>⚪ Neutral Return<br/>🟢 Ground&#93;
    end
    
    subgraph "Box 4 - Combined Switch Box"
        direction TB
        COMB_MAIN&#91;Main Switch 1<br/>⚫ COM ← Hot Pigtail<br/>🔴 T1 ↔ Red to MS2<br/>⚫ T2 ↔ Black to MS2<br/>🟢 GND ← Ground Pigtail&#93;
        COMB_VANITY&#91;Vanity Switch 2<br/>⚫ COM ← Hot Pigtail<br/>🔴 T1 ↔ Red from VS1<br/>⚫ T2 ↔ Black from VS1<br/>🟢 GND ← Ground Pigtail&#93;
        COMB_FAN&#91;Fan Switch<br/>⚫ LINE ← Hot Pigtail<br/>⚫ LOAD → Fan Control<br/>🟢 GND ← Ground Pigtail&#93;
        COMB_BUNDLES&#91;Wire Bundles<br/>⚫ Hot Distribution<br/>⚪ Neutral Pass-Through<br/>🟢 Ground Collection&#93;
        
        COMB_BUNDLES -.-> COMB_MAIN
        COMB_BUNDLES -.-> COMB_VANITY
        COMB_BUNDLES -.-> COMB_FAN
    end
    
    subgraph "Box 5 - Main Switch 2"
        MS2_SWITCH&#91;Main Switch 2<br/>⚫ COM → Switched Hot<br/>🔴 T1 ← Red from MS1<br/>⚫ T2 ← Black from MS1<br/>🟢 GND ← Ground&#93;
        MS2_NEUTRAL&#91;⚪ Neutral Pass-Through<br/>Wire Nut Only&#93;
    end
    
    subgraph "Box 6 - Main Light"
        ML_FIXTURE&#91;Main Light Fixture<br/>⚫ Switched Hot<br/>⚪ Neutral Return<br/>🟢 Ground&#93;
        ML_SPLICE&#91;Wire Splices<br/>⚫ Hot: Fixture + Pass-Through<br/>⚪ Neutral: Fixture + Pass-Through<br/>🟢 Ground: Fixture + Pass-Through&#93;
        ML_SPLICE -.-> ML_FIXTURE
    end
    
    subgraph "Box 7 - Exhaust Fan"
        FAN_MOTOR&#91;Fan Motor<br/>⚫ From Switch Control<br/>⚪ Neutral Direct<br/>🟢 Ground to Case&#93;
        FAN_PASS&#91;Pass-Through Wires<br/>⚫ Hot Continue<br/>⚪ Neutral Continue<br/>🟢 Ground Continue&#93;
    end
    
    %% Cable Connections with Wire Colors
    PANEL -->|14-2 Cable<br/>⚫⚪🟢| GFCI_LINE
    GFCI_LOAD -->|14-2 Cable<br/>⚫⚪🟢| VS1_SWITCH
    VS1_SWITCH -->|14-2 Cable<br/>⚫⚪🟢| VL_FIXTURE
    VS1_SWITCH -->|14-3 Cable<br/>⚫🔴⚪🟢| COMB_BUNDLES
    COMB_BUNDLES -->|14-3 Cable<br/>⚫🔴⚪🟢| MS2_SWITCH
    MS2_SWITCH -->|14-2 Cable<br/>⚫⚪🟢| ML_SPLICE
    ML_SPLICE -->|14-2 Cable<br/>⚫⚪🟢| FAN_PASS
    FAN_PASS -->|14-2 Cable<br/>⚫⚪🟢| COMB_BUNDLES
    
    %% Control Wires
    COMB_FAN -.->|⚫ Switched Hot| FAN_MOTOR
    
    %% Traveler Connections
    VS1_SWITCH -.->|🔴⚫ Travelers| COMB_VANITY
    COMB_MAIN -.->|🔴⚫ Travelers| MS2_SWITCH
    
    classDef boxPadding padding:10px 15px
    classDef panelStyle fill:#ff6b6b,stroke:#000,stroke-width:3px,color:#fff
    classDef boxStyle fill:#e8f4fd,stroke:#000,stroke-width:2px,color:#000
    classDef deviceStyle fill:#fff3cd,stroke:#000,stroke-width:2px,color:#000
    classDef fixtureStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    
    class PANEL,GFCI_LINE,GFCI_LOAD,VS1_SWITCH,VS1_NEUTRAL,VL_FIXTURE,COMB_MAIN,COMB_VANITY,COMB_FAN,COMB_BUNDLES,MS2_SWITCH,MS2_NEUTRAL,ML_FIXTURE,ML_SPLICE,FAN_MOTOR,FAN_PASS boxPadding
    class PANEL panelStyle
    class GFCI_LINE,GFCI_LOAD,VL_SPLICE,VS1_SWITCH,VS1_NEUTRAL,COMB_BUNDLES,MS2_SWITCH,MS2_NEUTRAL,ML_SPLICE,FAN_PASS boxStyle
    class COMB_MAIN,COMB_VANITY,COMB_FAN deviceStyle
    class VL_FIXTURE,ML_FIXTURE,FAN_MOTOR fixtureStyle
```

## Terminal Connection Diagram

```mermaid
%%{init: {'theme':'default', 'flowchart': {'nodeSpacing': 60, 'rankSpacing': 80, 'padding': 20}, 'themeVariables': {'primaryColor': '#ffffff', 'primaryTextColor': '#000000', 'primaryBorderColor': '#000000', 'lineColor': '#666666', 'sectionBkgColor': '#ffffff', 'altSectionBkgColor': '#f9f9f9', 'gridColor': '#cccccc', 'c0': '#ffffff', 'c1': '#ffffff', 'c2': '#ffffff', 'c3': '#ffffff', 'c4': '#ffffff'}}}%%
flowchart LR
    subgraph "3-Way Switch Terminals"
        direction TB
        COM&#91;COM Terminal<br/>⚫ Dark Screw&#93;
        T1&#91;T1 Terminal<br/>🟡 Brass Screw&#93;
        T2&#91;T2 Terminal<br/>🟡 Brass Screw&#93;
        GND&#91;Ground Terminal<br/>🟢 Green Screw&#93;
    end
    
    subgraph "Wire Colors - 14-3 Cable"
        BLACK&#91;⚫ Black Wire<br/>Hot or Traveler&#93;
        RED&#91;🔴 Red Wire<br/>Traveler&#93;
        WHITE&#91;⚪ White Wire<br/>Neutral&#93;
        BARE&#91;🟢 Bare Wire<br/>Ground&#93;
    end
    
    subgraph "Main Switch 1 Connections"
        MS1_COM&#91;COM ← ⚫ Hot from Source&#93;
        MS1_T1&#91;T1 ← 🔴 Red Traveler&#93;
        MS1_T2&#91;T2 ← ⚫ Black Traveler&#93;
        MS1_GND&#91;GND ← 🟢 Ground&#93;
    end
    
    subgraph "Main Switch 2 Connections"
        MS2_COM&#91;COM → ⚫ Switched Hot to Light&#93;
        MS2_T1&#91;T1 ← 🔴 Red Traveler&#93;
        MS2_T2&#91;T2 ← ⚫ Black Traveler&#93;
        MS2_GND&#91;GND ← 🟢 Ground&#93;
    end
    
    %% Traveler Connections
    MS1_T1 -.->|🔴 Red Wire| MS2_T1
    MS1_T2 -.->|⚫ Black Wire| MS2_T2
    
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
        
        STATE1&#91;Switch 1: ↑ UP<br/>Switch 2: ↑ UP<br/>Result: 💡 LIGHT OFF&#93;
        STATE2&#91;Switch 1: ↑ UP<br/>Switch 2: ↓ DOWN<br/>Result: 🔆 LIGHT ON&#93;
        STATE3&#91;Switch 1: ↓ DOWN<br/>Switch 2: ↑ UP<br/>Result: 🔆 LIGHT ON&#93;
        STATE4&#91;Switch 1: ↓ DOWN<br/>Switch 2: ↓ DOWN<br/>Result: 💡 LIGHT OFF&#93;
        
        STATE1 --> STATE2
        STATE2 --> STATE3
        STATE3 --> STATE4
        STATE4 --> STATE1
    end
    
    subgraph "Circuit Path Analysis"
        direction LR
        
        HOT_IN&#91;⚫ Hot Input<br/>Switch 1 COM&#93;
        TRAV1&#91;🔴 Traveler 1<br/>Red Wire&#93;
        TRAV2&#91;⚫ Traveler 2<br/>Black Wire&#93;
        SWITCH2&#91;Switch 2<br/>T1 & T2&#93;
        LIGHT_OUT&#91;⚫ To Light<br/>Switch 2 COM&#93;
        
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
        BREAKER&#91;⚡ 15A Circuit Breaker<br/>1800W Capacity&#93;
    end
    
    subgraph "Connected Loads"
        GFCI&#91;🔌 GFCI Outlet<br/>0W Standby&#93;
        VL&#91;💡 Vanity Light<br/>80W LED&#93;
        ML&#91;💡 Main Light<br/>60W LED&#93;
        FAN&#91;🌪️ Exhaust Fan<br/>90W Motor&#93;
        FUTURE&#91;🔌 Future Devices<br/>200W Reserve&#93;
    end
    
    subgraph "Load Summary"
        TOTAL&#91;📊 Total Load: 430W<br/>Circuit Usage: 24%<br/>Available: 1370W&#93;
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
        GFCI_REQ&#91;GFCI Protection<br/>NEC 210.8<br/>Required for Bathroom&#93;
        GROUND_REQ&#91;Proper Grounding<br/>NEC 250<br/>All Metal Components&#93;
        WIRE_REQ&#91;Wire Gauge<br/>NEC 310.15<br/>14 AWG for 15A Circuit&#93;
    end
    
    subgraph "Installation Standards"
        BOX_FILL&#91;Box Fill Calculation<br/>NEC 314.16<br/>Adequate Space&#93;
        SWITCH_ACCESS&#91;Switch Accessibility<br/>NEC 404.2<br/>Proper Height&#93;
        FIXTURE_MOUNT&#91;Fixture Mounting<br/>NEC 314.27<br/>Secure Installation&#93;
    end
    
    subgraph "Testing Requirements"
        VOLTAGE_TEST&#91;Voltage Testing<br/>Before Work&#93;
        CONTINUITY&#91;Continuity Testing<br/>All Connections&#93;
        GFCI_TEST&#91;GFCI Function Test<br/>Monthly Testing&#93;
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
        ⚫HOT&#91;⚫ Hot | Switched Hot - Black Wire&#93;
        ⚪NEUT&#91;⚪ Neutral - White Wire&#93;
        🟢GND&#91;🟢 Ground - Bare | Green Wire&#93;
        🔴TRAV1&#91;🔴 Traveler 1 - Red Wire&#93;
        ⚫TRAV2&#91;⚫ Traveler 2 - Black Wire in 14-3&#93;
    end
    
    subgraph "Panel to GFCI (14-2)"
        P1&#91;⚫ Panel Hot&#93; --> G1&#91;⚫ GFCI LINE Hot&#93;
        P2&#91;⚪ Panel Neutral&#93; --> G2&#91;⚪ GFCI LINE Neutral&#93;
        P3&#91;🟢 Panel Ground&#93; --> G3&#91;🟢 GFCI Ground&#93;
    end
    
    subgraph "GFCI to Vanity Light (14-2)"
        G4&#91;⚫ GFCI LOAD Hot&#93; --> V1&#91;⚫ Vanity Fixture Hot + Switch Feed&#93;
        G5&#91;⚪ GFCI LOAD Neutral&#93; --> V2&#91;⚪ Vanity Fixture Neutral + Circuit&#93;
        G6&#91;🟢 GFCI LOAD Ground&#93; --> V3&#91;🟢 Vanity Fixture Ground + Circuit&#93;
    end
    
    subgraph "Vanity Light to Switch 1 (14-3)"
        V4&#91;⚫ Hot from Fixture&#93; --> S1&#91;⚫ VS1 COM Terminal&#93;
        V5&#91;🔴 Red Traveler&#93; --> S2&#91;🔴 VS1 T1 Terminal&#93;
        V6&#91;⚫ Black Traveler&#93; --> S3&#91;⚫ VS1 T2 Terminal&#93;
        V7&#91;⚪ Neutral Pass-Through&#93; --> S4&#91;⚪ Wire Nut Only&#93;
        V8&#91;🟢 Ground&#93; --> S5&#91;🟢 VS1 Ground + Wire Nut&#93;
    end
    
    subgraph "Switch 1 to Combined Box (14-3)"
        S6&#91;⚫ Hot Continuation&#93; --> C1&#91;⚫ Hot Distribution to 3 Switches&#93;
        S7&#91;🔴 Red from VS1 T1&#93; --> C2&#91;🔴 VS2 T1 Terminal&#93;
        S8&#91;⚫ Black from VS1 T2&#93; --> C3&#91;⚫ VS2 T2 Terminal&#93;
        S9&#91;⚪ Neutral Pass-Through&#93; --> C4&#91;⚪ Neutral Bundle Wire Nut&#93;
        S10&#91;🟢 Ground&#93; --> C5&#91;🟢 Ground Bundle Wire Nut&#93;
    end
    
    subgraph "Combined Box Connections"
        C1 --> C6&#91;⚫ Main SW1 COM&#93;
        C1 --> C7&#91;⚫ Vanity SW2 COM&#93;
        C1 --> C8&#91;⚫ Fan Switch LINE&#93;
        C9&#91;🔴 Red MS1 T1&#93; --> C10&#91;🔴 To Main SW2 T1&#93;
        C11&#91;⚫ Black MS1 T2&#93; --> C12&#91;⚫ To Main SW2 T2&#93;
        C13&#91;⚫ Fan Switch LOAD&#93; --> C14&#91;⚫ Control to Fan Motor&#93;
        C5 --> C15&#91;🟢 All Switch Grounds&#93;
    end
    
    subgraph "Combined Box to Main Switch 2 (14-3)"
        C16&#91;⚫ From Main SW1 COM&#93; --> M1&#91;⚫ Main SW2 COM&#93;
        C10 --> M2&#91;🔴 Main SW2 T1&#93;
        C12 --> M3&#91;⚫ Main SW2 T2&#93;
        C4 --> M4&#91;⚪ Neutral Pass-Through&#93;
        C5 --> M5&#91;🟢 Main SW2 Ground&#93;
    end
    
    subgraph "Main Switch 2 to Main Light (14-2)"
        M6&#91;⚫ Main SW2 COM Output&#93; --> L1&#91;⚫ Main Light Fixture + Pass-Through&#93;
        M4 --> L2&#91;⚪ Main Light Neutral + Pass-Through&#93;
        M5 --> L3&#91;🟢 Main Light Ground + Pass-Through&#93;
    end
    
    subgraph "Main Light to Fan (14-2)"
        L4&#91;⚫ Hot Pass-Through&#93; --> F1&#91;⚫ Fan Box Pass-Through&#93;
        L2 --> F2&#91;⚪ Fan Neutral to Motor&#93;
        L3 --> F3&#91;🟢 Fan Ground to Motor + Case&#93;
    end
    
    subgraph "Fan Control from Combined Box"
        C14 --> F4&#91;⚫ Fan Motor Hot from Switch&#93;
    end
    
    classDef boxPadding padding:10px 15px
    classDef hotStyle fill:#ff9999,stroke:#000,stroke-width:2px,color:#000
    classDef neutralStyle fill:#f0f0f0,stroke:#000,stroke-width:2px,color:#000
    classDef groundStyle fill:#90ee90,stroke:#000,stroke-width:2px,color:#000
    classDef travelerStyle fill:#ffd700,stroke:#000,stroke-width:2px,color:#000
    
    class ⚫HOT,⚪NEUT,🟢GND,🔴TRAV1,⚫TRAV2,P1,P2,P3,G1,G2,G3,G4,G5,G6,V1,V2,V3,V4,V5,V6,V7,V8,S1,S2,S3,S4,S5,S6,S7,S8,S9,S10,C1,C2,C3,C4,C5,C6,C7,C8,C9,C10,C11,C12,C13,C14,C15,C16,M1,M2,M3,M4,M5,M6,L1,L2,L3,L4,F1,F2,F3,F4 boxPadding
    class P1,G1,G4,V1,V4,S1,S6,C1,C6,C7,C8,C16,M1,M6,L1,L4,F1,C13,C14,F4 hotStyle
    class P2,G2,G5,V2,V7,S4,S9,C4,M4,L2,F2 neutralStyle
    class P3,G3,G6,V3,V8,S5,S10,C5,C15,M5,L3,F3 groundStyle
    class V5,S2,S7,C2,C9,C10,M2,V6,S3,S8,C3,C11,C12,M3 travelerStyle
```

## Pigtail Requirements

Pigtails are short lengths of wire used to connect devices to spliced wires. Here's where they're needed in this circuit:

### Required Pigtails by Location:

#### Box 2 - Vanity Switch 1:
- **Ground Pigtail**: Only if switch lacks ground screw (modern switches usually have screws)
- **Hot | Neutral**: Direct connections, no pigtails needed

#### Box 4 - Combined Switch Box (3 switches):
**Hot Distribution (3 pigtails required):**
- Pigtail 1: Hot bundle → Main Switch 1 COM
- Pigtail 2: Hot bundle → Vanity Switch 2 COM  
- Pigtail 3: Hot bundle → Fan Switch LINE

**Ground Distribution (3 pigtails required):**
- Pigtail 1: Ground bundle → Main Switch 1 GND
- Pigtail 2: Ground bundle → Vanity Switch 2 GND
- Pigtail 3: Ground bundle → Fan Switch GND

**Neutral**: Pass-through only, no pigtails to switches

#### Box 5 - Main Switch 2:
- **Ground Pigtail**: Only if switch lacks ground screw
- **Hot | Neutral**: Direct connections, no pigtails needed

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
