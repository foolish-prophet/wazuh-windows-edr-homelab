# Wazuh Windows EDR Lab Setup

## Objective

The goal of this lab was to build a small Security Operations Center (SOC) environment using Wazuh SIEM to monitor Windows endpoint activity.

The project focused on endpoint telemetry collection, security event investigation, and SIEM alert tuning.

---

## Environment

### Virtualization

- VirtualBox

### Systems

| System | Purpose |
|---|---|
| Wazuh Manager | SIEM platform and alert management |
| Windows Server | Monitored endpoint |
| Sysmon | Endpoint telemetry collection |

---

## Implementation

### Wazuh Deployment

- Installed Wazuh Manager and Dashboard on Ubuntu
- Configured the Wazuh web interface
- Verified dashboard access

### Windows Endpoint Integration

- Installed Wazuh Agent on Windows Server
- Connected endpoint to Wazuh Manager
- Verified active agent communication

### Sysmon Integration

- Installed Sysmon on Windows Server
- Configured Wazuh Agent to collect Sysmon Operational logs

Collected telemetry included:

- Process creation events
- Registry changes
- Service activity
- Endpoint security events

---

## Testing Performed

### Authentication Monitoring

Generated failed login attempts and reviewed authentication activity in Wazuh.

Investigated Windows authentication events.

### User Account Testing

Created a temporary user account to generate security telemetry.

Verified event collection and removed the account after testing.

### Endpoint Detection

Generated endpoint activity and reviewed Sysmon-based detections.

---

## Alert Investigation

Investigated alerts including:

- Suspicious process activity
- Failed authentication attempts
- Service creation events

Performed false-positive analysis on legitimate Windows activity.

---

## SIEM Tuning

Reduced alert noise by tuning routine Windows events:

- Windows Logon Success
- Windows User Logoff

while maintaining visibility into authentication activity.

---

## Skills Demonstrated

- SIEM deployment
- Endpoint detection and response
- Windows security logging
- Sysmon configuration
- Alert triage
- False-positive investigation
- Detection tuning
