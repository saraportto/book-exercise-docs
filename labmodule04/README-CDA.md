# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

This module implements the methods from the sensor emulation module (humidity, pressure, and temperature), inheriting from BaseSensorSimTask. Each class retrieves data from the corresponding sensor and stores it in SensorData for further processing.

Additionally, HumidifierEmulatorTask, HvacEmulatorTask, and LedDisplayEmulatorTask (which derive from BaseActuatorSimTask and emulate actuators) manage the activation and deactivation of the actuator by displaying messages on the SenseHAT LED display in emulator mode.

The SenseHAT emulator functionality was also added to the SensorAdapterManager class, allowing dynamic loading of temperature, humidity, and pressure sensor emulators when the configuration enables it. Furthermore, if no emulators are used, _initEnvironmentalSensorTasks is called. Finally, it processes commands for actuators based on their type and location, updating the corresponding actuator if it matches locationID.


### Code Repository and Branch

URL: https://github.com/saraportto/python-components/tree/labmodule04


### Unit Tests Executed

- 
- 
- 

### Integration Tests Executed

- 
- 
- 

EOF.
