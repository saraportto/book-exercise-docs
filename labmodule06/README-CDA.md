# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

The MQTT Client Connector implements the IPubSubClient interface to manage communication with the MQTT broker. It uses default configuration settings to establish connection parameters and handles key events such as connection, disconnection, publishing, and subscribing.

The implementation enables bidirectional MQTT communication for the device, managing connections, subscriptions, and data transmission automatically based on the configuration.


### Code Repository and Branch

URL: https://github.com/saraportto/python-components/tree/labmodule06

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
- All unit tests in part02
- 

### Integration Tests Executed

- ConstrainedDeviceAppTest.py
- SystemPerformanceManagerTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DeviceDataManagerNoCommsTest.py
- SenseHatEmulatorQuickTest.py
- HumidityEmulatorTaskTest.py
- PressureEmulatorTaskTest.py
- TemperatureEmulatorTaskTest.py
- HumidifierEmulatorTaskTest.py
- HvacEmulatorTaskTest.py
- LedDisplayEmulatorTaskTest.py
- SensorEmulatorManagerTest.py
- ActuatorEmulatorManagerTest.py
- DataIntegrationTest.py
- MqttClientConnectorTest.py

EOF.
