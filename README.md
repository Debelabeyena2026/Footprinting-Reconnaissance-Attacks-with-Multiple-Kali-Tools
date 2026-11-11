# Footprinting & Reconnaissance Attacks with Multiple Kali Tools

This repository documents a practical cybersecurity exercise focused on footprinting and reconnaissance using multiple Kali Linux tools. The goal is to demonstrate how publicly available information and network reconnaissance techniques can be used to identify exposed services, active hosts, and potential vulnerabilities, while reinforcing responsible and authorized testing practices.

## Project Overview

Footprinting and reconnaissance are the first phases of a cyberattack lifecycle. In ethical cybersecurity work, these steps are used to collect information such as IP addresses, open ports, operating systems, hostnames, DNS records, and network layout. This project approaches the subject from a defensive standpoint by showing how the same information can be used to identify weaknesses and improve security posture.

The repository includes the project report PDF and a summary of the workflow, tools, methodology, findings, and recommendations associated with the exercise.

## Objectives

The primary objectives of this project are to:

- understand the purpose and process of footprinting and reconnaissance
- identify what information can be collected about a target
- use multiple Kali Linux tools to gather network intelligence
- assess the exposure of services and systems
- document findings in a structured and ethical manner
- highlight defensive measures that reduce reconnaissance risk

## Scope

This exercise focuses on the reconnaissance stage of ethical hacking and includes activities such as:

- domain and DNS discovery
- host and network enumeration
- OS and service fingerprinting
- port and service discovery
- route and topology analysis
- assessment of exposed information and security implications

## Tools Used

This lab makes use of common Kali Linux reconnaissance tools, including:

- Nmap – port scanning and service detection
- Netdiscover – active host discovery on the local network
- Whois – domain and ownership information
- Dig – DNS record lookup and analysis
- Traceroute – path and network route discovery
- Nslookup / Host – DNS resolution checks
- Additional reconnaissance utilities when necessary for deeper enumeration

## Methodology

The workflow followed in this project is consistent with a standard ethical reconnaissance procedure:

1. Define the authorized scope and confirm the target is approved for testing.
2. Gather passive information such as DNS data, domain ownership, and public-facing services.
3. Identify active hosts and devices on the target network.
4. Probe open ports and services using network scanning tools.
5. Infer operating systems and service versions from observed behavior.
6. Record findings and assess potential risk exposure.
7. Summarize lessons learned and recommend defensive controls.

## Example Reconnaissance Commands

The following command examples represent common tasks performed during footprinting and reconnaissance:

```bash
# Domain and DNS information
whois example.com

dig example.com

dig example.com ANY

# DNS resolution
nslookup example.com
host example.com

# Host discovery
netdiscover -r 192.168.1.0/24

# Port and service discovery
nmap -sV -sC example.com
nmap -A -T4 example.com

# Route analysis
traceroute example.com
```

## Sample Findings Template

A typical footprinting report will document information such as:

- target hostname and IP address
- active hosts discovered
- open ports and running services
- OS or service version indicators
- DNS records and zone information
- possible exposure points or misconfigurations
- risk assessment based on observed data

Example findings summary:

```text
Target: example.com
IP Address: 93.184.216.34
Open Ports: 80/tcp, 443/tcp
Observed Services: HTTP, HTTPS
DNS Records: A, MX, NS records present
Assessment: Public exposure is limited but provides enough information for enumeration.
```

## Security Analysis

The information collected during footprinting may seem harmless in isolation, but when combined, it can reveal important details about a system or organization. The risk is not simply that a port is open; the greater concern is how much information an attacker can infer about the network, systems, and defenses.

This is why organizations must protect:

- DNS records and zone data
- public-facing services and applications
- network segmentation and firewall policies
- version disclosure and banner data
- asset inventory and host metadata

## Recommendations

To reduce reconnaissance risk, organizations should:

- restrict unnecessary public exposure
- harden firewalls and intrusion detection systems
- keep operating systems and applications patched
- minimize metadata leaks in DNS and web services
- disable unused services and ports
- monitor for network scanning and enumeration activity
- enforce least-privilege access and segmentation
- regularly review public-facing infrastructure exposure

## Ethical Considerations

This project is intended for educational and ethical cybersecurity practice only. Reconnaissance should only be performed on systems and networks where explicit permission has been granted. The purpose of this exercise is learning, defense, and responsible security assessment—not unauthorized access or malicious activity.

## Repository Contents

This repository contains:

- `README.md` – project overview, objectives, workflow, and security guidance
- `Week 2 report.pdf` – the report file associated with the footprinting activity

## Conclusion

Footprinting and reconnaissance are key stages in the cyberattack lifecycle. By understanding how attackers gather public information and enumerate targets, defenders can build stronger security controls and reduce the risk of exploitation. This repository serves as a practical summary of that process and provides a foundation for responsible offensive-security learning in a controlled environment.

## License and Use

This project is for educational and reporting purposes. It should be used in accordance with ethical cybersecurity practices and applicable laws or institutional policies.
