# Threat Hunting Exercise

## Scenario

A user account generated login attempts from multiple locations within ten minutes.

## Why Is This Suspicious?

This behavior is suspicious because it is unlikely that a legitimate user could successfully log in from multiple geographical locations within such a short period. It may indicate that an attacker has obtained the user's credentials.

## What Evidence Would I Collect?

I would collect:

- Login timestamps.
- Source IP addresses.
- Authentication logs.
- SIEM alerts.
- User activity logs.
- Network connection logs.
- Device information used during authentication.

## What Actions Would I Recommend?

- Verify whether the login attempts belong to the legitimate user.
- Temporarily lock the account if suspicious activity continues.
- Reset the user's password.
- Enable Multi-Factor Authentication (MFA).
- Continue monitoring the account for unusual behavior.
- Investigate whether other user accounts are experiencing similar activities.

## Lessons Learned

Threat hunting allows security analysts to proactively identify suspicious behavior before it becomes a serious security incident. Reviewing authentication patterns can help detect compromised accounts early.

## What I Learned

- How to identify suspicious login behavior.
- The importance of collecting evidence during investigations.
- How SOC analysts proactively search for potential threats.
- The role of threat hunting in improving organizational security.
