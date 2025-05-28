# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

The reception of ActuatorData commands from the GDA was enabled in the CDA by integrating them into DeviceDataManager and the IDataMessageListener interface.

Logic was added to allow MqttClientConnector to process these commands and forward them accordingly.

Tests were implemented and executed to validate the MQTT subscription and command processing from the CDA.

Data transmission from the CDA to the GDA was implemented using both MQTT and CoAP protocols, including sensor messages, system performance metrics, and actuator responses. Additionally, local actuation logic based on temperature was integrated, enabling HVAC activation according to defined thresholds.

### Code Repository and Branch

URL: https://github.com/saraportto/python-components/tree/labmodule10


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
- MqttClientControlPacketTest.py (fails)
- CoapClientConnectorTest.py

EOF.
