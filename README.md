<p align="center">
<img src="https://github.com/user-attachments/assets/ea48681b-e330-4e26-b5a3-77b44a0e354c"/>
</p>

<h1>PowerShell - Prerequisites and Installation</h1>
This tutorial outlines the creation and manegment of Local User Accounts with PowerShell.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>


<p>
<img src="https://github.com/user-attachments/assets/72c20e40-e5bd-4dfa-99d1-35a90f019ec8"/>
</p>
<p>
"To begin, we need to open PowerShell with administrative privileges. This is important because creating or managing user accounts requires elevated permissions.
I search for 'PowerShell' in the Start menu, then right-click and choose 'Run as Administrator'.
Once PowerShell opens, you’ll see 'Administrator:' in the window title, which confirms we're running with the correct access level."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2583f27e-8a89-4e0f-9100-a7ed6322ea44"/>
</p>
<p>
*"Now I’ll create a new user account called 'TestUser1'.
Here, I'm using the New-LocalUser command with a few parameters:

-Name is the username.

-FullName is the display name for clarity.

-Description lets me leave a note, useful for documentation.

For the password, I’m using Read-Host -AsSecureString to securely prompt me without showing the typed password on screen.
Once I hit Enter, the user gets created locally on this machine."*
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/8305c8e2-1cf8-42f6-841e-e37adc74de02"/>
</p>
<p>
For the password, I’m using Read-Host -AsSecureString to securely prompt me without showing the typed password on screen.
Once I hit Enter, the user gets created locally on this machine."*
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/821020c5-ce5b-4675-ac93-3844ecb98ca1"/>
</p>
<p>
"By default, new local users don’t have admin rights.
If I want this user to have administrative permissions, I need to add them to the 'Administrators' group.
This is done using the Add-LocalGroupMember command.
In this case, I'm adding our new user 'TestUser1' to the 'Administrators' group.
Always use caution when giving admin rights — only do this for trusted or necessary accounts."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/b994d932-7ad2-4b4b-a12b-db52a154ee3e"/>
</p>
<p>
"By default, new local users don’t have admin rights. If I want this user to have administrative permissions, I need to add them to the 'Administrators' group. This is done using the Add-LocalGroupMember command. In this case, I'm adding our new user 'TestUser1' to the 'Administrators' group. Always use caution when giving admin rights — only do this for trusted or necessary accounts."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/6007f2e9-5f89-4c21-b307-a4802180bba3"/>
</p>
<p>
"To confirm that the new user was successfully created, I can list all local users on the system using the Get-LocalUser command. This outputs all user accounts, including system accounts and any others created manually. I can clearly see 'TestUser1' in the list now, which tells me the creation was successful."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/93fb6342-6563-4e49-8c35-64d288f68ee7"/>
</p>
<p>
"If I no longer want this user to have access, I have two options:
I can disable the account, which prevents them from logging in but keeps their data.
Or I can remove the user entirely, which deletes the account from the system.
Here, I’ll first show how to disable the user with Disable-LocalUser, then how to remove them with Remove-LocalUser."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ed14fb5f-83ea-404b-8264-97b19908ff6f"/>
</p>
<p>
"If I no longer want this user to have access, I have two options:
I can disable the account, which prevents them from logging in but keeps their data.
Or I can remove the user entirely, which deletes the account from the system.
Here, I’ll first show how to disable the user with Disable-LocalUser, then how to remove them with Remove-LocalUser."
</p>
<br />

