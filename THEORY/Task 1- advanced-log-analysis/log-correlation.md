### Log Correlation Analysis

## Objective
To analyze Windows Security logs and identify suspicious login activity by correlating multiple log events.

## Logs Observed
Event ID 4625 – Failed Login Attempts  
Event ID 4624 – Successful Login

## Observation
Multiple failed login attempts were observed before a successful login.

Example pattern:

10:01 AM – Failed login attempt  
10:02 AM – Failed login attempt  
10:03 AM – Failed login attempt  
10:04 AM – Successful login

## Analysis
This pattern indicates a potential brute force attack attempt where an attacker repeatedly tries passwords until a successful login occurs.

## Conclusion
Correlating authentication logs helps SOC analysts detect suspicious login behavior and possible account compromise.
