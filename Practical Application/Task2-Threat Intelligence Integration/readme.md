# Threat Intelligence Integration – SOC Investigation

## Overview

This project demonstrates how threat intelligence can be integrated into a Security Operations Center (SOC) workflow to enhance detection, investigation, and response. The integration of threat feeds such as AlienVault Open Threat Exchange (OTX) enables analysts to identify malicious indicators and enrich alerts with contextual intelligence.

Tools Used:

* Wazuh (SIEM)
* AlienVault OTX (Threat Intelligence)
* TheHive (Incident Management)

# 1. Threat Feed Import

Threat intelligence feeds provide indicators of compromise (IOCs) such as malicious IP addresses, domains, and file hashes. These indicators can be integrated into SIEM platforms to detect suspicious activity within monitored environments.

In this task, AlienVault OTX threat intelligence was used to identify malicious indicators. A mock malicious IP address was used to simulate IOC detection.

IOC Tested:
192.168.1.100

This IP address was searched within Wazuh security events to simulate detection of a known malicious indicator.


# 2. Alert Enrichment

Threat intelligence enrichment adds contextual information to alerts, allowing analysts to understand the risk and potential impact of suspicious activity.

The alert was enriched using AlienVault OTX intelligence, which provided reputation data for the identified IP address.

| Alert ID | IP            | Reputation      | Notes               |
| -------- | ------------- | --------------- | ------------------- |
| 003      | 192.168.1.100 | Malicious (OTX) | Linked to C2 server |

This enrichment allows analysts to quickly determine whether the alert requires escalation or containment actions.


# 3. Threat Hunting

Threat hunting was performed to identify suspicious login activity related to the MITRE ATT&CK framework technique **T1078 – Valid Accounts**.

A query was executed in Wazuh to identify user login events that were not associated with system accounts.

Query Used:
user.name != "system"

This query helps identify potential unauthorized account activity or misuse of legitimate credentials.


# Threat Hunting Summary 

Threat hunting was conducted using Wazuh to detect suspicious login activity associated with MITRE ATT&CK technique T1078 (Valid Accounts). Logs were filtered using the query `user.name != "system"` to identify non-system user logins. This approach helps detect unauthorized access attempts and potential credential misuse within monitored systems.

# Conclusion

Integrating threat intelligence feeds into SIEM platforms improves detection capabilities and provides valuable context for security alerts. In this task, AlienVault OTX indicators were used to simulate IOC detection and alert enrichment. Threat hunting techniques were also applied to identify suspicious account activity within system logs.

This workflow demonstrates how SOC analysts leverage threat intelligence to enhance incident detection, investigation, and response.
