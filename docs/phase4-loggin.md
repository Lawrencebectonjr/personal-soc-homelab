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

Observed real-time authentication logging via `/var/log/auth.log`.

Confirmed:
- SSH login attempts are logged
- Timestamped entries
- User attribution

This establishes baseline host-level visibility.

Actions Performed
Verified system logging service (rsyslog) was active on the Ubuntu server.


Identified high-value log files used in SOC operations, specifically:


/var/log/auth.log


/var/log/syslog


Enabled live log monitoring using tail -f on authentication logs.


Initiated an SSH connection from the HP laptop to the Ubuntu server.


Observed real-time log entries corresponding to the SSH authentication attempt.



Evidence Observed
SSH login attempts generated immediate log entries in /var/log/auth.log


Logs included:


Timestamp


Source IP address


Username


Authentication status


Confirmed correlation between user action and log telemetry



Outcome
This phase confirms:
Host-based logging is enabled and functioning


Authentication activity is observable in real time


The Ubuntu server provides reliable telemetry for security monitoring


This establishes a baseline for future detection and alerting activities.

Phase Status
✅ Completed

Establish host-level visibility by monitoring authentication activity in real time and validating that system logs accurately reflect user actions.
---

### **Actions Performed**
1. **Verified Service:** Confirmed the system logging service (`rsyslog`) was active on the Ubuntu server.
2. **Identified SOC Logs:** Located high-value log files used in SOC operations:
    * `/var/log/auth.log` (SSH logins, sudo attempts)
    * `/var/log/syslog` (General system activity)
3. **Live Monitoring:** Enabled live log monitoring using `tail -f` on authentication logs.
4. **Initiated Connection:** Performed an SSH connection from the HP laptop to the Ubuntu server.
5. **Real-Time Observation:** Observed log entries corresponding to the SSH authentication attempt as they happened.

---

### **Evidence Observed**
* **Immediate Generation:** SSH login attempts generated immediate log entries in `/var/log/auth.log`.
* **Telemetry Data:** Logs successfully captured:
    * Timestamp
    * Source IP address
    * Username
    * Authentication status
* **Correlation:** Confirmed direct correlation between user action and log telemetry.

---

### **Outcome**
This phase confirms:
* **Host-based logging** is enabled and functioning.
* **Authentication activity** is observable in real time.
* **Telemetry reliability:** The Ubuntu server provides reliable telemetry for security monitoring.

This establishes a baseline for future detection and alerting activities.

---

### **Phase Status**
✅ **Completed**


