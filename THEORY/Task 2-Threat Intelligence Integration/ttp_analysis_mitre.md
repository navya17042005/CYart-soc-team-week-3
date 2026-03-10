# TTP Analysis Using MITRE ATT&CK

## Objective
To map observed authentication behavior to known attacker techniques using the MITRE ATT&CK framework.

## Observed Activity
During log analysis, multiple failed login attempts (Event ID 4625) were detected before a successful login event (Event ID 4624).

## MITRE ATT&CK Technique
Technique ID: T1110  
Technique Name: Brute Force

## Description
The Brute Force technique involves attackers attempting many passwords or passphrases until the correct one is discovered.

## Analysis
The repeated login failures observed in the security logs may indicate a brute-force authentication attempt targeting the user account.

## SOC Relevance
Mapping suspicious activity to MITRE ATT&CK helps SOC analysts understand attacker behavior and improve detection strategies.
