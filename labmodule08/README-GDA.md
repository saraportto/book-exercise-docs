# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

**OPTION A CHOSEN**
The CoapServerGateway class was implemented to start a basic CoAP server capable of registering devices upon receiving POST requests.
This gateway was integrated into the DeviceDataManager, enabling the CoAP server to be started or stopped based on the enableCoapServer configuration flag, following the same pattern as the MQTT client.


Then, two new handlers, UpdateSystemPerformanceResourceHandler and UpdateTelemetryResourceHandler, were developed by extending GenericCoapResourceHandler. These handlers process PUT requests for SystemPerformanceData and SensorData, respectively.
An integration test class, UpdateResourceHandlerTest, was also added. It launches a CoAP server, registers the new handlers, and verifies through PUT requests that both SystemPerformanceData and SensorData are received and processed correctly.

The handleGET method was completed to validate the request context, log the incoming request, convert ActuatorData to JSON format, and return it as a CoAP response. This response includes both the resource name and the serialized actuator data.

Finally, support was added in DeviceDataManager to allow the registration and invocation of an IActuatorDataListener upon receiving actuator data.
In the CoapServerGateway, functionality was implemented to dynamically add CoAP resource handlers—both default and externally provided—by leveraging a hierarchical resource chain structure.



### CoAP Discovery: integration tests PIOT-GDA-08-002
Log output for the CoAP Discovery issued by the integration tests listed in either PIOT-CDA-08-002 or PIOT-GDA-08-002.


### CoAP GET: integration tests PIOT-CDA-08-003
Log output for the CoAP GET issued by the integration tests listed in either PIOT-CDA-08-003 or PIOT-GDA-08-003.

### Code Repository and Branch

URL: https://github.com/saraportto/java-components/tree/labmodule08


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
- UpdateResourceHandlerTest (fails)
- GetActuatorCommandResourceHandlerTest.java (fails)
- CoapServerGatewayTest


EOF.
