# SSH Brute Force Attack Analysis

## Objective

Demonstrate a brute force attack against an SSH service on port 22 in a controlled lab environment and analyze authentication security risks.

## Tools Used

* Kali Linux
* Hydra
* SSH Service
* Linux Terminal
* Target Virtual Machine

## Target Service

SSH (Secure Shell) — Port 22

The attack was performed only in a legal lab environment for security testing and educational purposes.

## Attack Flow

1. Identify target IP address
2. Verify open SSH port using Nmap
3. Confirm SSH service availability
4. Prepare username and password wordlists
5. Launch brute force attack using Hydra
6. Monitor authentication attempts
7. Detect successful credential match
8. Verify SSH access

## Example Commands

Port scanning:

nmap -p 22 <target_ip>

Brute force:

hydra -l root -P passwords.txt ssh://<target_ip>

## Impact

* Unauthorized remote access
* Credential compromise
* Privilege escalation
* Lateral movement
* Full system compromise

## Risk Level

High

## Indicators of Compromise

* Multiple failed SSH login attempts
* Repeated connections from one IP
* Successful login after many failures
* Unusual login times
* Suspicious auth.log entries

## Mitigation

* Disable password authentication
* Use SSH keys instead of passwords
* Fail2Ban protection
* Account lockout policy
* Strong password policy
* IP-based access restrictions

## Lessons Learned

SSH brute force attacks are common and dangerous when password authentication is weak.
Proper monitoring and key-based authentication significantly reduce the risk.
