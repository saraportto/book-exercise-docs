# Constrained Device Application (Connected Devices)

## Lab Module 09

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

**OPTION A CHOSEN**
The initialization of the CoAP client using aiocoap was implemented, along with its configuration through ConfigUtil and the base structure for all connector methods.
Full support for CRUD operations (GET, PUT, POST, and DELETE) was developed, including asynchronous payload transmission, response handling, and resource discovery.
Additionally, observation functionality was added with startObserver and stopObserver, enabling automatic updates from CoAP server resources to be received.

### Code Repository and Branch

URL: https://github.com/saraportto/python-components/tree/labmodule09


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
- CoapClientConnectorTest.py

EOF.
