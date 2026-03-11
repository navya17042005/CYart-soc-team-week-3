## Log Correlation Analysis

Sample logs were analyzed to identify suspicious authentication activity.

Multiple failed login attempts (Event ID 4625) were observed from the same IP address followed by a successful login (Event ID 4624). Shortly after authentication, outbound network traffic was detected.

This pattern suggests a potential brute-force attack followed by external communication.
