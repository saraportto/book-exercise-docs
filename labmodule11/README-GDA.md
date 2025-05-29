# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

MqttClientConnector was adapted to use reusable protected methods for publishing, subscribing, and unsubscribing from topics. Compatibility with the asynchronous client (MqttAsyncClient).


The CloudClientConnector class was implemented to fulfill the ICloudClient interface for sending data to the cloud (sensor and performance). Within DeviceDataManager, the use of Mosquitto/MQTT was replaced by this cloud client, activated via configuration.

The GDA was connected to the cloud service and subscribed to the LED-events topic (gda/led) in CloudClientConnector upon establishing the connection.

A MessageListener was implemented to receive actuator events, convert them into ActuatorData, and forward them to the CDA.

DeviceDataManager was updated to process that ActuatorData and publish it to the CDA via MQTT to activate the LED.


### Code Repository and Branch

URL: URL: https://github.com/saraportto/java-components/tree/labmodule11


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
