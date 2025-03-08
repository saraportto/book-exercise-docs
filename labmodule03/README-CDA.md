# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

This module implements several classes and methods for managing IoT device data, actuators and sensors. The BaseIot abstract class defines essential methods, including child classes like ActuatorData, SensorData, and SystemPerformanceData (with disk utilization tracking). It includes getters, setters, handleUpdateData, and a string representation method. The BaseSensorSimTask and BaseActuatorSimTask classes define initialization methods for sensor simulators (humidity, pressure and temperature) and actuator simulators (humidifier and HVAC). 

The SensorAdapterManager handles sensor emulation and data reading, while the ActuatorAdapterManager manages actuator simulators. The DeviceDataManager processes data, manages system requests, and monitors performance. However, _handleUpcomingDataAnalysis and _handleUpstreamTransmission were not implemented. Finally, a DeviceDataManager instance is created within the CDA class, where its start and stop methods are invoked.


### Code Repository and Branch

URL: https://github.com/saraportto/python-components/tree/labmodule03

### Unit Tests Executed

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py
- ActuatorDataTest.py
- SensorDataTest.py
- SystemPerformanceDataTest.py
- HumiditySensorSimTaskTest.py
- PressureSensorSimTaskTest.py
- TemperatureSensorSimTaskTest.py
- HumidifierActuatorSimTaskTest.py
- HvacActuatorSimTaskTest.py
- All unit tests in part02 (except for DataUtiltest.py, which fails)

### Integration Tests Executed

- ConstrainedDeviceAppTest.py
- SystemPerformanceManagerTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DeviceDataManagerNoCommsTest.py
- ConstrainedDeviceAppTest.py

EOF.
