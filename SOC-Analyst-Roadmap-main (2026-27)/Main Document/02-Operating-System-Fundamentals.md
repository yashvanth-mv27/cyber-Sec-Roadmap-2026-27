# <span style="color:#00C2FF">02. Operating System Fundamentals</span>

> Windows, Linux, Unix, macOS, and server admin fundamentals for SOC and blue team operations.

## <span style="color:#32D74B">Overview</span>

Operating systems are the runtime environment for enterprise workloads, user access, process execution, and telemetry generation. Security teams need strong OS fundamentals to interpret logs, hunt for malicious behaviors, and investigate endpoint activity.

---

## <span style="color:#FFB000">Windows Fundamentals</span>

### Kernel
The Windows kernel manages process scheduling, memory, hardware access, and system services.

### Processes
A process is an executing program; SOC analysts investigate parent-child relationships and suspicious command execution.

### Services
Windows services run in the background and can be started by the OS, by drivers, or by administrators.

### Registry
The Registry stores system and application configuration, often relevant in persistence and autorun investigations.

### Task Scheduler
Used to execute tasks at a scheduled time or after triggers. Common for persistence and execution abuse.

### Event Logs
Windows logs provide rich security and operational telemetry.

### PowerShell
PowerShell is used for automation and remediation but also frequently abused by attackers for execution and discovery.

### WMI
Windows Management Instrumentation is used for remote system management, often abused for persistence and execution.

### Sysmon
Sysmon captures process creation, network connections, and file creation events for deep endpoint visibility.

### Windows Defender
Endpoint protection with antivirus, exploit mitigation, and attack surface reduction.

---

## <span style="color:#FF5F57">Windows Event IDs</span>

| Event ID | Meaning | Detection opportunities |
|---|---|---|
| 4624 | Successful logon | New logons, impossible travel, service logons |
| 4625 | Failed logon | Brute force, password spraying |
| 4672 | Special privileges assigned | Privilege escalation, admin activity |
| 4688 | Process creation | Malware execution, script abuse |
| 4697 | Service installed | Persistence via new service |
| 4720 | Account created | New user creation or lateral movement |
| 4728 | Member added to security enabled global group | Privilege escalation via group changes |
| 4740 | User account lockout | Bruteforce detection |
| 4768 | Kerberos authentication ticket requested | Kerberos abuse, golden ticket suspicion |
| 4769 | Kerberos service ticket requested | Service ticket abuse, lateral movement |
| 4771 | Kerberos pre-authentication failed | Password spraying, brute force |
| 4776 | Credential validation | NTLM logon patterns, suspicious access |
| 5136 | Directory service changed | GPO or AD object changes |

### Hunting opportunities
- Review unusual parent-child process chains in 4688
- Look for suspicious service creation events 4697
- Correlate 4624 and 4672 for admin logons
- Investigate unusual DC authentication events 4768/4769
- Hunt impossible logon sequences and multiple failed attempts using 4625 and 4771

---

## <span style="color:#7C3AED">Linux Fundamentals</span>

### Kernel
The Linux kernel handles hardware communication, process scheduling, device I/O, and security enforcement.

### Processes
Processes are scheduled by the kernel; anomalies include unexpected shell spawning, hidden processes, or unusual network consumers.

### Users and permissions
Linux relies on users, groups, and permission bits to enforce access control.

### sudo
Allows administrative commands with restricted privilege escalation.

### iptables
Packet filtering firewall for Linux.

### systemd
System initialization and service manager for modern Linux distributions.

### cron
Scheduled tasks used for automation and sometimes for persistence.

### auditd
Kernel-level auditing used to track access and configuration changes.

### SELinux
Mandatory access control that restricts process and file access beyond standard Unix permissions.

---

## <span style="color:#00D4AA">Linux Logs</span>

- auth.log: authentication and authorization activity
- syslog: general system events
- messages: operational system messages
- secure: authentication logs and sudo activity
- audit.log: auditd output for changes and access events

### SOC use
Review failed SSH logins, privilege changes, scheduled job executions, and file access anomalies.

---

## <span style="color:#FFB000">Unix and macOS</span>

### Unix
Used in enterprise servers, containers, and appliances. Security teams review service startup, permission models, and file integrity.

### macOS
Focus on MDM, Gatekeeper, SIP, launchd, and endpoint telemetry. Apple endpoint logs are often correlated with EDR data.

### Windows Server
Handles AD, file services, DNS, DHCP, and enterprise identity infrastructure.

---

## <span style="color:#32D74B">System Administration Concepts</span>

- User and group management
- Service configuration and startup
- Patching and maintenance
- Backup and retention
- Monitoring and log collection
- Hardening baselines
- Access controls and least privilege

### Detection considerations
- Baseline changes in startup configs
- Unexpected privileged users
- Service tampering
- Network port changes
- Sensitive file modifications

---

## <span style="color:#FF5F57">Threat Hunting Ideas</span>

- Hunt for suspicious PowerShell execution on Windows
- Review SSH login anomalies and sudo usage on Linux
- Check service creation and startup script changes
- Review scheduled tasks, regsvr32 use, and WMI persistence
- Validate process lineage from parent to child execution

---

## <span style="color:#7C3AED">Interview Questions</span>

- What is the difference between a process and a service?
- How does Windows security auditing help SOC investigations?
- What is the purpose of SELinux or AppArmor?
- Why are scheduled tasks relevant in endpoint forensics?
- How do Linux permissions differ from Windows ACLs?

---

## <span style="color:#00C2FF">Conclusion</span>

Strong OS skills are essential for security investigation. Analysts need to know how processes, users, services, permissions, and logs behave in normal and abnormal situations to distinguish malicious activity from routine administration.
