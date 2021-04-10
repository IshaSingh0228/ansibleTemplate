Refer to this link for setting up
https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html

Create Windows VM with Containers AMI
Go to Security Groups and allow WinRM-HTTPS to Anywhere and save it.
Download the remote desktop file and open it through Remote desktop Connection App

Set-up inventory with user pass as done in this inventory.ini file
[window]
ec*-*-***-***-*.us-east-2.compute.amazonaws.com
[window:vars]
ansible_ssh_user = Administrator
ansible_ssh_pass = *****************
ansible_connection=winrm
ansible_winrm_server_cert_validation= ignore
ansible_winrm_transport = basic


Refer Site:
https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#winrm-setup

Run Get-Host on the node powershell as Admin
Name             : ConsoleHost
Version          : 5.1.17763.1490 (PowerShell version must be more than 3)



Refer File:
https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1
choose Raw and copy paste it into notepad.
Save the file as ConfigureRemotingForAnsible.ps1 in notepad type:All Files on Desktop
Run this command as it is
PS C:\Users\Administrator\Desktop> powershell.exe -ExecutionPolicy ByPass -File .\ConfigureRemotingForAnsible.ps1
Output:
Self-signed SSL certificate generated; thumbprint: 2DD7119D57B342068DCD50FD805F7C1BF1F35DBB

Lastly,
Run this command to check connection
ansible -i ~/project_winrm/inventory.ini window -m win_ping

Configuring IIS Server
Run ansible-playbook -i /home/ubuntu/project_winrm/inventory.ini iis_playbook.yml
and go to the instance 
open browser
put http://localhost
A Blue Server Screen will appear



