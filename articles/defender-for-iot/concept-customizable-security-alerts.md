---
title: Custom security alerts
description: Learn about customizable security alerts and recommended remediation using Defender for IoT features and service.
services: defender-for-iot
ms.service: defender-for-iot
documentationcenter: na
author: mlottner
manager: rkarlin
editor: ''

ms.devlang: na
ms.topic: conceptual
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/04/2020
ms.author: mlottner
---

# Defender for IoT custom security alerts

Defender for IoT continuously analyzes your IoT solution using advanced analytics and threat intelligence to alert you to malicious activity.

We encourage you to create custom alerts based on your knowledge of expected device behavior to ensure alerts act as the most efficient indicators of potential compromise in your unique organizational deployment and landscape.

The following lists of Defender for IoT alerts are definable by you based on your expected IoT Hub and/or device behavior. For more information about how to customize each alert, see [create custom alerts](quickstart-create-custom-alerts.md).

## Built-in custom alerts in the IoT Hub

| Severity | Alert name | Data source | Description | Suggested remediation |
|--|--|--|--|--|
| Low | Custom alert - The number of cloud to device messages in AMQP protocol is outside the allowed range | IoT Hub | The number of cloud to device messages (AMQP protocol) within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of rejected cloud to device messages in AMQP protocol is outside the allowed range | IoT Hub | The number of cloud to device messages (AMQP protocol) rejected by the device, within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of device to cloud messages in AMQP protocol is outside the allowed range | IoT Hub | The amount of device to cloud messages (AMQP protocol) within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of direct method invokes is outside the allowed range | IoT Hub | The amount of direct method invokes within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of file uploads is outside the allowed range | IoT Hub | The amount of file uploads within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of cloud to device messages in HTTP protocol is outside the allowed range | IoT Hub | The amount of cloud to device messages (HTTP protocol) in a time window is not in the configured allowed range |
| Low | Custom alert - The number of rejected cloud to device messages in HTTP protocol is not in the allowed range | IoT Hub | The amount of cloud to device messages (HTTP protocol) within a specific time window is outside the currently configured and allowable range. |
| Low | Custom alert - The number of device to cloud messages in HTTP protocol is outside the allowed range | IoT Hub | The amount of device to cloud messages (HTTP protocol) within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of cloud to device messages in MQTT protocol is outside the allowed range | IoT Hub | The amount of cloud to device messages (MQTT protocol) within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of rejected cloud to device messages in MQTT protocol is outside the allowed range | IoT Hub | The amount of cloud to device messages (MQTT protocol) rejected by the device within a specific time window is outside the currently configured and allowable range. |
| Low | Custom alert - The number of device to cloud messages in MQTT protocol is outside the allowed range | IoT Hub | The amount of device to cloud messages (MQTT protocol) within a specific time window is outside the currently configured and allowable range. |
| Low | Custom alert - The number of command queue purges that are outside of the allowed range | IoT Hub | The amount of command queue purges within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The number of module twin updates is outside the allowed range | IoT Hub | The amount of module twin updates within a specific time window is outside the currently configured and allowable range. |
| Low | Custom alert - The number of unauthorized operations is outside the allowed range | IoT Hub | The amount of unauthorized operations within a specific time window is outside the currently configured and allowable range. |


## Agent-based security custom alerts

| Severity | Alert name | Data source | Description | Suggested remediation |
|--|--|--|--|--|
| Low | Custom alert - The number of active connections is outside the allowed range | Classic security module, Azure RTOS | Number of active connections within a specific time window is outside the currently configured and allowable range. | Investigate the device logs. Learn where the connection originated and determine if it is benign or malicious. If malicious, remove possible malware and understand source. If benign, add the source to the allowed connection list. |
| Low | Custom alert - The outbound connection created to an IP that isn't allowed | Classic security module, Azure RTOS | An outbound connection was created to an IP that is outside your allowed IP list. | Investigate the device logs. Learn where the connection originated and determine if it is benign or malicious. If malicious, remove possible malware and understand source. If benign, add the source to the allowed IP list. |
| Low | Custom alert - The number of failed local logins is outside the allowed range | Classic security module, Azure RTOS | The number of failed local logins within a specific time window is outside the currently configured and allowable range. |  |
| Low | Custom alert - The sign in of a user that is not on the allowed user list | Classic security module, Azure RTOS | A local user outside your allowed user list, logged in to the device. | If you are saving raw data, navigate to your log analytics account and use the data to investigate the device, identify the source, and then fix the allow/block list for those settings. If you are not currently saving raw data, go to the device and fix the allow/block list for those settings. |
| Low | Custom alert - A process was executed that is not allowed | Classic security module, Azure RTOS | A process that is not allowed was executed on the device. | If you are saving raw data, navigate to your log analytics account and use the data to investigate the device, identify the source, and then fix the allow/block list for those settings. If you are not currently saving raw data, go to the device and fix the allow/block list for those settings. |
|

## Next steps

- Learn how to [customize an alert](quickstart-create-custom-alerts.md)
- Defender for IoT service [Overview](overview.md)
- Learn how to [Access your security data](how-to-security-data-access.md)
- Learn more about [Investigating a device](how-to-investigate-device.md)
