---
Title: Block Diagram, Process Diagram, and Message Structure 
---
## Part 1: Team Block Diagram
<img src="https://raw.githubusercontent.com/EGR314-2025-S-311/T311.github.io/refs/heads/main/images/TeamBLOCK.png">

[Block Diagram Download](https://github.com/EGR314-2025-S-311/T311.github.io/blob/main/images/Team%20Block%20Diagram.pdf)

## Part 2: Sequence Diagram
<img width="468" alt="image" src="https://github.com/user-attachments/assets/06cad9ed-694c-4612-8d99-c81a206fdac9" />


## Part 3: Message Types

| Message Type                              | Description                                                      |
| ----------------------------------------- | ---------------------------------------------------------------- |
| 1. Wifi Toggle - Auto/Manual              | 1 byte for toggling between Auto and Manual mode                 | 
| 2. Light Level                            | 24 Bytes (6 for each sensor with 2 as identifier and 4 as readings)                                      |
| 3. Voltage Sensor                         | 5 bytes  (1 for identifier and 4 as readings)                                                     |
| 4. Button - Digital Signal                | 2 bytes for 2 buttons to control stepper motor          |
| 5. Unique Identifier                      | 4 bytes for identifing the message to be our team's              | 

| Message Type 1 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 1 (uint8_t)                        | Automatic or Manual - "0" or "1"                                 |

| Message Type 2 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 2-3 (char)                     | Light Level with a space - "L1"                                  |
| Bytes 4-8 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 9-10 (char)                     | Light Level with a space - "L2"                                  |
| Bytes 11-14 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 15-16 (char)                     | Light Level with a space - "L3"                                  |
| Bytes 17-20 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 21-22 (char)                     | Light Level with a space - "L4"                                  |
| Bytes 23-26 (float)                         | Light Level Reading - "XXXX"                                     |

| Message Type 3 Definitions |                      |
|----------------------------|----------------------|
| Bytes 27-28 (char)                       | Voltage with a space " V"                                        |
| Bytes 29-32 (float)                       | Voltage Level Reading  " X.X"                                    |

| Message Type 4 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 33 (uint8_t)                     | byte to control motor turning left          |
| Bytes 34 (uint8_t)  | byte to control motor turning right |

| Message Type 4 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 35-38 (char)                      | Unique Identifier - "TEAM311"                                   |
