# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

This implementation aims to add functionality to the SystemPerformanceManager class, by defining some of its methods, which call the SystemCpuUtilTask and SystemMemUtilTask classes to correctly manage the system’s performance. To facilitate this, getters and setters for BaseSystemUtilTask are defined in order for SystemCpuUtilTask and SystemMemUtilTask to inherit from it. Moreover, the getTelemetryValue method is overridden in each of those two classes.  

Then, the SystemPerformanceManager class is instantiated in the GatewayDeviceApp, so that the GDA can properly handle the system’s performance.

A change had to be made in the BaseSystemUtilTask class, as its private Logger had to be switched to a protected Logger due to the errors thrown by SystemCpuUtilTask and SystemMemUtilTask tests when the Logger was private (it wasn’t accessible for them).


### Code Repository and Branch

URL: https://github.com/saraportto/java-components/tree/labmodule02


### Unit Tests Executed

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest


### Integration Tests Executed

- GatewayDeviceAppTest
- SystemPerformanceManagerTest

EOF.
