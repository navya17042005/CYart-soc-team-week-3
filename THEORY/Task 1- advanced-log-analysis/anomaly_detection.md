# Anomaly Detection

## Objective
The objective of anomaly detection is to identify unusual or suspicious activities in system logs that deviate from normal user behavior.

## Observed Behavior
While analyzing the Windows Security logs, multiple failed login attempts (Event ID 4625) were observed within a very short time period.

These failed login attempts occurred before a successful login event (Event ID 4624).

## Suspicious Indicators
- Multiple failed login attempts in a short time frame
- Same user account targeted repeatedly
- Similar source network address for the attempts

## Analysis
Under normal conditions, users typically enter the correct password within one or two attempts. However, repeated failed login attempts within seconds or minutes indicate abnormal authentication behavior.

This pattern may suggest a **brute-force password attack**, where an attacker repeatedly tries different passwords to gain access.

## Conclusion
Detecting anomalies such as repeated login failures helps SOC analysts identify potential security threats and investigate possible unauthorized access attempts.
