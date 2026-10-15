# Security Audit Report

## The Principle of Least Privilege (PoLP)
The Principle of Least Privilege holds that any user, program, or process should receive only the permissions required to perform its task, and no more. This matters for cloud user accounts because a compromised account can only do as much harm as its permissions allow. When access is tightly limited, one breach is far less likely to escalate into a total system compromise.

## Attack Surface
The attack surface of a virtual machine is the sum of all the places an unauthorized person might try to break in. Open ports, running services, installed packages, and user accounts each add to it. Because a smaller surface gives attackers fewer chances to find a weakness, hardening a server means turning off or removing everything that isn't absolutely needed.

## Default Deny Policy
A default deny policy blocks all traffic unless it is specifically permitted, allowing only connections known to be necessary. This beats trying to block bad actors one by one, since no one can anticipate every malicious IP address or attack method ahead of time. By treating all traffic as untrusted until it is proven safe, the policy shuts out unknown and future threats instead of having to respond to each one after it appears.
