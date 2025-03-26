<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Learn to Configure Roles, Departments, and Teams
- Learn to Configure Agents (workers)
- Learn to Configure Users (customers)
- Creating SLA (Service Level Agreements)
- Creating and Editing Help Topics

<h2>Configuration Steps</h2>

Admin/Analyst Login Page:
http://localhost/osTicket/scp/login.php 

End Users osTicket URL:
http://localhost/osTicket 


<p>
<img src="https://i.imgur.com/F3SS37p.png"/>
</p>
<p>
Configure Roles (for grouping permissions)
  
Admin Panel -> Agents -> Roles -> Add New Role

Name it "Supreme Admin" and check mark all options under the "Permissions" Tab and create the new role.
</p>
<br />

<p>
<img src="https://i.imgur.com/sdgJqJL.png"/>
</p>
<p>
Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
  
Admin Panel -> Agents -> Departments -> Add New Department

Parent: Top Level Department

Name: SysAdmins
</p>
<br />

<p>
<img src="https://i.imgur.com/iYDcAEw.png"/>
</p>
<p>
Configure Teams
  
Admin Panel -> Agents -> Teams (Pull Agents from different Departments) -> Add New Team

Name: Online Banking

Can add agents when needed.

</p>
<br />

<p>
<img src="https://i.imgur.com/n4EjxeS.png"/>
</p>
<p>
Allow anyone to create tickets
  
Admin Panel -> Settings -> User Settings

Make sure this box is UNCHECKED = Registration Required: Require registration and login to create tickets 

</p>
<br />

<p>
<img src="https://i.imgur.com/nbluJzH.png"/>
<img src="https://i.imgur.com/99vO6h7.png"/>
<img src="https://i.imgur.com/6ppqhV1.png"/>
  
</p>
<p>
Configure Agents (workers)
  
Admin Panel -> Agents -> Add New

Jane (Dept: SysAdmins, Role: Supreme Admin, Team: Online Banking)

Fill out the name, email, and Username. Click "Set Password" to configure password settings (Uncheck box and password options will pop up, and also uncheck "Require password change at next login"). Next, go to the "Access" tab and give the proper department and role to the agent. The "Permissions" tab should have all boxes checkmarked since a SysAdmin is being created.


Do the same process for the next agent:

John (Dept: Support, Role: View Only)

</p>
<br />

<p>
<img src="https://i.imgur.com/UqMf06Q.png"/>
</p>
<p>
  
Agent Panel -> Users -> Add New

Configure Users (customers) for the following:

Karen

Ken

</p>
<br />

<p>
<img src="https://i.imgur.com/0GdTYG0.png"/>
</p>
<p>
  
Admin Panel -> Manage -> SLA

Configure SLA for the following:
  
Sev-A (Grace Period: 1 hour, Schedule: 24/7)

Sev-B (Grace Period: 4 hours, Schedule: 24/7)

Sev-C (Grace Period: 8 hours, Business Hours)

</p>
<br />

<p>
<img src="https://i.imgur.com/vc7DbfU.png"/>
</p>
<p>
  
Admin Panel -> Manage -> Help Topics

Configure Help Topics (For when users create a ticket) for the following:

Business Critical Outage

Personal Computer Issues

Equipment Request

Password Reset

Other

</p>
<br />
