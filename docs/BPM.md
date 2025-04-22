---
Title: Block Diagram, Process Diagram, and Message Structure 
---
## Part 1: Team Block Diagram
<img src="https://raw.githubusercontent.com/EGR314-2025-S-311/T311.github.io/refs/heads/main/images/TeamBLOCK.png">

[Block Diagram Download](https://github.com/EGR314-2025-S-311/T311.github.io/blob/main/images/Team%20Block%20Diagram.pdf)

## Part 2: Sequence Diagram
<img width="468" alt="image" src="https://github.com/user-attachments/assets/06cad9ed-694c-4612-8d99-c81a206fdac9" />


## Part 3: Message Types

| Byte | Function |
|----|-------|
| AZ | Start |
| YB | Stop  |

| Team Members | Team IDs |
|--------------|----------|
| Shon Ha | h |
| Maximus Mathews | m |
| Shelton Larance | l |
| Rohan Fernandez | f |
| Broadcast | X |


| Message Type                              | Description                                                      |
| ----------------------------------------- | ---------------------------------------------------------------- |
| 1. Wifi Toggle - Auto/Manual              | 1 byte for toggling between Auto and Manual mode                 | 
| 2. Light Level                            | 24 Bytes (6 for each sensor with 2 as identifier and 4 as readings)                                      |
| 3. Button - Digital Signal                | 2 bytes for 2 buttons to control stepper motor          |

| Message Type 1 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 1 (char)                        | Mode (M)                                 |
| Bytes 2 (char)                        | Automatic or Manual - "0" or "1"                                 |

| Message Type 2 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 3-4 (char)                     | Light Level with a space - "L1"                                  |
| Bytes 5-8 (char)                         | Light Level Reading - "XXXX"                                     |
| Bytes 9-10 (char)                     | Light Level with a space - "L2"                                  |
| Bytes 11-14 (char)                         | Light Level Reading - "XXXX"                                     |
| Bytes 15-16 (char)                     | Light Level with a space - "L3"                                  |
| Bytes 17-20 (char)                         | Light Level Reading - "XXXX"                                     |
| Bytes 21-22 (char)                     | Light Level with a space - "L4"                                  |
| Bytes 23-26 (char)                         | Light Level Reading - "XXXX"                                     |


| Message Type44 Definitions                |                                                                  |
| ----------------------------------------- | ---------------------------------------------------------------- |
| Bytes 32 (char)  | button left (L) |
| Bytes 33 (char)                     | byte to control motor turning left          |
| Bytes 34 (char)  | button right (R) |
| Bytes 35 (char)  | byte to control motor turning right |

| **Message Type**          | **Message ID Type: Char** | **Rohan HMI ID: f**                        | **Maximus Sensor ID: m**          | **Shon Motor ID: h**                                             | **Shelton MQTT ID: l**                  |
|---------------------------|---------------------------|--------------------------------------------|-----------------------------------|------------------------------------------------------------------|-----------------------------------------|
| Mode Toggle               | M                         | R (activates button toggle to control motor) | -            | R (Sets motor into manual control using buttons)                 | S (mqtt topic: /EGR314/TEAM311/Mode)    |
| Light Levels              | S1-S4                     | -                                          | S (sends light data to motor)     | R (using data, turns motor in direction with highest light level) | -                                       |
| Button-Digital Signal     | L & R                     | S                                          | -            | R (manual control using buttons)                                 | -                          |



