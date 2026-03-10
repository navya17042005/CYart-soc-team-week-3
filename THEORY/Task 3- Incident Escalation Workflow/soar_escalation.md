# SOAR-Based Incident Escalation

## Objective
Demonstrate how Security Orchestration, Automation, and Response (SOAR) platforms automate incident escalation in a SOC environment.

## Incident Example
Multiple failed login attempts followed by a successful login were detected in Windows authentication logs.

Event IDs:
4625 – Failed Login  
4624 – Successful Login

## Automated Workflow

1. SIEM detects suspicious authentication activity.
2. The alert is forwarded to the SOAR platform.
3. SOAR automatically enriches the alert using threat intelligence sources.
4. A ticket is automatically created in the incident management system.
5. The alert is assigned to a Tier 1 SOC analyst.
6. If the incident severity is high, SOAR automatically escalates the case to Tier 2 analysts.

## Example Automation Tasks

- Automatic IP reputation lookup
- Alert severity classification
- Ticket generation
- Analyst assignment

## Benefits of SOAR Automation

- Faster incident response
- Reduced manual workload
- Consistent incident handling
- Improved SOC efficiency

## Conclusion

SOAR platforms automate repetitive tasks such as alert enrichment and ticket assignment, allowing SOC analysts to focus on deeper investigation and threat response.

SIEM Alert Triggered
        ↓
SOAR Platform Receives Alert
        ↓
Threat Intelligence Lookup
        ↓
Ticket Created Automatically
        ↓
Assigned to Tier 1 Analyst
        ↓
If High Severity → Escalate to Tier 2
