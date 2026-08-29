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

![Department Configuration] <img width="2240" height="1403" alt="4C69C177-286B-494C-B5CA-348AA2960B9A_1_102_a" src="https://github.com/user-attachments/assets/23a456d3-02ff-4610-81c1-381b7e260fe1" />


---

## Ticket Example 1: Entire Mobile/Online Banking System Is Down

### Ticket Intake

As an end user, I created the following ticket:

```text
Entire mobile/online banking system is down.
```

This issue represented a business-critical outage affecting the organization’s online banking services and potentially many customers.

![Banking Outage Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

### Ticket Review

While signed in as help desk agent **John**, I reviewed the ticket’s initial properties:

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

![Sev-A Ticket Properties](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

### Department Access Test

After assigning the ticket to the Online Banking department, I attempted to view it again as **John**.

This demonstrated how department assignments and permissions affect whether an agent can view or modify a ticket.

### Resolution

I signed in as **Jane**, worked the escalated ticket, documented the resolution, and closed it after completing the issue.

![Resolved Banking Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

## Ticket Example 2: Accounting Department Needs an Adobe Upgrade

### Ticket Intake

As an end user, I created the following ticket:

```text
Accounting department needs an Adobe upgrade; the current installation is broken.
```

![Adobe Upgrade Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

### Ticket Review

While signed in as **John**, I reviewed the following ticket properties:

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

As **John**, I worked the ticket to completion, documented the actions taken, and closed the ticket after resolving the issue.

![Resolved Adobe Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

## Ticket Example 3: CFO’s Laptop Will Not Turn On

### Ticket Intake

As an end user, I created the following ticket:

```text
CFO's laptop will no longer turn on.
```

![CFO Laptop Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

### Ticket Review

While signed in as **John**, I reviewed the following ticket properties:

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

The **Sev-B** SLA was appropriate because the issue prevented an executive from using an essential work device and required a prompt response.

### Resolution

As **John**, I worked the ticket to completion, recorded the troubleshooting performed, and closed the ticket after resolving the issue.

![Resolved Laptop Ticket](https://github.com/user-attachments/assets/ADD-YOUR-IMAGE-LINK-HERE)

---

## Ticket Summary

| Ticket | SLA | Department | Agent |
|---|---|---|---|
| Entire mobile/online banking system is down | Sev-A: 1 hour, 24/7 | Online Banking | Jane |
| Accounting department needs an Adobe upgrade | Sev-B: 4 hours, 24/7 | Support | John |
| CFO’s laptop will not turn on | Sev-B: 4 hours, 24/7 | Support | John |

## Ticket Permissions and Escalation

I also tested osTicket’s role-based access behavior:

1. I configured the tickets and handled the **Sev-A** ticket last.
2. I switched to the Admin Panel.
3. I assigned myself view access to the **SysAdmins** department.
4. I returned to the Agent Panel and reviewed the escalated ticket.
5. I observed how department permissions determined whether an agent could view or modify the ticket.

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
