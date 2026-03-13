# Splunk Phantom Playbook – Auto Escalation

## Objective

Automatically assign high-priority alerts to Tier-2 SOC analysts.

## Trigger

Alert Severity = High

## Workflow Steps

1. Receive alert from SIEM.
2. Evaluate alert severity.
3. If severity = High, automatically create incident case.
4. Assign case to Tier-2 investigation team.
5. Notify SOC team via email or ticketing system.

## Test Scenario

A mock alert representing unauthorized access on Server-Y was generated. The playbook automatically assigned the alert to Tier-2 analysts for further investigation.

## Outcome

The automated workflow ensures faster escalation of critical alerts and improves incident response efficiency.
