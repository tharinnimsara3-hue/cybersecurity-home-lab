# Brute-Force Detection

## What is a Brute-Force Attack?

A brute-force attack is an attempt to guess a user's password by trying many different passwords.

## Indicators of a Brute-Force Attack

- Multiple failed login attempts
- Repeated attempts from the same IP address
- Attempts against multiple user accounts
- High number of authentication failures

## Detection Methods

- Monitor Windows Event ID 4625
- Monitor Linux authentication logs
- Configure SIEM alerts
- Block suspicious IP addresses

## Prevention

- Strong passwords
- Multi-factor authentication (MFA)
- Account lockout policies
- Rate limiting
