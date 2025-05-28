# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

MqttClientConnector was updated to support authentication (username/password) and secure connections (TLS) using certificates, with all settings made configurable via the properties file.

Automatic subscriptions to the CDA topics (SensorData, SystemPerformanceData, and ActuatorDataResponse) were added directly within the connectComplete() method, using Option 1 (a single callback handler).

In DeviceDataManager, duplicate subscription logic was removed from startManager() to delegate subscription handling entirely to MqttClientConnector.

Finally, logic was implemented on the GDA side to analyze humidity data received from the CDA. If values are detected to be outside the defined thresholds for a certain period, an actuator command (ON/OFF) is generated and sent to the CDA. In addition, sensor information is logged and transmitted for upstream processing or storage.


### Code Repository and Branch

URL: https://github.com/saraportto/java-components/tree/labmodule10



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
- MqttClientConnectorTest
- MqttClientControlPacketTest
- UpdateResourceHandlerTest
- GetActuatorCommandResourceHandlerTest
- CoapServerGatewayTest
- DeviceDataManagerSimpleCdaActuationTest

EOF.
