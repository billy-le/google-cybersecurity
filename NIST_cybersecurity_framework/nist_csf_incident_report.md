# Incident Report

## Summary

The company experienced a DDoS attack which compromised the internal network for two hours. The attack stopped our network services by flooding it with ICMP packets.

The cybersecurity team was able to block the incoming ICMP packets and stopping only non-critical network services while restoring critical network services. Upon investigation, the cybersecurity team found that the malicious attacker sent the ICMP packets through an unused port on our firewall which bypass our security.

To prevent from future attacks, the team add a new rule to rate limit the incoming ICMP packets and add a verification of said packets on the firewall. This ensure that the source IP is coming from a legitimate source and not being spoofed by the attacker.

Finally we add monitor capabilities for any unusual traffic and add an IDS/IPS system to alert and respond to any suspicious network requests.

## Identify

The team was able to identify the security gap in our router configuration. The attacker was able to send ICMP packets through one of the ports and gain access to our network.

## Protect

The team implemented new rules for the firewall to verify incoming requests to ensure they are coming from the source IP and not a spoof. They also implemented monitoring applications like IDP/IPS and networking logging to identify any potential threat or unusual traffic.

## Detect

To detect new threats, the team implemented IDP/IPS and network logging to see any spike in traffic or suspicious network activity

## Respond

The initial response to the attack was to block the IP address that was sending the ICMP packets. The next steps were to stop all non-critical network services and restoring critical network services. After the investigatation, we found security gaps in our firewall configuration and implemented new security measures to migate such an attack in the future.

To contain future incidents, the security team will routinely check firewall configuration and update them as needed. As new incidents happen, we plan to use the new monitoring tools to help identify threats more quickly and to restore network services. These same monitoring tools can help us find vulnerabilities in the system and update our security posture.

## Recover

The team was able to restore critical network services after blocking the IP address and stopping non-critical network services.
