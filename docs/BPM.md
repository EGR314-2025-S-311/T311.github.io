---
Title: Block Diagram, Process Diagram, and Message Structure 
---
## Part 1: Team Block Diagram
<img src="https://raw.githubusercontent.com/EGR314-2025-S-311/T311.github.io/refs/heads/main/images/TeamBLOCK.png">

[Block Diagram Download](https://github.com/EGR314-2025-S-311/T311.github.io/blob/main/images/Team%20Block%20Diagram.pdf)

## Part 2: Sequence Diagram
<img src="https://github.com/EGR314-2025-S-311/T311.github.io/blob/main/images/_Sequence%20Diagram%20.drawio.png?raw=true">

## Part 3: Message Types

| Message Type                              | Description                                                      |
| ----------------------------------------- | ---------------------------------------------------------------- |
| 1. Wifi Toggle - Auto/Manual              | 1 byte for toggling between Auto and Manual mode                 | 
| 2. Light Level and Voltage                | 13 Bytes                                                         |
| 3. Button - Digital Signal                | 1 byte for all 4 buttons (each has 2 bits for 0 and 1)           |
| 4. Unique Identifier                      | 4 bytes for identifing the message to be our team's              | 

| Message Type 1 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 1 (uint8_t)                        | Automatic or Manual - "A" or "M"                                 |

| Message Type 2 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 2-3 (uint8_t)                     | Light Level with a space - "L1"                                  |
| Bytes 4-8 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 9-10 (uint8_t)                     | Light Level with a space - "L2"                                  |
| Bytes 11-14 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 15-16 (uint8_t)                     | Light Level with a space - "L3"                                  |
| Bytes 17-20 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 21-22 (uint8_t)                     | Light Level with a space - "L4"                                  |
| Bytes 23-26 (float)                         | Light Level Reading - "XXXX"                                     |
| Bytes 27-28 (uint8_t)                       | Voltage with a space " V"                                        |
| Bytes 29-32 (float)                       | Voltage Level Reading  " X.X"                                    |

| Message Type 3 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 33 (uint8_t)                     | Space with a byte with data of the all Button readings           |

| Message Type 4 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 34-37 (uint8_t)                      | Unique Identifier - "TEAM311"                                   |
