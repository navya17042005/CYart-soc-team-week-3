## Log Enrichment

## Objective
Log enrichment is the process of adding additional contextual information to raw log data to improve security analysis.

## Process
An IP address observed in the authentication logs was extracted and analyzed using external threat intelligence sources.

## IP Analysis
Source IP Address: 127.0.0.1

Lookup tools used:
- VirusTotal
- AbuseIPDB

## Result
The IP address belongs to the local system (loopback address), which indicates the login attempts originated from the same machine.

## Conclusion
Log enrichment helps analysts understand the origin and reputation of IP addresses involved in security events. This additional context improves incident investigation and threat detection.
