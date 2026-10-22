# osTicket – Post-Installation Configuration (Part 2)

Independent configuration of roles, departments, teams, agents, users, SLAs and help topics in osTicket after the base installation.

## What was done
- Configured custom Roles with appropriate permission sets
- Created Departments (including a System Administrators department with 24/7 schedule)
- Created Teams (Level I Support and Level 2 Support)
- Configured user registration settings
- Added Agents (staff) and end Users (customers)
- Defined Service Level Agreements (SEV-A, SEV-B, SEV-C) with different response targets and schedules
- Created Help Topics for ticket categorisation
- Documented the complete post-installation configuration process

## Purpose
A personal exercise to understand help-desk configuration and how tickets are categorised, assigned and prioritised. It is not commercial IT service-desk experience.

## Tools & technologies used
- Microsoft Azure (Virtual Machines)
- Windows 10 (21H2)
- Internet Information Services (IIS)
- osTicket (admin panel)
- Remote Desktop

## AI assistance
None used for the core configuration or primary documentation.  
---

<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="200"/>
</p>

**Prerequisites (Part 1):**  
[https://github.com/LawrenceDavy/osticket-prereqs](https://github.com/LawrenceDavy/osticket-prereqs)

**Part 3 (Ticket Lifecycle):**  
[https://github.com/LawrenceDavy/ticket-lifecycle](https://github.com/LawrenceDavy/ticket-lifecycle)

> **Note:** Log in with admin credentials before starting these steps.

---

## 1. Configure Roles

![Roles](https://github.com/LawrenceDavy/post-install-config/assets/24421979/f48c50e0-dbe9-497b-84d9-78cff5350739)

Roles are sets of permissions matched to the responsibilities of different staff members.

- Go to **Admin Panel → Agents → Roles**
- Create / configure the required roles (example: Supreme Admin)

---

## 2. Configure Departments

![Departments](https://github.com/LawrenceDavy/post-install-config/assets/24421979/d0a03cce-bbd4-4428-bc62-bfe8ee5102d4)

Departments act as hubs for specific types of inquiries and can have their own settings.

- Go to **Admin Panel → Agents → Departments**
- Create a **System Administrators** department
- Assign yourself as manager
- Give the department full control of the ticketing system
- Set the schedule to **24/7** so tickets can be handled outside normal hours for emergencies

---

## 3. Configure Teams

![Teams](https://github.com/LawrenceDavy/post-install-config/assets/24421979/91b8033f-445c-4030-b0eb-945ba17f90d3)

Teams group agents from different departments so they can handle specific issues or users (via Help Topics or Ticket Filters).

- Go to **Admin Panel → Agents → Teams**
- Create:
  - Level I Support
  - Level 2 Support

---

## 4. User Registration Settings

![User Settings](https://github.com/LawrenceDavy/post-install-config/assets/24421979/b6beddd4-8e82-4c1b-8f08-1bdac56d4771)

- Go to **Admin Panel → Settings → Users**
- Decide whether registration and login are required to create tickets (or allow guest submissions)

---

## 5. Configure Agents (Staff)

![Agents](https://github.com/LawrenceDavy/post-install-config/assets/24421979/da9bde3c-1082-46d4-ac90-20c8cb75fef5)

Agents are the staff who respond to tickets.

- Go to **Admin Panel → Agents → Add New**
- Create example agents:
  - Jane Jane
  - John John

---

## 6. Configure Users (Customers / End Users)

![Users](https://github.com/LawrenceDavy/post-install-config/assets/24421979/827baf44-938f-41f8-bde8-b9356f75cd42)

Users are the people who submit tickets. They can be guests or registered accounts.

- Go to **Agent Panel → Users → Add New**
- Create example users:
  - Karen K
  - Ken Masters

---

## 7. Configure Service Level Agreements (SLAs)

![SLAs](https://github.com/LawrenceDavy/post-install-config/assets/24421979/0743ba13-0c03-4dd7-9631-b99be7824826)

SLAs define expected resolution times based on severity / business impact.

- Go to **Admin Panel → Manage → SLA**
- Create the following example SLAs:

| SLA     | Grace Period | Schedule       | Notes                          |
|---------|--------------|----------------|--------------------------------|
| SEV-A   | 1 hour       | 24/7           | Most severe / business critical |
| SEV-B   | 4 hours      | 24/7           | High priority                  |
| SEV-C   | 8 hours      | Business hours | Standard priority              |

---

## 8. Configure Help Topics

![Help Topics](https://github.com/LawrenceDavy/post-install-config/assets/24421979/b479c0db-9c08-4e34-a8f0-95e2baeb0dd7)

Help Topics categorise incoming tickets and can automatically route them to the correct department, apply an SLA, and set priority.

- Go to **Admin Panel → Manage → Help Topics**
- Create example topics:
  - Business Critical Outage
  - Personal Computer Issues
  - Equipment Request
  - Password Reset

---

## Next Steps

Continue to **Part 3 – Ticket Lifecycle** to walk through creating, updating, escalating and closing tickets:  
[https://github.com/LawrenceDavy/ticket-lifecycle](https://github.com/LawrenceDavy/ticket-lifecycle)

---

## Lessons Learned
- Clear role and department design makes permission management much simpler later.
- Setting a 24/7 schedule on the System Administrators department ensures emergency tickets can still be actioned outside normal hours.
- Matching Help Topics to SLAs and departments creates predictable routing and response expectations.
- Documenting each configuration step makes the system easier to hand over or rebuild.

---

**Last verified:** August 2026
