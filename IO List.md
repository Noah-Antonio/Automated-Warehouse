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
