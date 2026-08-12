# Windows Event Log Investigation Lab

![Event Viewer Notes Banner](https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=1200&q=80)

## Objective

Hands-on investigation of Windows Security Events using Windows Event Viewer.

The lab focuses on authentication and account activity and documents the process of collecting, filtering, and analysing Windows event logs.

## Lab Environment

* OS: Windows
* Tool: Windows Event Viewer
* Log: Windows Security
* Environment: Local Windows Lab

## Events Investigated

| Event ID | Activity                    |
| -------- | --------------------------- |
| 4624     | Successful Logon            |
| 4625     | Failed Logon                |
| 4672     | Special Privileges Assigned |
| 4720     | User Account Created        |

## Investigation Process

```text
Windows Event Viewer
        ↓
Windows Logs
        ↓
Security
        ↓
Filter Event ID
        ↓
Open Event
        ↓
Review Details
        ↓
Analyze Activity
        ↓
Document Findings
```

## 4625 — Failed Logon

Event ID 4625 records an unsuccessful logon attempt.

Investigation fields:

* Account Name
* Logon Type
* Failure Reason
* Timestamp
* Source information

The event was generated using controlled failed login attempts in the lab.

## 4624 — Successful Logon

Event ID 4624 records a successful authentication.

Investigation fields:

* Account Name
* Logon Type
* Timestamp
* Workstation
* Source information
* Authentication details

4624 was correlated with 4625 events to examine authentication activity.

## 4672 — Special Privileges Assigned

Event ID 4672 records a logon session where special privileges were assigned.

Investigation fields:

* Account
* Account Domain
* Assigned Privileges
* Timestamp

The event was reviewed to understand the activity of privileged accounts.

## 4720 — User Account Created

Event ID 4720 records the creation of a Windows user account.

Investigation fields:

* New Account
* Account Creator
* Domain
* Timestamp

A test account was created in the controlled lab environment, and the resulting event was investigated.

## Evidence

Screenshots of the Event Viewer investigations are stored in:

```text
evidence/
└── screenshots/
    ├── 4625-filter.png
    ├── 4625-event.png
    ├── 4624-event.png
    ├── 4672-event.png
    └── 4720-event.png
```

Sensitive information is redacted before publication.

## Key Learning

* Windows Security log navigation
* Event ID filtering
* Authentication event analysis
* Account activity investigation
* Privileged activity identification
* Event correlation
* Evidence collection
* Basic SOC investigation methodology

## Technologies

* Windows
* Windows Event Viewer
* Windows Security Event Logs
* GitHub
