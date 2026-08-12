# Investigation 01 — Failed Logon

## Objective

Investigate Windows Security Event ID 4625 and determine
whether the failed authentication activity is suspicious.

## Lab Environment

- OS: Windows 11
- Log Source: Windows Event Viewer
- Log: Windows Security Log
- Event ID: 4625

## Scenario

Multiple incorrect password attempts were intentionally
generated against a test account in a controlled lab
environment.

## Investigation

Event ID: 4625
Event Type: Failed Logon

Important fields:

- Account Name: soc test
- Logon Type: 2
- Failure Reason: Unknown user name or bad password.
- Workstation Name: TEJAS
- Source Network Address: 127.0.0.1
- Timestamp: 12-08-2026 15:23:16

## Analysis

A 4625 event indicates that a logon attempt failed.

A single failed login does not necessarily indicate
malicious activity. Multiple failures from the same
source within a short period could indicate possible
brute-force activity.

## Questions Investigated

1. Which account was targeted?
2. When did the failures occur?
3. What was the Logon Type?
4. What was the source?
5. Were there multiple attempts?
6. Was a successful login observed afterwards?

## Conclusion

The observed event represents a failed authentication
attempt. Additional events and timeline correlation are
required before determining whether the activity is
malicious.

## Next Investigation

Check Event ID 4624 for successful authentication after
the failed attempts and correlate the timestamps.
