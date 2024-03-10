<h2>This part of the tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.</h2>

<br>
<br>

Note: Make sure you have logged in with your admin credentials before we continue

<hr>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/f48c50e0-dbe9-497b-84d9-78cff5350739)
- In helpdesk management, osTicket Roles play a pivotal role in streamlining operations. These roles are meticulously tailored sets of permissions, intricately woven to match the unique responsibilities of each employee.
- Configure Roles
  - Admin Panel --> Agents --> Roles
  - Supreme Admin 

<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/d0a03cce-bbd4-4428-bc62-bfe8ee5102d4)
- Each department serves as a distinct hub for handling specific types of inquiries. Additionally, administrators have the flexibility to fine-tune settings for individual departments. These configurations ensure efficient ticket management and streamlined workflows.
-  Creat a System Administration Department and assign yourself the manager. Provide the department with full control of the ticketing system. Set the schedule to 24/7 to allow access during non-operation hours, for emergencies.
- Configure Departments
  - Admin Panel --> Agents --> Departments
  - System Administrators 

<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/91b8033f-445c-4030-b0eb-945ba17f90d3)
- Teams organizes helpdesk employees from various departments enabling them to address specific issues or users via Help Topics or Ticket Filters.
- Configure Teams
  - Admin Panel --> Agents --> Teams
    - Level I Support
    - Level 2 Support    

<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/b6beddd4-8e82-4c1b-8f08-1bdac56d4771)
- Allow anyone to create tickets
  - Admin Panel --> Settings --> User Settings
  - Registration Required: Require registration and login to create tickets
<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/da9bde3c-1082-46d4-ac90-20c8cb75fef5)
- osTicket Agents serve as the frontline responders, addressing each ticket of user inquiries, ensuring timely resolutions and unwavering support.
- Configure Agents(Workers)
  - Admin Panel --> Agents --> Add New
    - Jane Jane
    - John John 
  
<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/827baf44-938f-41f8-bde8-b9356f75cd42)
- Helpdesk users are the organization's employees and/or customers who will be submitting tickets. Users can be guests or registered in osTicket. Registered users can login or use their email to track their ticket's progress and view submission history.
- Configure Users(customers)
  - Agent Panel --> Users --> Add New
    - Karen K
    - Ken Masters  
<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/0743ba13-0c03-4dd7-9631-b99be7824826)
- Service Level Agreements (SLAs) define the expected resolution time for tickets. Severity determines these timelines, reflecting the impact on business operations.
- In this example use service levels (severity) SEV-A, SEV-B, SEV-C with SEV-A being the most severe (impactful on business operations). For SEV-A I set a grace period for 1 hour, this indicates that the ticket must be closed within 1 hour of receving. I set the schedule to 24/7 allowing the ticket to be addressed after hours for emergencies.
- Configure SLA
  - Admin Panel --> Manage --> SLA
    - Sev-A (1 hour, 24/7)
    - Sev-B (4 hours, 24/7)
    - Sev-C (8 hours, business hours)

<hr>
<br>
<br>

![image](https://github.com/LawrenceDavy/post-install-config/assets/24421979/b479c0db-9c08-4e34-a8f0-95e2baeb0dd7)
Help Topics ensure Efficient Ticket Categorization. They serve as the compass in our ticketing system. They are used deftly guide tickets toward specific departments. Additionally, they influence ticket configurations, including SLAs and priority levels
- Configure Help Topics
  - Admin Panel -> Manage -> Help Topics
    - Business Critical Outage
    - Personal Computer Issues
    - Equipment Request
    - Password Reset

