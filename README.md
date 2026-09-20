# Nmap Network Scanning & Reconnaissance

Authorized network reconnaissance and service enumeration performed against a Windows 11 VMware laboratory host using Nmap.

## Lab
- Kali Linux (scanner): 192.168.250.129
- Windows 11 (target): 192.168.250.128
- Network: VMware Host-only, 192.168.250.0/24

## Workflow
Host Discovery → Port Scanning → Service & Version Detection → OS Detection → NSE → Firewall/Filtering Detection → Final Report

## Key Results
| Port | State | Service |
|---|---|---|
| 135/tcp | Open | msrpc |
| 139/tcp | Open | netbios-ssn |
| 445/tcp | Open | microsoft-ds |
| 9468/tcp | Filtered | unknown |

Nmap strongly suggested Windows 11 at approximately 97% confidence, while warning that OS detection may be unreliable because no exact match was obtained.

Safe/default NSE results showed SMB dialects 2.0.2, 2.1, 3.0, 3.0.2 and 3.1.1, with SMB signing enabled and required. The ACK scan showed packet-filtering behavior on the tested ports.

## Evidence
See the `screenshots/` directory for the eight evidence captures.

## Disclaimer
This project was conducted only against an authorized VMware laboratory target. Do not scan systems you do not own or have explicit permission to test.
