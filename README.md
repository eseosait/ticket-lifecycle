# osTicket: Ticket Lifecycle Examples

## Project Overview

In this lab, I practiced the complete lifecycle of help desk tickets in **osTicket**. I created tickets as an end user, reviewed and modified ticket properties as a help desk agent, assigned tickets to the appropriate departments, documented troubleshooting activity, and resolved the tickets.

This lab simulated how help desk professionals manage incidents from initial intake through resolution.

## Environments and Technologies Used

- Microsoft Azure Virtual Machine
- Windows 10/11
- Internet Information Services (IIS)
- osTicket
- Web browser

## osTicket Access URLs

### Admin/Analyst Login Page

```text
http://localhost/osTicket/scp/login.php
```

### End-User Portal

```text
http://localhost/osTicket
```

## Ticket Lifecycle

The general lifecycle followed during this lab was:

1. A user submitted a support ticket.
2. A help desk agent reviewed the ticket properties.
3. The ticket was categorized and prioritized.
4. An SLA plan and department were assigned.
5. The ticket was assigned to an agent or team.
6. Troubleshooting notes and updates were added.
7. The issue was resolved and the ticket was closed.

## Preliminary Configuration

Before creating the tickets, I completed the following administrative changes:

- Changed the **SysAdmins** department into a top-level department.
- Deleted the **Maintenance** department instead of archiving it.


---

## Ticket Example 1: Entire Mobile/Online Banking System Is Down

### Ticket Intake

As an end user, I created the following ticket:

```text
Entire mobile/online banking system is down.
```

This issue represented a business-critical outage affecting the organization’s online banking services and potentially many customers.

![Banking Outage Ticket] <img width="2240" height="1403" alt="4C69C177-286B-494C-B5CA-348AA2960B9A_1_102_a" src="https://github.com/user-attachments/assets/738a1114-7788-45e1-a87d-be91a4e51cc2" />


### Ticket Review

While signed in as help desk agent **Emma**, I reviewed the ticket’s initial properties:

- Priority
- Department
- SLA plan
- Assigned agent or team

### Ticket Classification and Escalation

I updated the ticket with the following properties:

| Property | Selection |
|---|---|
| Severity/SLA | Sev-A |
| Grace Period | 1 hour |
| Schedule | 24/7 |
| Department | Online Banking |

The **Sev-A** SLA was appropriate because a complete banking outage is a critical incident requiring immediate attention.

![Sev-A Ticket Properties] <img width="2200" height="1429" alt="C0C57015-4043-4B06-9229-654C7A5D5805_1_102_o" src="https://github.com/user-attachments/assets/4da965a4-2f08-46b2-9c96-36c3ed78e024" />

### Department Access Test

After assigning the ticket to the Online Banking department, I attempted to view it again as **John**.

This demonstrated how department assignments and permissions affect whether an agent can view or modify a ticket.
<img width="2200" height="1429" alt="927C12F7-4645-45F8-8DBD-52F3A098E3E7_1_102_o" src="https://github.com/user-attachments/assets/1c1ee654-60d1-4f20-8b86-6c0af0f9e1a1" />


### Resolution

I signed in as **Ikponmwosa**, worked the escalated ticket, documented the resolution, and closed it after completing the issue.
<img width="2200" height="1429" alt="0C939A1F-66AD-49DE-8AD9-0B92819D715D_1_102_o" src="https://github.com/user-attachments/assets/4e74bdc8-32db-4c5d-93a1-d6a268b5c96c" />
<img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/0c59e842-ef35-48c7-b768-af62bc2433c4" />


![Resolved Banking Ticket] <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/9eaea41e-c824-48a9-9d95-33fc580de3d3" /> <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/e5b47707-9b8d-4fb9-8354-3f75b3513080" />


---

## Ticket Example 2: Accounting Department Needs an Adobe Upgrade

### Ticket Intake

As an end user, I created the following ticket:

```text
Can't access the Finance Shared folder
```

![Can't access the Finance Shared folder Ticket] <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/6fec39dc-6ed5-42a3-a1b8-b88496ca3d62" />


### Ticket Review

While signed in as **Emma**, I reviewed the following ticket properties:

- Priority
- Department
- SLA plan
- Assigned agent or team

### Ticket Classification

I updated the ticket with the following properties:

| Property | Selection |
|---|---|
| Severity/SLA | Sev-B |
| Grace Period | 4 hours |
| Schedule | 24/7 |
| Department | Support |

The **Sev-B** SLA was appropriate because the broken application affected business operations but was not a company-wide critical outage.

### Resolution

As **Emma**, I worked the ticket to completion, documented the actions taken, and closed the ticket after resolving the issue.

![Resolved the Finance Shared folder Ticket] <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/d8dc2b3c-833a-411f-887c-a877bba572cd" />


---

## Ticket Example 3: Can't access the Finance shared folder

### Ticket Intake

As an end user, I created the following ticket:

```text
Can't access the Finance Shared folder
```

![Can't access the Finance shared folder Ticket]
<img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/d26c46f7-b459-4900-84b2-0ba7534dc22e" />


### Ticket Review

While signed in as **Emma**, I reviewed the following ticket properties:

- Priority
- Department
- SLA plan
- Assigned agent or team

### Ticket Classification

I updated the ticket with the following properties:

| Property | Selection |
|---|---|
| Default/SLA | Sev-C |
| Grace Period | 8 hours |
| Schedule | 24/7 |
| Department | Support |

The **Sev-C** SLA was appropriate because the issue prevented only one user from getting access to the shared folder.

### Resolution

As **Emma**, I worked the ticket to completion, recorded the troubleshooting performed, and closed the ticket after resolving the issue.

![Resolved Shared access folder Ticket] <img width="3024" height="1964" alt="image" src="https://github.com/user-attachments/assets/3fcb3297-f9f1-4d9e-8112-8eb2fb4afb57" />


---

## Ticket Summary

| Ticket | SLA | Department | Agent |
|---|---|---|---|
| Can't access the Finance shared folder | Sev-C: 8 hour, 24/7 | Support | Emma |

## Ticket Permissions and Escalation

I also tested osTicket’s role-based access behavior:

1. I configured the tickets and handled the **Sev-C** ticket.


This demonstrated how ticket visibility can change when tickets are transferred or escalated to different departments.

## Ticket Communication

Ticketing systems commonly send email notifications whenever a ticket is created or updated. These notifications provide the user with a copy of the response and allow communication to continue throughout the ticket’s lifecycle.

Documenting each update creates a clear history of:

- The reported problem
- Ticket assignments and transfers
- Troubleshooting actions
- Communication with the user
- The final resolution

## Ticket Intake Methods

Support tickets may be created through several channels, including:

- Web forms
- Email
- Phone calls
- Chat applications
- Walk-up or in-person requests
- Monitoring and alerting systems

Regardless of the intake method, the help desk should document the issue and manage it through a consistent ticket lifecycle.

## Skills Demonstrated

- Creating and managing support tickets
- Reviewing and updating ticket properties
- Prioritizing incidents according to business impact
- Applying SLA plans
- Assigning and transferring tickets
- Working with departments and agent permissions
- Escalating critical incidents
- Documenting troubleshooting and resolutions
- Resolving and closing tickets
- Communicating with end users

## Conclusion

This lab provided practical experience managing support requests from initial submission through resolution. I learned how ticket priority, SLA requirements, department assignments, agent permissions, escalation, and documentation work together in an enterprise help desk environment.
