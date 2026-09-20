# Nmap Findings

## Scope
Target: 192.168.250.128 (Windows 11 VMware VM)

## Open/Filtered Ports
- 135/tcp — open — MSRPC
- 139/tcp — open — NetBIOS session service
- 445/tcp — open — SMB / Microsoft-DS
- 9468/tcp — filtered / unknown

## OS Detection
Nmap suggested Microsoft Windows 11 at approximately 97% confidence, but explicitly warned the OS result may be unreliable and no exact match was obtained.

## NSE
SMB dialects observed: 2.0.2, 2.1, 3.0, 3.0.2, 3.1.1.
SMB signing was reported as enabled and required.
Some scripts returned negotiation/execution errors; these are recorded as limitations rather than vulnerabilities.

## Firewall / Filtering
An ACK scan reported all tested ports as filtered, indicating packet-filtering behavior. The scan does not identify a specific firewall product.

## Conclusion
The assessment provides a baseline network attack-surface inventory for the authorized Windows lab target.
