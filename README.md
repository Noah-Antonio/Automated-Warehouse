# Automated Warehouse
PLC-based automated warehouse system using state-based sequential ladder logic to control pallet loading, storage, retrieval, and unloading. Features strong interlocking, Start/Stop, Emergency Stop, Reset functionality, and flexible mode switching during operation.


## Overview
This project is a PLC-based automated warehouse control system featuring a vertical 6×9 warehouse with 54 storage locations and a motorized fork crane for automated pallet handling. The system uses state-based sequential ladder logic to manage pallet loading, storage, retrieval, and unloading. The loading sequence consists of Loading, Receiving, Transporting, Storing, and Returning states, while unloading uses Retrieving, ReturningUnload, and Unloading states. ReadyToStart and ReadyToStop states manage operation transitions, with ReadyToStop allowing the current loading or unloading sequence to finish before the machine stops.

A strong interlocking system prevents conflicting operations and ensures proper sequencing. Start, Stop, Emergency Stop, and Reset controls are incorporated into the system. An Emergency Stop immediately stops the machine, with operation requiring the pallet to be manually removed before restarting. The system also supports mode switching during operation while maintaining the required state and safety conditions.


## Features
- **State-Based Sequential Control** – Dedicated states for loading, receiving, transporting, storing, returning, retrieving, unloading, and controlled start/stop transitions.
- **Pallet Handling** – Automated loading, storage, retrieval, and unloading using a motorized fork crane.
- **Interlocking System** – Prevents conflicting machine operations and ensures safe state transitions.
- **Ready-to-Stop Functionality** – Allows an active loading or unloading sequence to finish before stopping.
- **Emergency Stop** – Immediately stops machine operation and requires manual pallet removal before restarting.
- **Start/Stop & Reset Controls** – Provides controlled operator interaction with the system.
- **Mode Switching** – Allows operating modes to be changed during operation while maintaining safety and sequence conditions.


## Technologies

- **CODESYS**
- **Factory I/O**
- **Modbus TCP/IP Communication**
- **IEC 61131-3 Ladder Diagram (LD)**


## Engineering Concepts Demonstrated

- PLC Programming
- Sequential State-Based Control
- Ladder Logic Development
- Automated Material Handling
- Machine State Management
- Process Interlocking
- Safety Interlocks
- Start/Stop Control
- Emergency Stop & Reset Logic
- Controlled Stop Sequences
- Mode Management
- Fault & Recovery Handling
- Automated Pallet Storage & Retrieval
- Machine Sequence Testing & Validation



## I/O List

### Digital Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX4.0 | At_Entry_Sensor | Retroreflective Sensor | Detects when a pallet reaches the entry conveyor |
| %IX4.1 | At_Load_Sensor | Retroreflective Sensor | Detects when a pallet reaches the end of the load conveyor |
| %IX4.2 | At_Left_Sensor | Sensor | Detects when the crane forks are in the leftmost position |
| %IX4.3 | At_Middle_Sensor | Sensor | Detects when the crane forks are in the middle position |
| %IX4.4 | At_Right_Sensor | Sensor | Detects when the crane forks are in the rightmost position |
| %IX4.5 | At_Unload_Sensor | Retroreflective Sensor | Detects when a pallet reaches the unload conveyor |
| %IX4.6 | At_Exit_Sensor | Retroreflective Sensor | Detects when a pallet reaches the end of the exit conveyor |
| %IX4.7 | Moving_X | Sensor | Indicates that the crane is moving along the X-axis |
| %IX5.0 | Moving_Z | Sensor | Indicates that the crane is moving along the Z-axis |
| %IX5.1 | Start | White Pushbutton | Commands the system to start operation |
| %IX5.2 | Reset | Blue Pushbutton | Resets the system following an emergency stop |
| %IX5.3 | Stop | Gray Pushbutton | Commands the system to stop after the current loading or unloading sequence is completed |
| %IX5.4 | Emergency_Stop | Emergency Stop Button | Immediately halts system operation |
| %IX5.5 | Mode_Unload | Selector | Selects between loading and unloading operating modes |

### Digital Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX4.0 | Entry_Conveyor_CMD | Roller Conveyor | Commands the entry conveyor to operate |
| %QX4.1 | Load_Conveyor_CMD | Loading Conveyor | Commands the load conveyor to operate |
| %QX4.2 | Forks_Left_CMD | Crane Forks | Commands the crane forks to extend to the left |
| %QX4.3 | Forks_Right_CMD | Crane Forks | Commands the crane forks to extend to the right |
| %QX4.4 | Lift_CMD | Stacker Crane | Commands the crane forks to raise or lower |
| %QX4.5 | Unload_Conveyor_CMD | Unloading Conveyor | Commands the unload conveyor to operate |
| %QX4.6 | Exit_Conveyor_CMD | Roller Conveyor | Commands the exit conveyor to operate |
| %QX4.7 | Start_Status_Light | White Light Indicator | Indicates that the system has been commanded to start |
| %QX5.0 | Reset_Status_Light | Blue Light Indicator | Indicates that the system has been reset |
| %QX5.1 | Stop_Status_Light | Gray Light Indicator | Indicates that the system has been commanded to stop |

### Register Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Target_Position | Stacker Crane | Specifies the target warehouse position for the crane |


## Demonstration

