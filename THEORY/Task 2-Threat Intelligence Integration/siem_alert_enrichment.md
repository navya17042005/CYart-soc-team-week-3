# SIEM Threat Intelligence Integration

## Objective
Demonstrate how threat intelligence feeds are integrated into SIEM platforms for automated alert enrichment.

## Scenario
A network log containing a suspicious IP address was analyzed.

Log Example:
Source IP: 185.220.101.45  
Destination IP: 192.168.1.10  
Port: 443

## Threat Intelligence Lookup
The source IP address was checked using VirusTotal.

## Result
The IP address is associated with TOR network infrastructure and may be used to hide attacker identity.

## Alert Enrichment
In a SIEM environment, the platform would automatically check incoming logs against threat intelligence feeds.

If the IP matches a known malicious indicator, the SIEM enriches the alert with additional information such as:

- IP reputation
- Known threat activity
- Related threat campaigns

## Conclusion
Threat intelligence integration improves SOC detection capabilities by automatically identifying known malicious indicators within security logs.

Security Log
     ↓
SIEM Platform
     ↓
Threat Intelligence Feed Check
     ↓
Malicious Indicator Match
     ↓
Alert Generated for SOC Analyst
