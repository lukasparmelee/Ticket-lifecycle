# osTicket Help Desk Lab — Ticket Lifecycle Management

**Project type:** Hands-on IT support simulation  
**Focus:** Ticket intake, prioritization, assignment, escalation, and resolution  
**Environment:** Microsoft Azure virtual machine, Windows 10 (21H2), Remote Desktop, IIS, osTicket v1.15.8

## Project overview

I used an osTicket lab environment to simulate common IT service desk workflows, from an end user's initial request through agent triage and ticket closure. I practiced reviewing ticket properties, assigning departments and severity-based service-level agreements (SLAs), and working within agent access permissions.

**What this project demonstrates:** help desk ticket management, incident prioritization, support routing, role-based access awareness, and documentation of support workflows.

> **Scope:** This is a simulated training environment, not a production help desk. The incidents, users, and SLAs below are lab scenarios; no real financial system or employee device was affected.

## Lab environment

- **Cloud infrastructure:** Microsoft Azure virtual machines
- **Remote administration:** Remote Desktop
- **Web server:** Internet Information Services (IIS)
- **Ticketing platform:** osTicket v1.15.8
- **Operating system:** Windows 10 (21H2)

## Workflow objectives

1. Create tickets from the end-user portal.
2. Review and modify ticket properties as a help desk agent.
3. Assign tickets to departments and apply appropriate SLAs.
4. Observe how agent permissions affect ticket visibility.
5. Escalate, work, and close tickets in the simulated environment.

## Step-by-step lab walkthrough

### 1. Access the end-user and agent portals

I used the local osTicket installation to access the two interfaces:

- **End-user portal:** `http://localhost/osTicket`
- **Staff/admin login:** `http://localhost/osTicket/scp/login.php`

These addresses refer to the lab machine's local installation.

![End-user portal login](./enduser.png)

![Staff and admin login](./admin.png)

### 2. Ticket 1 — Mobile and online banking outage

**Scenario:** “Entire mobile/online banking system is down”

- **Submitted by:** Karen (end user)
- **Agent:** John
- **SLA:** Sev-A — 1 hour, 24/7
- **Department:** Online Banking

I reviewed the ticket's priority, department, SLA, and assignee fields. I applied the Sev-A SLA and routed the ticket to Online Banking. I then signed in as John to examine the ticket's visibility and access restrictions. In the lab, the ticket was ultimately resolved using Jane's SysAdmins account.

![Banking outage ticket](./ticket-3.png)

### 3. Ticket 2 — Accounting software upgrade

**Scenario:** “Accounting department needs Adobe upgrade, broken”

- **Submitted by:** Ken (end user)
- **Agent:** John
- **SLA:** Sev-C — 8 business hours
- **Department:** Support

I inspected the ticket properties, applied the Sev-C SLA, routed it to Support, and worked the ticket to completion as John.

![Adobe upgrade support ticket](./ticket-4.png)

### 4. Ticket 3 — CFO laptop not powering on

**Scenario:** “CFO’s laptop will no longer turn on”

- **Submitted by:** Karen (end user)
- **Agent:** John
- **SLA:** Sev-B — 4 hours, 24/7
- **Department:** Support

I reviewed and updated ticket properties, applied the Sev-B SLA, assigned the Support department, and completed the simulated troubleshooting and ticket closure as John.

![CFO laptop support ticket](./ticket-5.png)

## Incident prioritization summary

| Lab ticket | Department | SLA applied | Workflow practiced |
| --- | --- | --- | --- |
| Online banking outage | Online Banking | Sev-A: 1 hour, 24/7 | High-severity routing, agent access checks, escalation |
| Adobe upgrade issue | Support | Sev-C: 8 business hours | Routine support request handling and completion |
| CFO laptop won't power on | Support | Sev-B: 4 hours, 24/7 | Prioritization, troubleshooting workflow, closure |

*These SLA settings were defined for the lab. They are not universal industry severity definitions.*

## Skills demonstrated and lessons learned

- **Ticket triage:** Different incidents require different routing and response expectations.
- **SLA awareness:** Service targets help agents prioritize work; the specific thresholds depend on organizational policy.
- **Role-based access:** Agent accounts may not have identical visibility or authority over tickets.
- **Support workflow:** A ticket should have an identifiable owner, appropriate categorization, and a documented resolution path.

## Related projects

This project is the final stage of a three-part osTicket lab:

1. [osTicket installation and prerequisites](https://github.com/lukasparmelee/osTicket-prereqs)
2. [osTicket post-installation configuration](https://github.com/lukasparmelee/post-install-config)
3. **Ticket lifecycle management** (this repository)

[Return to my GitHub portfolio](https://github.com/lukasparmelee)

## Security and reproducibility notes

This project documents a historical training environment. The local URLs, user names, example incidents, and SLA settings are illustrative. Any recreated environment should use supported software versions, unique credentials, appropriate access restrictions, and no real customer information.
