# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

Most of the methods in SensorData, ActuatorData, SystemPerformanceData, and SystemStateData have been implemented, including getters, setters, and the protected handleUpdateData method.

The SystemPerformanceManager class has been enhanced to collect system performance metrics, including CPU, memory, and disk utilization. For disk utilization, a separate SystemDiskUtilTask class was created. The collected data is then sent to a listener via the IDataMessageListener interface.

Additionally, methods in DataUtil have been implemented to convert objects (ActuatorData, SensorData, SystemPerformanceData) to and from JSON using Gson for serialization and deserialization.

The DeviceDataManager class initializes and manages system performance monitoring, handles incoming and outgoing data messages, and sets up communication connections for the IoT gateway.

The GatewayDeviceApp class now initializes DeviceDataManager, which manages device data and is instantiated during application startup. The execution flow also considers a configuration setting (ENABLE_RUN_FOREVER_KEY) to determine whether the application should run indefinitely or for a predefined duration. Additionally, the stopApp method has been modified to check if the application is running in a test environment, preventing System.exit(code) from terminating tests prematurely.

Optional tasks were not implemented.

### Code Repository and Branch

URL: https://github.com/saraportto/java-components/tree/labmodule05


### Unit Tests Executed

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- SystemStateDataTest
- DataUtilTest


### Integration Tests Executed

- GatewayDeviceAppTest
- SystemPerformanceManagerTest
- DataIntegrationTest
- DeviceDataManagerNoCommsTest

EOF.
