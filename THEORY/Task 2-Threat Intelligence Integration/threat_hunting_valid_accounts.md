# Threat Hunting Using Threat Intelligence

## Objective
Use threat intelligence and authentication logs to proactively identify suspicious login activity.

## Hunting Technique
MITRE ATT&CK Technique: T1078 – Valid Accounts

## Data Source
Windows Security Logs

Key Event IDs:
4625 – Failed Login Attempt  
4624 – Successful Login

## Observed Pattern
Multiple failed login attempts were detected followed by a successful login event.

Example timeline:

10:01 – Failed login attempt  
10:02 – Failed login attempt  
10:03 – Failed login attempt  
10:04 – Successful login

## Analysis
Repeated authentication failures followed by a successful login may indicate a brute-force attempt where an attacker eventually guesses the correct password.

This behavior aligns with credential-based attacks described in the MITRE ATT&CK framework.

## Threat Hunting Result
The authentication logs show a pattern consistent with brute-force login attempts targeting a user account.

## Conclusion
Threat hunting using attacker techniques and authentication logs helps SOC analysts detect credential abuse and investigate suspicious login behavior.

## Threat Hunting with Intelligence

Threat hunting was performed on Windows authentication logs to identify suspicious login activity.

The observed pattern of repeated failed login attempts followed by a successful login was mapped to MITRE ATT&CK techniques related to credential abuse.

This demonstrates how threat intelligence and attacker techniques can guide proactive security investigations.
