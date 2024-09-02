# Drone Flight Control Module 

This Python module is designed to control drone flight operations. It provides a comprehensive set of functions for connecting to a drone, controlling its movement, and managing flight modes through the MAVLink protocol. This module is perfect for developers working on drone automation and control systems.

## Features 

- **Connect to the Drone:** Establish a connection to the drone using a specified connection string.
- **Flight Mode Management:** Set the drone to GUIDED mode for precise control.
- **Takeoff and Landing:** Automate the drone's takeoff to a specified altitude and handle landing procedures.
- **Directional Movement:** Command the drone to move forward, backward, left, and right.
- **Rotation Control:** Rotate the drone to a specific angle in a designated direction.
- **Arm/Disarm:** Safety features to arm or disarm the drone before and after flights.

## Requirements 

- Python 3.6 or higher
- pymavlink library
- A MAVLink-compatible drone (like those from the ArduPilot or PX4 series)

## Installation 🛠

To use this module, clone the repository and install the required Python package:

```bash
git clone https://github.com/yourusername/drone-control-module.git
cd drone-control-module
pip install pymavlink
```

## Usage 

### Connecting to the Drone

To start, connect to your drone using the connection string which is typically a serial port or a network address.

```python
connection = connect_to_drone('COM6')  # Adjust the connection string as needed
```

### Setting Drone to Guided Mode

Ensure the drone is in GUIDED mode to accept high-level commands:

```python
set_mode_guided(connection)
```

### Taking Off

Command the drone to take off to a specified altitude:

```python
takeoff_drone(connection, 5)  # Drone takes off to 5 meters altitude
```

### Moving the Drone

Move the drone in specific directions:

```python
move_forward(connection, 10)  # Move forward 10 meters
move_right(connection, 5)     # Move right 5 meters
```

### Landing the Drone

Finally, safely land the drone:

```python
land_drone(connection)
```

You can find a complete example under the `main()` function within the module, which demonstrates a sequence of operations from takeoff to landing.
