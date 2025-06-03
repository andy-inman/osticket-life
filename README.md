<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake Through Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Lifecycle Stages</h2>

<p>
<img src="https://i.imgur.com/NnJJak1.png" height="80%" width="80%" alt="Ticket Intake"/>
</p>
<p>
<b>Intake:</b><br />
The end-user <i>Karen</i> logs into the portal at <code>http://localhost/osTicket</code> and creates a new ticket with the following details:
<ul>
  <li><b>Help Topic:</b> Business Critical Outage</li>
  <li><b>Subject:</b> Mobile/Online Banking Down</li>
  <li><b>Message:</b> The entire mobile and online banking system is currently unavailable. Customers are unable to log in or perform transactions.</li>
  <li><b>Email:</b> karen@example.com</li>
</ul>
The ticket is now in the system with default properties.
</p>
<br />

<p>
<img src="https://i.imgur.com/5xyZsFM.png" height="80%" width="80%" alt="Ticket Assignment"/>
</p>
<p>
<b>Assignment & Communication:</b><br />
Help Desk Agent <i>John</i> logs in at <code>http://localhost/osTicket/scp/login.php</code> and opens the unassigned ticket queue. He locates Karen’s ticket and observes:
<ul>
  <li><b>Priority:</b> Normal (default)</li>
  <li><b>Department:</b> Help Desk (default)</li>
  <li><b>SLA:</b> None</li>
  <li><b>Assigned To:</b> Unassigned</li>
</ul>

John updates the ticket properties as follows:
<ul>
  <li><b>Department:</b> Online Banking</li>
  <li><b>SLA Plan:</b> Sev-A (1 hour, 24/7)</li>
  <li><b>Assigned To:</b> Jane (SysAdmin)</li>
</ul>

Because the department is now Online Banking and John is not a member, he loses visibility to the ticket.
</p>
<br />

<p>
<img src="https://i.imgur.com/P1rzfz9.png" height="80%" width="80%" alt="Working the Issue"/>
</p>
<p>
<b>Working the Issue:</b><br />
SysAdmin <i>Jane</i> logs in and accesses the reassigned ticket. She investigates the issue:
<ul>
  <li>Checks system logs for service downtime</li>
  <li>Restarts online banking backend services</li>
  <li>Verifies public-facing service availability</li>
</ul>
Jane posts an internal note:
<pre>
Restarted the banking servers and validated external connectivity. Service appears stable now.
</pre>
She then resolves the ticket.
</p>
<br />

<p>
<b>Resolution:</b><br />
Karen receives a notification via email (assuming email is configured):
<pre>
Your support ticket regarding the online banking outage has been resolved.
Please try again and let us know if the issue persists.
</pre>

The issue has been successfully resolved end-to-end.
</p>
<br />

<h2>Additional Notes</h2>

- osTicket supports real-time notifications via email for every ticket update, reply, and status change.
- Tickets can come in through various channels: email, web form, phone, chat apps, or even informal in-person requests.
- Best practice in IT support is to log every issue, even if resolved quickly, to ensure metrics and workload tracking are accurate.
