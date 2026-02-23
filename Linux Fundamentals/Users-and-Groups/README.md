# Users and Groups

- user info: tail -10 /etc/passwd
- user passwd: tail -5 /etc/shadow
- group info: tail -10 /etc/group
- group passwd: tail -10 /etc/gshadow

## Commands

Create user:
```
sudo useradd username
```
Create group:
```
sudo groupadd groupname
```
Add user to group:
```
sudo usermod -aG groupname username
```
Check groups:
```
groups username
```
Check current user:
```
whoami
```
## Example

Groups:
dev_team
hr_team
intern_team

Users:
dev1 → dev_team
dev2 → dev_team
hr1 → hr_team
intern1 → intern_team
