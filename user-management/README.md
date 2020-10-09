# user-management

Some basic Ansible playbooks to manage local users across any number of servers:

Playbooks to do:

- Add/delete users
- Lock/unlock users
- Add ssh key pairs
- Add authorized_key files
- Add users to /etc/sudoers file

> **_NOTE:_**  The expect script ```expect-deploying-initial-user-without-ansible``` is exactly that. When you have a new deployed system on your network, this system must have an ssh user with escalated priveleges in order for the Ansible Control Node / Tower to connect and execute playbooks. This pushes out the pubkey to the deployed server and creates an ```~/.ssh/authorized_keys``` in order to allow Ansible to connect. **Recommendation:** Use  `create-account.yml` as an example to fix your ansible user's account (such as .ssh permissions, etc.).
