# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

This implementation adds functionality to the SystemPerformanceManager, defining some of its methods. Thus, the class and its methods can be invoked from the ConstrainedDeviceApp.

The BaseSystemUtilTask is built, and will serve as a core class for other classes to extend from, defining some of its getter methods. This allows SystemCpuUtilTask and SystemMemUtilTask to extend from BaseSystemUtilTask and implement functionality for collecting CPU (SystemCpuUtilTask) and memory (SystemMemUtilTask) utilization metrics from the local system.

Therefore, these two classes are instantiated in the SystemPerformanceManager, and their getTelemetryValue methods are used in the handleTelemetry method of the SystemPerformanceManager class. Additional logging info in the startManager and stopManager methods is also implemented.


### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/saraportto/python-components/tree/labmodule02

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest.py
- SystemPerformanceManagerTest.py

EOF.
