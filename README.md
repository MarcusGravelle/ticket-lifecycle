<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle Examples</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket. It follows the lab checklist sequence (department prep, three test tickets, permissions behavior, and closeout). 


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10 Enterprise N (22H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake
- Assignment and Communication
- Working the Issue
- Resolution

<h2>Lifecycle Stages</h2>

<!-- 1) TICKET A: Intake + Sev-A triage -->

<p>
<strong>1) Intake – Business-Critical Outage (Ticket A):</strong><br/>
End-user submits: “<em>Online Banking System Outage</em>” at <code>http://localhost/osTicket</code>.<br/>
As Agent <em>john</em>, open the ticket in the Agent Panel and set properties: <strong>SLA = Sev-A (1 hour, 24/7)</strong>, <strong>Department = Online Banking</strong>, verify <em>Priority</em> and <em>Assigned To</em>. This classifies it as a critical outage. 
</p>
<p>
<img src="https://i.imgur.com/hu8Kyvh.png" height="80%" width="80%" alt="Ticket Creation by Karen"/>

Ticket submitted by Karen for Banking System Outage
  
<img src="https://i.imgur.com/LZ1e42c.png" height="80%" width="80%" alt="Ticket A intake and Sev-A triage"/>

Ticket is marked as Emergency to be fixed under an SLA of SEV-A

</p>
<br />

<!-- 2) TICKET B: Intake + Sev-B triage -->

<p>
<strong>2) Intake – Application Issue (Ticket B):</strong><br/>
End-user submits: “<em>=Accounting Department Software Failure</em>”.<br/>
As <em>Marcus</em>, set properties to: <strong>SLA = Sev-B (4 hours, 24/7)</strong>, <strong>Department = Support</strong>; verify priority/assignee. This is urgent but not a full outage. Work this ticket through to completion as <em>john</em>. 
</p>
<p>
<img src="https://i.imgur.com/4PpWB5M.png" height="80%" width="80%" alt="Ticket B intake and Sev-B triage"/>

Ticket Submitted by Ken for issue with Accounting Department

</p>
<br />

<!-- 3) TICKET C: Intake + Sev-B triage -->

<p>
<strong>3) Intake – Device Failure (Ticket C):</strong><br/>
End-user submits: “<em>CFO’s laptop will no longer turn on</em>”.<br/>
As <em>Marcus</em>, set properties to: <strong>SLA = Sev-C (8 hours, Weekdays)</strong>, <strong>Department = Support</strong>; verify priority/assignee. Work this ticket through to completion as <em>Marcus</em>. 
</p>
<p>
<img src="https://i.imgur.com/6hCk0cy.png" height="80%" width="80%" alt="Ticket C intake and Sev-C triage"/>

CFO Laptop Ticket Submitted by Ken, Updated to show SEV-C for Low Priority, Assigned to <em>Marcus</em>
  
</p>
<br />

<!-- 4) WORK TO COMPLETION: roles switch and closures -->

<p>
<strong>4) Work & Resolution:</strong><br/>
Process all Tickets to Completion. Use internal notes and public replies as needed; transition status from <em>Open</em> → <em>In Progress</em> → <strong>Closed</strong>. Confirm SLA targets are met (1-hour for Sev-A; 4-hour for Sev-B). Admin login: <code>http://localhost/osTicket/scp/login.php</code> · End-user portal: <code>http://localhost/osTicket</code>. 
</p>
<p>
<img src="https://i.imgur.com/hX26ZAh.png" height="80%" width="80%" alt="Closing SLA SEV-A"/>

Fix Found for SEV-A, pushed an update to customer and closed ticket

<img src="https://i.imgur.com/NvzU506.png" height="80%" width="80%" alt="Closing SLA SEV-B"/>

Fix Found for SEV-B, Updates pushed to employees that were missing Microsoft Print to PDF which is required for Visual C++

<img src="https://i.imgur.com/VymhvyZ.png" height="80%" width="80%" alt="Closing SLA SEV-C"/>

Fix Found for SEV-C, new power cable given to CFO. Laptop fully functional now.

<img src="https://i.imgur.com/Nd2s6Do.png" height="80%" width="80%" alt="All Tickets Closed"/>

All Tickets showing Closed in the osTicket System

</p>
<br />

<!-- 5) EMAIL BEHAVIOR -->

<p>
<strong>5) Soft Speaking and Customer Skills(Concept):</strong><br/>
In all Ticketing software and Help Desk/It Positions Soft Skills or Customer Service is needed for better experience on both Sides. 
</p>
<p>
<img src="https://i.imgur.com/NvzU506.png height="80%" width="80%" alt="SEV-B Fix"/>

Photo shows fix for Sev-B, tone is appropriate for speaking to the customer and is infomrative. It is pushing the customer away, but letting them know that their issue has been fixed.
  
</p>
<br />

<h2>End Result</h2>
This lab demonstrates a complete, working ticket workflow in osTicket—from intake to verified closure—running on an Azure-hosted Windows environment with IIS. Three representative incidents were created and triaged with the correct routing and SLAs, then worked to completion with clear agent communication and audit trails:

- **Sev-A (1 hour, 24/7)** — Business-critical outage (**Online Banking System Outage**) routed to **Support**, prioritized and resolved within target.
- **Sev-B (4 hours, 24/7)** — Department-level application issue (**Accounting export to PDF failing**) assigned to **Support**, corrected and communicated to affected users.
- **Sev-C (8 hours, business hours)** — Individual device failure (**CFO laptop won’t power on**) handled by **Support** with documented fix and closure.

Each ticket shows proper lifecycle transitions (**Open → In Progress → Closed**), appropriate **Department** and **SLA** application, and agent updates suitable for end-user communication. Final screenshots in the repository confirm creation, triage, and “All Tickets Closed,” demonstrating SLA compliance and a production-style help-desk workflow.

