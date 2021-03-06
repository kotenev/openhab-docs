---
layout: documentation
title: PST02-1B - ZWave
---

{% include base.html %}

# PST02-1B Multisensor

This describes the Z-Wave device *PST02-1B*, manufactured by *Devolo* with the thing type UID of ```devolo_pst021b_00_000```. 

Multisensor


## Channels
The following table summarises the channels available for the PST02-1B Multisensor.

| Channel | Channel Id | Channel Type UID | Category | Item Type |
|---------|------------|------------------|----------|-----------|
| Binary Sensor | sensor_binary | sensor_binary | Door | Switch |
| Sensor (temperature) | sensor_temperature | sensor_temperature | Temperature | Number |
| Sensor (luminance) | sensor_luminance | sensor_luminance | Temperature | Number |
|  | battery-level | system.battery-level |  |  |


### Sensor (temperature)

#### Scale

Select the scale for temperature readings


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_scale |
| Data Type        | TEXT || Default Value | 0 |
| Options | Celsius (0) |
|  | Fahrenheit (1) |


### Device Configuration
The following table provides a summary of the configuration parameters available in the PST02-1B Multisensor.
Detailed information on each parameter can be found below.

| Parameter   | Description |
|-------------|-------------|
| 2: Basic Set Level | \-1 -> 0xFF(-1) turns on the light. 1 - 100 -> For dimmers 1 to 100 means the light streng... |
| 3: PIR Sensitivity | parameter to set the Sensitivity for the PIR (Passiv Infrared Sensor) 0 -> 0 means disable... |
| 4: Light Threshold | Setting the illumination threshold to turn on the light. When the event triggered and the ... |
| 5: Operation Mode | Bit 0: 1 means security mode; 0 means home automation mode. Bit 1: 1 means enable test mod... |
| 6: Multi-Sensor Function Switch | Bit 0: Disable magnetic integrate illumination. Bit 1: Disable PIR integrate Illumination.... |
| 7: Customer Function | Parameter to set the Customer Function. Bit 0: Reserved. Bit 1: Enable sending motion OFF ... |
| 8: PIR Re-Detect Interval Time | In the security mode, after the PIR motion detected, setting the re-detect time 3 8 sec - ... |
| 9: Turn Off Light Time | After turn on the light, setting the delay time to turn off the light when the PIR motion ... |
| 10: Auto Report Battery Time | interval time for auto report the battery level 1 30 min - 127 30 min -> 30 minutes per ti... |
| 12: Auto Report Illumination Time | interval time for auto report the illumination state 1 30 min - 127 30 min -> 30 minutes p... |
| 13: Auto Report Temperature Time | Interval time for auto report the temperature state 1 30 min - 127 30 min -> 30 minutes pe... |
| 1: Reports |  |
| 2: Light Control |  |


#### 2: Basic Set Level

\-1 -> 0xFF(-1) turns on the light. 1 - 100 -> For dimmers 1 to 100 means the light strength


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_2_1 |
| Data Type        | INTEGER |
| Range | -1 to 100 |
| Default Value | -1 |


#### 3: PIR Sensitivity

parameter to set the Sensitivity for the PIR (Passiv Infrared Sensor) 0 -> 0 means disable the PIR motion; 1 - 99 -> 1 means the lowest sensitivity, 99 means the highest sensitivity


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_3_1 |
| Data Type        | INTEGER |
| Range | 0 to 99 |
| Default Value | 70 |


#### 4: Light Threshold

Setting the illumination threshold to turn on the light. When the event triggered and the environment illumination lower then the threshold, the device will turn on the light 0 -> 0 means turn off illumination detected function And never turn on the


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_4_1 |
| Data Type        | INTEGER |
| Range | 0 to 100 |
| Default Value | 100 |


#### 5: Operation Mode

Bit 0: 1 means security mode; 0 means home automation mode. Bit 1: 1 means enable test mode; 0 means disable test mode. Notice: Bit0 and Bit1 will effect when the DIP Switch setting to program mode. If Bit1 is enabled, the Bit0 is useless. Bit 2: Disable


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_5_1 |
| Data Type        | INTEGER |
| Range | 0 to 127 |
| Default Value | 0 |


#### 6: Multi-Sensor Function Switch

Bit 0: Disable magnetic integrate illumination. Bit 1: Disable PIR integrate Illumination. Bit 2: Disable magnetic integrate PIR (Default is Disable) Bit 3: When Bit2 is 0 (Enable), the device is install in the same room with the light? 0: In the same roo


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_6_1 |
| Data Type        | INTEGER |
| Range | 0 to 127 |
| Default Value | 4 |


#### 7: Customer Function

Parameter to set the Customer Function. Bit 0: Reserved. Bit 1: Enable sending motion OFF report. 0: Disable, 1: Enable. Note: Depends on the Bit4, 0: Report Notification CC, Type: 0x07, Event: 0xFE 1: Sensor Binary Report,


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_7_1 |
| Data Type        | INTEGER |
| Range | 0 to 127 || Default Value | 0 |
| Options | Preset: PIR Super Sensitivity and Binary Report and Motion Off Report (22) |


#### 8: PIR Re-Detect Interval Time

In the security mode, after the PIR motion detected, setting the re-detect time 3 8 sec - 127 8 sec -> 8 seconds per tick, and minimum time is 24 seconds, default tick is 3 (24 seconds).


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_8_1 |
| Data Type        | INTEGER |
| Range | 3 to 127 |
| Default Value | 3 |


#### 9: Turn Off Light Time

After turn on the light, setting the delay time to turn off the light when the PIR motion is not detected 4 8 sec - 127 8 sec -> 8 seconds per tick, and minimum time is 32 seconds, default tick is 4 (32 seconds)


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_9_1 |
| Data Type        | INTEGER |
| Range | 4 to 127 |
| Default Value | 4 |


#### 10: Auto Report Battery Time

interval time for auto report the battery level 1 30 min - 127 30 min -> 30 minutes per tick and minimum time is 30 minutes, default tick is 12 (6 hours)


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_10_1 |
| Data Type        | INTEGER |
| Range | 1 to 127 |
| Default Value | 12 |


#### 12: Auto Report Illumination Time

interval time for auto report the illumination state 1 30 min - 127 30 min -> 30 minutes per tick and minimum time is 30 minutes, default tick is 12 (6 hours)


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_12_1 |
| Data Type        | INTEGER |
| Range | 1 to 127 |
| Default Value | 12 |


#### 13: Auto Report Temperature Time

Interval time for auto report the temperature state 1 30 min - 127 30 min -> 30 minutes per tick and minimum time is 30 minutes, default tick is 12 (6 hours)


| Property         | Value    |
|------------------|----------|
| Configuration ID | config_13_1 |
| Data Type        | INTEGER |
| Range | 1 to 127 |
| Default Value | 12 |


#### 1: Reports


| Property         | Value    |
|------------------|----------|
| Configuration ID | group_1 |
| Data Type        | TEXT |
| Range |  to  |


#### 2: Light Control


| Property         | Value    |
|------------------|----------|
| Configuration ID | group_2 |
| Data Type        | TEXT |
| Range |  to  |


---

Did you spot an error in the above definition or want to improve the content?
You can edit the database [here](http://www.cd-jackson.com/index.php/zwave/zwave-device-database/zwave-device-list/devicesummary/534).
