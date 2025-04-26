# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

The MQTT Client Connector implements the IPubSubClient interface to manage communication with the MQTT broker. It uses default configuration settings to establish connection parameters and handles key events such as connection, disconnection, publishing, and subscribing.

The implementation enables bidirectional MQTT communication for the device, managing connections, subscriptions, and data transmission automatically based on the configuration.

### MQTT Control Packets Captured in Wireshark

| Control Packet        | Specific Line                                                    | Description                                |
|------------------------|------------------------------------------------------------------|--------------------------------------------|
| **CONNECT**            | 4 0.000198 ::1 ::1 MQTT 90 Connect Command                      | Connect Command                            |
| **CONNACK**            | 7 0.002916 ::1 ::1 MQTT 80 Connect Ack                           | Connect Acknowledge                        |
| **SUBSCRIBE**          | 9 0.003001 ::1 ::1 MQTT 93 Subscribe Request (id=1) [test/topic] | Subscribe Request                          |
| **SUBACK**             | 11 0.003082 ::1 ::1 MQTT 81 Subscribe Ack (id=1)                 | Subscribe Acknowledge                      |
| **PUBLISH (QoS 0)**    | 21 5.949913 ::1 ::1 MQTT 101 Publish Message [test/topic]        | Publish Message (QoS 0)                    |
| **DISCONNECT**         | 22 5.949926 ::1 ::1 MQTT 78 Disconnect Req                      | Disconnect Request                         |
| **PUBLISH (QoS 1)**    | 37 9.434860 ::1 ::1 MQTT 105 Publish Message (id=1) [test/topic] | Publish Message (QoS 1)                    |
| **PUBACK**             | 40 9.434970 ::1 ::1 MQTT 80 Publish Ack (id=1)                   | Publish Acknowledge (QoS 1)                |
| **PUBLISH (QoS 2)**    | 57 12.717463 ::1 ::1 MQTT 105 Publish Message (id=1) [test/topic]| Publish Message (QoS 2)                    |
| **PUBREC**             | 59 12.717536 ::1 ::1 MQTT 80 Publish Received (id=1)             | Publish Received (QoS 2)                   |
| **PUBREL**             | 61 12.717607 ::1 ::1 MQTT 80 Publish Release (id=1)              | Publish Release (QoS 2)                    |
| **PUBCOMP**            | 64 12.717700 ::1 ::1 MQTT 80 Publish Complete (id=1)             | Publish Complete (QoS 2)                   |
| **PINGREQ**            | 73 59.880223 ::1 ::1 MQTT 78 Ping Request                        | Ping Request                               |
| **PINGRESP**           | 75 59.880353 ::1 ::1 MQTT 78 Ping Response                       | Ping Response                              |
| **UNSUBSCRIBE**        | 105 184.485544 ::1 ::1 MQTT 92 Unsubscribe Request (id=2)        | Unsubscribe Request                        |
| **UNSUBACK**           | 109 184.485747 ::1 ::1 MQTT 80 Unsubscribe Ack (id=2)            | Unsubscribe Acknowledge                    |


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
