## TASK - 1   [20-03-2026]
Create user called james with UID 1594 
```
sudo useradd -u 1594 james
```
and desginate home dir as /var/www/james
```
sudo usermod -d /var/www/james james

to verify:
grep james /etc/passwd
```

## TASK - 2   [20-03-2026]
Create group called nautilus_admin_users and assign user stark on group 
```
sudo groupadd nautilus_admin_users
```
and Assign user stark on group nautilus_admin_users
```
Create a user
sudo useradd stark

Assign user to Group
sudo usermod -aG nautilus_admin_users stark
```
## TASK - 3   [20-03-2026]
What xFusionCorp scenario is simulating:
* A backup agent needs to be installed on App Server 1. Before installing it, the sysadmin must create the OS identity it will run under — with no login access for security

Create a user mariyam with non-interactive shell access
```
sudo useradd -s /sbin/nologin mariyam

```
## TASK - 4   [21-03-2026]
Create a user without home dir 
```
sudo useradd -M rose
```

