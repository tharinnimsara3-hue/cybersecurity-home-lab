# Security Event Correlation Exercise

## Scenario

A user account generated 30 failed login attempts, followed by one successful login and unusual network activity five minutes later.

## Is This Suspicious?

Yes. This sequence of events is highly suspicious because multiple failed login attempts followed by a successful login may indicate a successful brute-force attack or unauthorized access.

## What Logs Would I Investigate?

I would investigate:

- Windows Security Event Logs
- Event ID 4625 (Failed Login Attempts)
- Event ID 4624 (Successful Login)
- SIEM alerts
- Network traffic logs
- Firewall logs
- Linux authentication logs (if Linux systems are involved)

## What Containment Actions Would I Recommend?

- Temporarily disable or lock the affected account.
- Reset the user's password.
- Enable Multi-Factor Authentication (MFA).
- Block suspicious IP addresses if identified.
- Increase monitoring of the affected systems.

## What Additional Evidence Would I Collect?

- Login timestamps.
- Source IP addresses.
- User activity after the successful login.
- Running processes on the affected system.
- Network connections established after authentication.
- Any additional security alerts generated during the incident.

## What I Learned

Security incidents often involve multiple related events. Correlating failed logins, successful logins, and network activity helps SOC analysts identify potential account compromise.
