# active-directory-home-lab
> From Zero to Helpdesk Ready: Building lab.local on Windows Server 2022

### Why I built this
I was tired of just watching YouTube on AD. So I decided to break my own VirtualBox before I break production.

### Lab Setup
- **Host:** VirtualBox 7.0
- **Server:** Windows Server 2022 - lab.local

### Day 1 - What I Built
- OU Structure: Lagos-Branch, Human Resources, Information Technology
- User: Tunde Adekunle (tunde.adekunle) inside HR OU
- Group: HR-Team

### Day 2 - Real Helpdesk Tasks
1. Disabled & Enabled account (leave/return scenario)
2. Password Reset to P@ssw0rd123! + "User must change password at next logon"
3. Account Unlock after 5 failed attempts
4. 8-char minimum policy

### PowerShell Commands
```powershell
Disable-ADAccount -Identity "Tunde Adekunle"
Enable-ADAccount -Identity "Tunde Adekunle"
Set-ADAccountPassword -Identity "Tunde Adekunle" -Reset
Unlock-ADAccount -Identity "Tunde Adekunle"
Get-ADUser -Identity "Tunde Adekunle"
