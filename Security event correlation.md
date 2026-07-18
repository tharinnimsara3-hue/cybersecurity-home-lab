# Security Event Correlation

## What is Security Event Correlation?

Security event correlation is the process of connecting multiple security events to identify suspicious activities or attacks.

## Why is it Important?

- Detects attacks more accurately.
- Reduces false positives.
- Helps analysts understand attack patterns.
- Improves incident investigations.

## Example

A possible attack sequence:

1. Multiple failed login attempts.
2. A successful login occurs.
3. Unusual processes are executed.
4. Suspicious network activity is detected.

When these events occur together, they may indicate an account compromise.

## Common Sources Used

- Windows Event Logs
- Linux Authentication Logs
- SIEM Alerts
- Firewall Logs
- Network Traffic Logs

## What I Learned

SOC analysts combine information from different sources to determine whether suspicious activities are related to the same incident.
