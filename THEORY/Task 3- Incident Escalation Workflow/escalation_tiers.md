# SOC Incident Escalation Tiers

## Objective
Understand how security incidents are escalated across SOC tiers.

## Incident Example
Multiple failed login attempts followed by a successful login were observed in Windows Security logs.

Event IDs:
4625 – Failed Login  
4624 – Successful Login

## Tier 1 – Triage (SOC Analyst)

Responsibilities:
- Monitor SIEM alerts
- Validate whether alert is real or false positive

Action Taken:
A Tier 1 analyst observed repeated authentication failures followed by successful login.

Result:
Activity flagged as suspicious.

Decision:
Escalated to Tier 2 for deeper investigation.

## Tier 2 – Investigation (SOC Analyst)

Responsibilities:
- Perform log analysis
- Correlate multiple events
- Check threat intelligence

Action Taken:
The analyst reviewed authentication logs and confirmed the pattern resembles a brute-force attempt.

MITRE Technique:
T1110 – Brute Force

Decision:
Escalated to Tier 3 for advanced analysis.

## Tier 3 – Advanced Analysis

Responsibilities:
- Malware analysis
- Advanced threat hunting
- Incident response

Action Taken:
Security team investigates whether the account has been compromised and checks for lateral movement.

## Conclusion
SOC escalation tiers ensure that security incidents are handled efficiently by analysts with increasing expertise.

SIEM Alert
     ↓
Tier 1 Analysis
     ↓
Escalate
     ↓
Tier 2 Investigation
     ↓
Escalate
     ↓
Tier 3 Incident Response
