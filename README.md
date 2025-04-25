<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

### 📍 [Part 1: Prerequisites & osTicket Installation](https://github.com/derickayala25/osticket-prereqs)
### 👉 Part 2: Post-Installation Configuration
### 👉 [Part 3: Ticket Lifecycle Demo](https://github.com/derickayala25/ticket-lifecycle)

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=o-YBDTqX_ZU)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket (Help Desk Customer Support Software)

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)

<h2>Installation Steps</h2>

<br/>

<b>Acknowledge Agent and Admin panels</b><br/>
Once you log in to osTicket there are two panels which you can work in: Agent Panel and Admin Panel. You'll know which panel you're in by looking at the top right of the browser tab.
If you see Admin Panel, then you're in the Agent Panel. If you see Agent Panel, then you're in the Admin Panel.</br>

If you log in as the Administrator (instead of as an Agent), the Agent panel is for viewing and working on tickets as an Agent. In this panel you're not able to do administrative changes as in resetting passwords, adding new users, etc.

In the Admin panel, however, you have access to back-end configuration options. You can adjust system settings, add permissions, set up teams, roles, etc.

It basically breaks down as Agents have Roles (and permissions associated with those roles), Agents can be part of a Team, and a Team will be 
part of a Department or Departments.

<p>
<img src="https://github.com/user-attachments/assets/1d8f20ca-8fa4-4d8f-81da-4f3903331035" height="80%" width="80%" alt="Agent Panel"/>
</p>

<p>
<img src="https://github.com/user-attachments/assets/b09f55c9-ca4e-4f3f-9417-52bddcdd99ca" height="80%" width="80%" alt="Admin Panel"/>
</p><br/>


<b>Default Roles in osTicket</b></br>
The default Roles that come with osTicket are <b>View only</b>, <b>Limited Access</b>, <b>Expanded Access</b>, and <b>All Access</b>. You can find these roles with their assigned permissions by going to the <b>Admin Panel</b>, clicking on the <b>Agents</b> tab and clicking on <b>Roles</b>. You can also create new roles with their own custom permissions. 

<p>
<img src="https://github.com/user-attachments/assets/ef9863f4-83d2-4bbc-a9ea-5c76b1cbd208" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Default Departments in osTicket</b></br>
Default <b>Parent</b> departments that appear in osTicket are <b>Top Level Department</b>, <b>Maintenance</b>, and <b>Support</b>. You can give the same level of access to the whole <b>Department</b> or give each individual <b>Agent</b> different access permissions. If you choose <b>Top Level Department</b> as the <b>Parent</b> Department, then the new <b>Department</b> you create will be itself become a <b>Parent</b> Department.

<p>
<img src="https://github.com/user-attachments/assets/5a6c3b14-a787-4702-a786-30b656134ccf" height="80%" width="80%" alt="Default Roles"/>
</p><br/>

<b>Adding a new Department</b></br>
Let's create a new Department called <b>SysAdmins</b>. We'll have the <b>Top Level Department</b> as it's <b>Parent</b> and we'll leave the rest of the default settings as is.
1. In the <b>Admin Panel</b>, navigate to <b>Agents</b> > <b>Departments</b>.
2. Click on `(+) Add New Department`
3. Type <b>SysAdmins</b> in the <b>Name:</b> box
4. Click the `Create Dept` button at the bottom

<p>
<img src="https://github.com/user-attachments/assets/541f2c7e-645e-4e96-88d3-8559ae963d10" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Default Teams in osTicket</b></br>
Teams allow you to pull Agents from different Departments and organize them to handle a specific issue.

The default Team in osTicket is <b>Level 1 Support</b>. You can select a <b>Team</b> Lead and individual <b>Agent</b> members.

<p>
<img src="https://github.com/user-attachments/assets/899d6407-9273-481f-ac4b-7477f7afe832" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Adding a new Team</b></br>
We'll create two new teams. The first will be called <b>Online Banking</b> and the second will be <b>In-House Systems</b>.
1. In the <b>Admin Panel</b>, navigate to <b>Agents</b> > <b>Teams</b>
2. Click on `(+) Add New Team`
3. Type <b>Online Banking</b> in the <b>Name:</b> box
4. Click the `Create Team` button at the bottom
5. Follow the same steps for the <b>In-House Systems</b> team.

<p>
<img src="https://github.com/user-attachments/assets/67d31570-1870-4a35-95c0-20d0695ab236" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Allowing end users to create tickets</b></br>
osTicket, by default, allows any end user to create tickets. However, if we want to make changes to those permissions, we can follow these steps:
1. In the <b>Admin Panel</b>, go to <b>Settings</b> > <b>Users</b>
2. In the <b>Authentication Settings</b> area, make any desired updates.

<p>
<img src="https://github.com/user-attachments/assets/1ca59603-d4e1-48af-acf0-8e39e3df6694" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Configuring Agents</b></br>
Next, we'll configure Agents. These are the actual workers/employees.
1. In the <b>Admin Panel</b>, go to <b>Agents</b>
2. Click on `(+) Add New Agent`
3. Once there, required fields are <b>First</b> and <b>Last Name</b>, <b>Email Address</b>, <b>Username</b>, <b>Primary Department</b> and <b>Role</b> (in the <b>Access</b> tab).
4. You can also set a password and assign a team. For this example, the password will be <b>Password1</b> for both agents.
5. For this example, the agent will be Jane Doe, her email is jane@newcompany.com and she's part of the <b>SysAdmins</b> department. Her role has <b>Expanded Access</b> and she's also part of the <b>Online Banking</b> team.
6. To set her password, click on the `Set Password` button. Uncheck the <b>Send the agent a password reset email</b> box, enter the password and confirm, uncheck the <b>Require password change at next login</b> box, and click on `Set`.
7. Once done, click the `Create` button at the bottom
8. We'll also add John Doe as a New Agent. He will also be part of the <b>SysAdmins</b> department. His role has <b>Expanded Access</b> and he's part of the <b>In-House Systems</b> team.

<p>
<img src="https://github.com/user-attachments/assets/12b0d4ab-d821-4981-a76f-3030f7ee4e17" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Configuring End Users</b></br>
Next, we'll configure an end user. These are the people requesting the services, the customers.
1. In the <b>Agent Panel</b>, go to <b>Users</b> > <b>Add User</b>
2. Required fields are <b>Email Address</b> and <b>Full Name</b>. This user will be Karen at karen@enduser.com.
3. Click on the `Add User` button

<p>
<img src="https://github.com/user-attachments/assets/ce47116b-d8e2-4086-a357-26f0ff38728f" height="80%" width="80%" alt="Default Roles"/>
</p><br/>

<b>Configuring Service Level Agreements</b></br>
Now, we'll configure some Service Level Agreements (SLA). This is a formal contract between a service provider and a customer 
that defines the expected level of service, including specific metrics, responsibilities, and remedies if service levels are not met. 
The osTicket Default SLA has an 18 hour grace period. However, you can add new SLAs. To do this:
1. Go to the <b>Admin Panel</b> > <b>Manage</b> > <b>SLA</b> > <b>Add New SLA Plan</b>.
2. We'll <b>Name</b> the first SLA <em>Sev-A</em>, give it a <b>Grace Period</b> of 1 hour and put it under a 24/7 <b>Schedule</b>.
3. Click on the `Add Plan` button.
4. The second one we'll <b>Name</b> Sev-B. This one will have a <b>Grace Period</b> of 4 hours and will also have a 24/7 <b>Schedule</b>.
5. The third one we'll <b>Name</b> Sev-C and give it an 8 hour <b>Grace Period</b> and a Business Hours <b>Schedule</b>.

<p>
<img src="https://github.com/user-attachments/assets/971f929a-1f37-4026-88b5-b188215fedf1" height="80%" width="80%" alt="Default Roles"/>
</p><br/>


<b>Configuring Help Topics</b></br>
Next, we'll configure Help Topics. Help Topics guide what information is gathered from Users and how tickets are routed or assigned. 
You can assign a specific department to handle a topic, add SLAs, etc. osTicket already has five <b>Parent Topics</b> built in.
For this example, we'll add five Help Topics and associate each with a Parent Topic. To do this:
1. Go to the <b>Admin Panel</b> > <b>Manage</b> > <b>Help Topics</b> > <b>Add New Help Topic</b>.
2. We'll name the first <b>Topic</b> <em>Business Critical Outage</em> and assign it's <b>Parent Topic</b> as <em>Report a Problem</em>.
3. Click on the `Add Topic` button. Click on the <b>Help Topics</b> tab again.
4. The second <b>Topic</b> will be <em>Personal Computer Issues</em> and the <b>Parent Topic</b> will also be <em>Report a Problem</em>.
5. The third <b>Topic</b> will be <em>Equipment Request</em> with <b>Parent Topic</b> <em>General Inquiry</em>.
6. The fourth <b>Topic</b> will be <em>Password Reset</em> and we'll assign it to <em>Report a Problem/Access Issue</em>.
7. The last <b>Topic</b> that we'll add is <em>Other</em> and we'll assign it to <em>General Inquiry</em>.
8. Please note that when you add a topic, the topic itself (along with it's <b>Parent Topic</b>) will become available as a <b>Parent Topic</b> when you're ready to add the next topic.

<p>
<img src="https://github.com/user-attachments/assets/ee4bb690-8a6b-4502-85c1-261ab5815cb3" height="80%" width="80%" alt="Default Roles"/>
</p><br/>

### 📍 [Part 1: Prerequisites & osTicket Installation](https://github.com/derickayala25/osticket-prereqs)
### 👉 Part 2: Post-Installation Configuration
### 👉 [Part 3: Ticket Lifecycle Demo](https://github.com/derickayala25/ticket-lifecycle)

