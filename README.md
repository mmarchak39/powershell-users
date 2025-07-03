<p align="center">
<img src="https://github.com/user-attachments/assets/ea48681b-e330-4e26-b5a3-77b44a0e354c"/>
</p>

<h1>PowerShell - User creation and managment</h1>
This tutorial outlines the creation and manegment of Local User Accounts with PowerShell.<br />


<h2>Environments and Technologies Used</h2>

- PowerShell

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)


<h2>Example User Managment</h2>


<p>
<img src="https://github.com/user-attachments/assets/72c20e40-e5bd-4dfa-99d1-35a90f019ec8"/>
</p>
<p>
To create or manage a new local user you will first need to open PowerShell with administrative privileges.
search for 'PowerShell' in the Start menu, then either right-click and choose "Run as Administrator" or select "Run as Administrator" when viewing Powershell within start menu.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/2583f27e-8a89-4e0f-9100-a7ed6322ea44"/>
</p>
<p>
To create a new User I'm using "the New-LocalUser" command with some additional parameters in addition to example names, description, and password:

"-Name" is the username. "User1"

"-FullName" is the display name. "John-Doe"

"-Description" allows you to leave a note. "Created for testing"

"-Password" I’m additionally using "Read-Host -AsSecureString" this will let you create the User without showing the typed password on screen.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/821020c5-ce5b-4675-ac93-3844ecb98ca1"/>
</p>
<p>
After creating a Password and hitting Enter, the user gets created locally on this machine.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/6007f2e9-5f89-4c21-b307-a4802180bba3"/>
</p>
<p>
We can use the "Get-LocalUser" command to verify the account was successfully created. This allows you to view all user accounts, including system accounts and any others created manually.
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/b994d932-7ad2-4b4b-a12b-db52a154ee3e"/>
</p>
<p>
By default, new local users don’t have admin rights. By using the "Add-LocalGroupMember" command followed by "Group "Administrators" -Member" and then the user (In this case User1) we can add the Local User to the Administrators group.
</p>
<br />



<p>
<img src="https://github.com/user-attachments/assets/93fb6342-6563-4e49-8c35-64d288f68ee7"/>
</p>
<p>
If you no longer want a local user to have access to the system you can disable the account, this prevents them from logging in but will keep their data.
Using the "Disable-LocalUser" Command followed by -Name and then the name of the local user you want to disable (In this case User1) you can disable the User. Using the "Get-LocalUser" Command you can verify the account is no longer enabled. 
</p>
<br />


<p>
<img src="https://github.com/user-attachments/assets/ed14fb5f-83ea-404b-8264-97b19908ff6f"/>
</p>
<p>
If you no longer want the user to be on the system you can use the "Remove-LocalUser." command followed by "-Name" and then the User you want to remove (In this case User1) to remove them entirely including all of their data. Using the "Get-LocalUser" command we can see that "User1" is no longer listed in the systems local users.
</p>
<br />

