# mini-SOC-Splunk-Lab
# Mini-SOC Lab: Brute-Force Attack Detection with Splunk

## Objective
The goal of this project was to build a functional Mini Security Operations Center (SOC) to gain hands-on experience with SIEM engineering, log analysis, and incident response. 

## Tools & Environment
* **SIEM:** Splunk Enterprise
* **Attacker System:** Kali Linux (Hydra)
* **Target System:** Red Hat Enterprise Linux (RHEL)
* **Network:** Virtual Bridged Network

## Methodology
1. **Infrastructure Setup:** Deployed a RHEL server and configured the local firewall to allow SSH and Splunk web traffic.
2. **SIEM Deployment:** Installed Splunk Enterprise and configured it to ingest `/var/log/secure` authentication logs.
3. **Attack Simulation:** Launched a simulated SSH brute-force attack against the RHEL server using Kali Linux and the `rockyou.txt` password dictionary.
4. **Threat Hunting:** Utilized Splunk Processing Language (SPL) to query the ingested logs, identify the attacker's IP address, and confirm the intrusion signature.

## Results & Artifacts

![Splunk detecting the Hydra attack]()
*Splunk successfully detected a massive spike in failed SSH authentication attempts originating from the Kali Linux IP address.*

![Hydra brute force in Kali terminal]()
*The simulated attack utilizing Hydra.*
