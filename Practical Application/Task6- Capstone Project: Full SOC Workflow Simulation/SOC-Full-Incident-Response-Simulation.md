# Full SOC Workflow Simulation

## Overview

This project simulates a complete Security Operations Center (SOC) workflow including attack simulation, detection, triage, containment, escalation, and incident reporting.

The objective is to demonstrate how SOC analysts respond to real-world security incidents using common security tools.

## Tools Used

- Metasploit
- Wazuh SIEM
- CrowdSec
- TheHive
- Google Docs


# 1. Attack Simulation

A simulated cyberattack was performed using the Metasploit framework targeting a known vulnerability in the Metasploitable2 virtual machine.

The exploit used was:

exploit/multi/samba/usermap_script

This exploit targets a vulnerability in Samba that allows remote attackers to execute commands on the target system.

The attack was launched from a Kali Linux machine against the Metasploitable2 server.


# 2. Detection and Triage

The attack was detected using the Wazuh SIEM platform which monitors security events and generates alerts for suspicious activity.

| Timestamp | Source IP | Alert Description | MITRE Technique |
|-----------|-----------|------------------|----------------|
| 2025-08-18 14:00:00 | 192.168.1.101 | Samba exploit | T1210 |

MITRE Technique:

T1210 – Exploitation of Remote Services

This alert indicates an attempt to exploit a vulnerable network service.

# 3. Response and Containment

After confirming the malicious activity, containment measures were implemented.

The attacker IP address was blocked using CrowdSec to prevent further exploitation attempts.

The affected virtual machine was isolated from the network to stop the attacker from gaining additional access.

The block was verified using a ping test which confirmed that the attacker system could no longer communicate with the target host.

# 4. Incident Escalation

The incident was escalated to Tier 2 analysts using TheHive incident management platform.

Case Title:
Unauthorized Samba Exploit Attempt

### Escalation Summary 

A high-priority security alert was triggered after suspicious activity targeting the Samba service was detected on the Metasploitable2 server. The attack originated from IP address 192.168.1.101 and attempted to exploit a known Samba vulnerability using the Metasploit framework. The alert was detected by Wazuh SIEM and classified as a potential exploitation attempt corresponding to MITRE ATT&CK technique T1210. Initial triage confirmed the presence of suspicious activity. Immediate containment actions were taken by blocking the attacker IP using CrowdSec and isolating the affected server. The incident has been escalated to Tier 2 analysts for further forensic investigation and remediation.

# 5. Incident Report

An incident report was created following the SANS reporting template.

## Executive Summary

A simulated attack targeting a Samba vulnerability was conducted in a controlled lab environment to test SOC monitoring and response capabilities. The attack was detected by Wazuh SIEM and investigated by SOC analysts.

## Timeline

14:00 – Metasploit exploit launched  
14:01 – Wazuh detected suspicious activity  
14:03 – Alert triaged by SOC analyst  
14:05 – Attacker IP blocked using CrowdSec  
14:10 – Incident escalated to Tier 2 via TheHive

## Recommendations

- Regular patch management for vulnerable services
- Continuous SIEM monitoring
- Network segmentation
- Improved intrusion detection rules

# 6. Management Briefing (100 words)

A simulated cyberattack targeting a vulnerable Samba service was detected in the SOC environment. The attack originated from an internal testing machine using the Metasploit framework. The monitoring system (Wazuh) successfully generated an alert identifying the suspicious activity. The SOC team analyzed the alert, confirmed the exploitation attempt, and implemented containment measures by blocking the attacker IP using CrowdSec. The affected system was isolated to prevent further compromise. The incident was escalated to Tier 2 analysts for deeper investigation. This exercise demonstrates the effectiveness of the SOC detection and response process in identifying and mitigating potential cyber threats.
