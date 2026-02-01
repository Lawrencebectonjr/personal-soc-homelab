# Phase 4: Logging & Visibility

## Objective
To observe real-time authentication logs on the Ubuntu server when accessed via SSH from a remote host (HP Laptop).

## Technical Tasks
* [x] Establish SSH connectivity
* [x] Identify high-value SOC logs (`/var/log/auth.log`)
* [x] Observe real-time authentication events

## Evidence
### 1. SSH Attempt
I initiated an SSH connection from my HP laptop to the server.
![SSH Attempt](docs/assets/ssh_ss.png)

### 2. Auth Log Entry
Using `tail -f /var/log/auth.log`, I captured the following event:
![Auth Log Detection](docs/assets/auth_ss.png)

