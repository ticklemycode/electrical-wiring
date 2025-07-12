# Bathroom Electrical Wiring - Mermaid Diagram

This document provides a detailed Mermaid flowchart diagram of the bathroom electrical wiring system.

## Complete Circuit Flow Diagram

```mermaid
flowchart TD
    A[Electrical Panel<br/>15A Breaker] -->|14-2 w/Ground<br/>Hot, Neutral, Ground| B[GFCI Outlet<br/>15A, 120V]
    
    B -->|14-2 w/Ground<br/>Hot, Neutral, Ground| C[Vanity Light Fixture<br/>LED Compatible]
    
    C -->|14-3 w/Ground<br/>Hot, Red Traveler, Black Traveler, Neutral, Ground| D[Vanity Switch 1<br/>3-Way Switch]
    
    D -->|14-3 w/Ground<br/>Hot, Red Traveler, Black Traveler, Neutral, Ground| E[Main Switch 1<br/>3-Way Switch]
    
    E -->|14-3 w/Ground<br/>Switched Hot, Red Traveler, Black Traveler, Neutral, Ground| F[Main Light Fixture<br/>LED Compatible]
    
    F -->|14-2 w/Ground<br/>Hot, Neutral, Ground| G[Exhaust Fan<br/>CFM Rated]
    
    G -->|14-3 w/Ground<br/>Hot, Red Traveler, Black Traveler, Neutral, Ground| H[Main Switch 2<br/>3-Way Switch]
    
    H -->|14-3 w/Ground<br/>Red Traveler, Black Traveler, Neutral, Ground| I[Vanity Switch 2<br/>3-Way Switch]
    
    I -->|14-2 w/Ground<br/>Hot, Neutral, Ground| J[Fan Switch<br/>Single Pole]
    
    %% 3-Way Control Connections
    D -.->|Traveler Wires<br/>Control Signal| I
    E -.->|Traveler Wires<br/>Control Signal| H
    
    %% Fan Control
    J -.->|Switched Hot<br/>Control Wire| G
    
    %% Styling
    classDef panelStyle fill:#ff6b6b,stroke:#000,stroke-width:3px,color:#fff
    classDef gfciStyle fill:#4ecdc4,stroke:#000,stroke-width:2px,color:#000
    classDef fixtureStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    classDef switchStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef wireStyle stroke:#666,stroke-width:2px
    
    class A panelStyle
    class B gfciStyle
    class C,F,G fixtureStyle
    class D,E,H,I,J switchStyle
```

## 3-Way Switch Control Logic Diagram

```mermaid
flowchart LR
    subgraph "Main Light Control"
        MS1[Main Switch 1<br/>Position A/B] 
        MS2[Main Switch 2<br/>Position A/B]
        ML[Main Light<br/>ON/OFF]
        
        MS1 -.->|Traveler 1<br/>Red Wire| MS2
        MS1 -.->|Traveler 2<br/>Black Wire| MS2
        MS2 -->|Switched Hot| ML
    end
    
    subgraph "Vanity Light Control"
        VS1[Vanity Switch 1<br/>Position A/B]
        VS2[Vanity Switch 2<br/>Position A/B]
        VL[Vanity Light<br/>ON/OFF]
        
        VS1 -.->|Traveler 1<br/>Red Wire| VS2
        VS1 -.->|Traveler 2<br/>Black Wire| VS2
        VS2 -->|Switched Hot| VL
    end
    
    subgraph "Fan Control"
        FS[Fan Switch<br/>ON/OFF]
        FAN[Exhaust Fan<br/>ON/OFF]
        
        FS -->|Switched Hot| FAN
    end
    
    classDef switchStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef deviceStyle fill:#45b7d1,stroke:#000,stroke-width:2px,color:#fff
    
    class MS1,MS2,VS1,VS2,FS switchStyle
    class ML,VL,FAN deviceStyle
```

## Wire Routing and Box Connections

```mermaid
flowchart TD
    subgraph "Electrical Panel"
        PANEL[15A Breaker<br/>Hot: Black<br/>Neutral: White<br/>Ground: Bare]
    end
    
    subgraph "Box 1 - GFCI Outlet"
        GFCI_LINE[LINE Side<br/>From Panel]
        GFCI_LOAD[LOAD Side<br/>To Downstream]
        GFCI_LINE --> GFCI_LOAD
    end
    
    subgraph "Box 2 - Vanity Light"
        VL_HOT[Hot Connection]
        VL_NEUTRAL[Neutral Connection]
        VL_GROUND[Ground Connection]
        VL_HOT --> VL_NEUTRAL
    end
    
    subgraph "Box 3 - Switch Box 1"
        SW1_VS[Vanity Switch 1<br/>COM, T1, T2, GND]
        SW1_MS[Main Switch 1<br/>COM, T1, T2, GND]
    end
    
    subgraph "Box 4 - Main Light"
        ML_SWITCH[Switched Hot]
        ML_NEUTRAL[Neutral]
        ML_GROUND[Ground]
        ML_SWITCH --> ML_NEUTRAL
    end
    
    subgraph "Box 5 - Exhaust Fan"
        FAN_HOT[Hot Pass-Through]
        FAN_NEUTRAL[Neutral]
        FAN_GROUND[Ground]
        FAN_SWITCH_HOT[From Fan Switch]
        FAN_SWITCH_HOT --> FAN_HOT
    end
    
    subgraph "Box 6 - Switch Box 2"
        SW2_MS[Main Switch 2<br/>COM, T1, T2, GND]
        SW2_VS[Vanity Switch 2<br/>COM, T1, T2, GND]
        SW2_FS[Fan Switch<br/>Hot, Load, GND]
    end
    
    %% Wire Connections
    PANEL -->|14-2| GFCI_LINE
    GFCI_LOAD -->|14-2| VL_HOT
    VL_HOT -->|14-3| SW1_VS
    SW1_VS -->|14-3| SW1_MS
    SW1_MS -->|14-3| ML_SWITCH
    ML_SWITCH -->|14-2| FAN_HOT
    FAN_HOT -->|14-3| SW2_MS
    SW2_MS -->|14-3| SW2_VS
    SW2_VS -->|14-2| SW2_FS
    
    %% Traveler Connections
    SW1_VS -.->|Travelers| SW2_VS
    SW1_MS -.->|Travelers| SW2_MS
    SW2_FS -.->|Control| FAN_SWITCH_HOT
    
    classDef panelStyle fill:#ff6b6b,stroke:#000,stroke-width:3px,color:#fff
    classDef boxStyle fill:#e8f4fd,stroke:#000,stroke-width:2px,color:#000
    classDef deviceStyle fill:#fff3cd,stroke:#000,stroke-width:1px,color:#000
    
    class PANEL panelStyle
    class GFCI_LINE,GFCI_LOAD,VL_HOT,VL_NEUTRAL,VL_GROUND,ML_SWITCH,ML_NEUTRAL,ML_GROUND,FAN_HOT,FAN_NEUTRAL,FAN_GROUND,FAN_SWITCH_HOT boxStyle
    class SW1_VS,SW1_MS,SW2_MS,SW2_VS,SW2_FS deviceStyle
```

## Terminal Connection Diagram

```mermaid
flowchart LR
    subgraph "3-Way Switch Terminals"
        direction TB
        COM[COM Terminal<br/>Dark Screw]
        T1[T1 Terminal<br/>Brass Screw]
        T2[T2 Terminal<br/>Brass Screw]
        GND[Ground Terminal<br/>Green Screw]
    end
    
    subgraph "Wire Colors - 14-3 Cable"
        BLACK[Black Wire<br/>Hot or Traveler]
        RED[Red Wire<br/>Traveler]
        WHITE[White Wire<br/>Neutral]
        BARE[Bare Wire<br/>Ground]
    end
    
    subgraph "Main Switch 1 Connections"
        MS1_COM[COM ← Hot from Source]
        MS1_T1[T1 ← Red Traveler]
        MS1_T2[T2 ← Black Traveler]
        MS1_GND[GND ← Ground]
    end
    
    subgraph "Main Switch 2 Connections"
        MS2_COM[COM → Switched Hot to Light]
        MS2_T1[T1 ← Red Traveler]
        MS2_T2[T2 ← Black Traveler]
        MS2_GND[GND ← Ground]
    end
    
    %% Traveler Connections
    MS1_T1 -.->|Red Wire| MS2_T1
    MS1_T2 -.->|Black Wire| MS2_T2
    
    classDef terminalStyle fill:#f9ca24,stroke:#000,stroke-width:2px,color:#000
    classDef wireStyle fill:#6c5ce7,stroke:#000,stroke-width:2px,color:#fff
    classDef connectionStyle fill:#e8f4fd,stroke:#000,stroke-width:1px,color:#000
    
    class COM,T1,T2,GND terminalStyle
    class BLACK,RED,WHITE,BARE wireStyle
    class MS1_COM,MS1_T1,MS1_T2,MS1_GND,MS2_COM,MS2_T1,MS2_T2,MS2_GND connectionStyle
```

## Switch Position Logic Table

```mermaid
flowchart TD
    subgraph "3-Way Switch Logic - Main Light"
        direction TB
        
        STATE1[Switch 1: UP<br/>Switch 2: UP<br/>Result: LIGHT OFF]
        STATE2[Switch 1: UP<br/>Switch 2: DOWN<br/>Result: LIGHT ON]
        STATE3[Switch 1: DOWN<br/>Switch 2: UP<br/>Result: LIGHT ON]
        STATE4[Switch 1: DOWN<br/>Switch 2: DOWN<br/>Result: LIGHT OFF]
        
        STATE1 --> STATE2
        STATE2 --> STATE3
        STATE3 --> STATE4
        STATE4 --> STATE1
    end
    
    subgraph "Circuit Path Analysis"
        direction LR
        
        HOT_IN[Hot Input<br/>Switch 1 COM]
        TRAV1[Traveler 1<br/>Red Wire]
        TRAV2[Traveler 2<br/>Black Wire]
        SWITCH2[Switch 2<br/>T1 & T2]
        LIGHT_OUT[To Light<br/>Switch 2 COM]
        
        HOT_IN --> TRAV1
        HOT_IN --> TRAV2
        TRAV1 --> SWITCH2
        TRAV2 --> SWITCH2
        SWITCH2 --> LIGHT_OUT
    end
    
    classDef stateStyle fill:#fd79a8,stroke:#000,stroke-width:2px,color:#000
    classDef pathStyle fill:#00b894,stroke:#000,stroke-width:2px,color:#fff
    
    class STATE1,STATE2,STATE3,STATE4 stateStyle
    class HOT_IN,TRAV1,TRAV2,SWITCH2,LIGHT_OUT pathStyle
```

## Circuit Load Analysis

```mermaid
flowchart TD
    subgraph "Circuit Capacity"
        BREAKER[15A Circuit Breaker<br/>1800W Capacity]
    end
    
    subgraph "Connected Loads"
        GFCI[GFCI Outlet<br/>0W Standby]
        VL[Vanity Light<br/>80W LED]
        ML[Main Light<br/>60W LED]
        FAN[Exhaust Fan<br/>90W Motor]
        FUTURE[Future Devices<br/>200W Reserve]
    end
    
    subgraph "Load Summary"
        TOTAL[Total Load: 430W<br/>Circuit Usage: 24%<br/>Available: 1370W]
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
    
    classDef capacityStyle fill:#e17055,stroke:#000,stroke-width:3px,color:#fff
    classDef loadStyle fill:#74b9ff,stroke:#000,stroke-width:2px,color:#000
    classDef summaryStyle fill:#00b894,stroke:#000,stroke-width:2px,color:#fff
    
    class BREAKER capacityStyle
    class GFCI,VL,ML,FAN,FUTURE loadStyle
    class TOTAL summaryStyle
```

## Safety and Code Compliance

```mermaid
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
    
    classDef safetyStyle fill:#ff7675,stroke:#000,stroke-width:2px,color:#000
    classDef standardStyle fill:#fdcb6e,stroke:#000,stroke-width:2px,color:#000
    classDef testStyle fill:#55a3ff,stroke:#000,stroke-width:2px,color:#fff
    
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
