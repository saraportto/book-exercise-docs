# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

The MqttClientConnector class (which implements the IPubSubClient and MqttCallbackExtended interfaces) was initialized by setting up MQTT connection parameters such as host, port, keep-alive interval, and client ID using values from the configuration file. It prepares the client for connecting to the MQTT broker. 

Methods to establish a connection to the MQTT broker and disconnect the client from it were implemented, as well as methods to publish messages to specific topics, subscribe and unsubscribe from topics, and handle MQTT callbacks for connection events, message arrival, and message delivery.

The last step involves integrating an MqttClientConnector into the DeviceDataManager class, enabling MQTT client functionality by conditionally creating and managing the connection, subscriptions, and disconnections based on configuration flags.


### Code Repository and Branch

URL: https://github.com/saraportto/java-components/tree/labmodule07


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


EOF.
