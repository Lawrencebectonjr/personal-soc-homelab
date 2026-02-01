# SOC Home Lab: Network Connectivity Phase

## Objective
Establish and verify network visibility between the Windows Analysis Station (HP Laptop) and the Ubuntu Server (MacBook Pro).

## System Information
* **Windows Host (HP Laptop):** 192.123.0.!$%
* **Ubuntu Server (MacBook Pro):** 192.123.0.!@#
* **Default Gateway:** 192.123.0.$%#

## Progress Log

### 1. Identify Network Interfaces
* **Action:** Ran `ipconfig` on Windows to find the local IPv4 address.
* **Action:** Ran `ip a` on the Ubuntu Server.
* **Result:** Confirmed the Ubuntu Server is active on interface `wlp2s0` with IP `192.123.0.#@$`.

### 2. Connection Testing (ICMP)
* **Initial Attempt:** Failed due to syntax error (used `< >` brackets in PowerShell).
* **Correction:** Executed `ping 192.123.0.@#$` directly in PowerShell.
* **Verification:** Successful connectivity confirmed with 0% packet loss and an average round-trip time of 91ms.

## 3 - Technical Log: Secure Remote Access

### Connectivity Results
- **Ping Status:** Successful (Average 91ms)
- **SSH Service:** Active and Running (verified via `systemctl status ssh`)
- **Firewall Config:** UFW enabled; Port 22/TCP allowed for SSH

### Troubleshooting & Resolution
- **Issue:** 'Permission Denied' during initial SSH attempt.
- **Root Cause:** Attempted login using the system hostname (`klackplix`) as the user.
- **Resolution:** Corrected syntax to `ssh tarfear@192.123.0.!#@` using the proper account username. Connection successful.

### Maintenance Performed
- [x] Installed `ufw` and configured basic rules.
- [x] Initiated `apt upgrade` to resolve pending kernel version (6.8.0-94-generic).
- [x] Verified remote terminal control from HP Laptop to Ubuntu Server.


## Technical Summary
The lab environment is "alive." The Windows host can successfully route traffic to the Ubuntu target within the `192.123.0.0/24` subnet.

*IP and names have been slightly changed or altered to protect privacy.
