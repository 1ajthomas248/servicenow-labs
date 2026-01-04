# Lab 01 – Incident Management Fundamentals

### Overview

This lab focuses on understanding and practicing the core incident management workflow in ServiceNow. The objective is to simulate how a Tier 1 help desk analyst handles a user-reported issue from initial intake through investigation, escalation, and resolution in an enterprise IT environment.

The lab walks through creating basic support structure, submitting an incident, working the ticket as Tier 1 support, escalating to Tier 2, and properly resolving and closing the incident.

### Environment Details

Platform: ServiceNow
Release: Zurich
Instance Type: Personal Developer Instance (PDI)
Role Simulated: Tier 1 IT Support / Help Desk Analyst

### Phase 1 – Create Assignment Groups

The first step is to create assignment groups that represent support teams in a real organization.

- Navigate to User Administration → Groups.

- Create the following groups:

```
Group 1
Name: Service Desk Tier 1
Description: Frontline IT support team
```

```
Group 2
Name: Messaging / Email Support
Description: Tier 2 team responsible for email systems
```

These groups simulate Tier 1 and Tier 2 ownership during the incident lifecycle.

<img width="512" height="128" alt="image" src="https://github.com/user-attachments/assets/b5f1dd85-97ef-41ca-b030-de1dd336a5cf" />
<img width="512" height="88" alt="image" src="https://github.com/user-attachments/assets/346f7032-8790-4f1c-a0f0-b8c2390ce40e" />

### Phase 2 – Create a Test End User

Next, create an end user who will report an issue.

- Navigate to User Administration → Users → New.

- Create a user with the following details:

```
Name: Alex Johnson
User ID: alex.johnson
Email: alex.johnson@testcorp.com
Password: Set a simple test password
Roles: None
```

This user represents a standard employee without any IT permissions.

<img width="512" height="238" alt="image" src="https://github.com/user-attachments/assets/a69c20e5-6941-4eea-a961-31131caa6ac1" />

### Phase 3 – Create an Incident

Now simulate a real help desk issue by creating an incident.

Navigate to Incident → Create New.

Fill out the incident with the following details:

```
Caller: Alex Johnson
Short description: Unable to access corporate email
Description: User reports Outlook is not loading and webmail access is failing.
Category: Email
Impact: 2 – Medium
Urgency: 2 – Medium
```

Observe that the Priority field is automatically calculated based on impact and urgency.

Save the incident.

<img width="512" height="158" alt="image" src="https://github.com/user-attachments/assets/826c3f5c-8b71-478e-9308-693338698c8a" />

### Phase 4 – Assign and Work the Incident (Tier 1)

Simulate Tier 1 help desk handling the issue.

Open the incident and update the following fields:

```
Assignment group: Service Desk Tier 1
State: In Progress
```

Add a work note such as:
- Investigating email connectivity issue. Initial troubleshooting in progress.

Save the incident.

This step represents a Tier 1 analyst actively working the ticket.

### Phase 5 – Escalate the Incident (Tier 2)

Simulate escalation to a Tier 2 team after determining the issue requires specialized support.

Update the incident with the following changes:

```
Assignment group: Messaging / Email Support
Impact: 1 – High
```

Leave urgency unchanged.

Add a work note such as:
- Issue appears to affect multiple users. Escalating to Messaging team for further investigation.

Observe how the Priority increases automatically due to the updated impact.

Save the incident.

<img width="512" height="132" alt="image" src="https://github.com/user-attachments/assets/aa81b4a8-2a30-4d00-9e9b-bf2a6e2f5488" />

### Phase 6 – Resolve and Close the Incident

Simulate resolution of the issue by the Tier 2 team.

Update the incident:

```
State: Resolved
Resolution code: Solved (Permanent Fix or Workaround)
Resolution notes: Restarted email services and restored user access.
```

Save the incident.

Finally, change the state to Closed and save again.

This completes the full incident lifecycle.

<img width="512" height="89" alt="image" src="https://github.com/user-attachments/assets/df8044ab-8937-4754-aa53-f2bc43071fc5" />

### Key Takeaways

This lab demonstrated the complete incident lifecycle in ServiceNow, from user submission through investigation, escalation, and resolution. By creating assignment groups and an end user, the lab simulated a realistic Tier 1 help desk workflow and Tier 2 escalation process. The exercise reinforced how ServiceNow uses structured fields, ownership, and priority logic to manage incidents efficiently in enterprise IT environments.
