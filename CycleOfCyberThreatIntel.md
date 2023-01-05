# The Cycle of Cyber Threat Intelligence
Date: January 05, 2023

Source link: https://www.youtube.com/watch?v=J7e74QLVxCk

Author: Katie Nickels

# Full Process of Cyber Threat Intelligence

The purpose of cyber threat intelligence is to analyze information about the **_intent, capability, and opportunities of adversaries._**

This intelligence supports SOCs and their processes of incident response, specifically when it comes to decision making and resource prioritization.

## 1. Planning and Direction Fundamentals
**Intelligence requirements** are objectives that analysts seek to satisfy through their discovery phase.

**Threat model** is what you have and what your adversary wants.

## 2. Collection
### Intrusion Analysis
We can look at things like intrusion analysis frameworks, like the Lockheed Martin Cyber Kill Chain

### Malware
There are lots of public intelligence reports. Do not pull all intel from a single source, each one can be helpful.

[VirusTotal](https://www.virustotal.com/gui/home/upload), and [JOESandbox](https://www.joesandbox.com/#windows) are useful tools to scan files online to check for malware hidden.

### Domains
We can also pivot through whois lookups to validate emails, then go through 1 piece of data to another.

### External Data Sets (Threat data feeds)
We can look through IP addresses, digital hashes, and file names, but we should consider the source of the data for legitimacy.

### TLS Certificates
[Censys.io](https://censys.io/) and [Scans.io](https://scans.io/) are repositories of information for finding command and control infrastructure. 

## 3. Processing and Exploitation
After collecting all of our data, we need to break the large amount of data into smaller buckets. 

We should once again look at different frameworks like the Cyber Kill Chain, Diamond Model, and The MITRE ATT&CK.

We should also store this data in some repository for not only ourselves, but for others to see. Here are some places to do so: 
[CRITS](https://crits.github.io/#code), [MISP Threat Sharing](https://www.misp-project.org/), [threatnote](https://threatnote.io/), and [YETI](https://yeti-platform.github.io/)

### 4. Analysis and Production
A side note to keep in mind is that above all else, bias can change the quality and objectivity of our analysis. By minimizing bias, we can correlate actors, activity groups, campaigns, and intrusion sets that may not seem possible to correlate.

### 5. Dissemination
When presenting our analysis to an audience, we need to be considerate of our audience. Things to consider include their level of technical knowledge, and what part of the analysis matters to them.

# In Summary: Threat Assessment = Confidence + Analysis + Evidence + Sources
