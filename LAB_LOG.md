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

## Technical Summary
The lab environment is "alive." The Windows host can successfully route traffic to the Ubuntu target within the `192.123.0.0/24` subnet.

*IP has been slightly changed or altered to protect privacy.
