# Threat Intelligence Investigation Workflow

## Objective

Determine how the identified indicators would normally be investigated
using threat-intelligence resources.

## Investigation Process

### 1. Email Address

Investigate the sender and Reply-To addresses for:

- Previous reports
- Domain relationships
- Reputation information
- Known phishing campaigns

### 2. Domain

Investigate suspicious domains for:

- Domain registration information
- Domain age
- DNS records
- Hosting information
- Historical reputation
- Previous abuse reports

### 3. URL

Investigate the URL for:

- Reputation
- Redirect behaviour
- URL structure
- Associated domains
- Previous reports

### 4. IP Address

Investigate IP addresses for:

- Geolocation
- ASN/provider
- Hosting information
- Abuse reports
- Historical malicious activity

## Tools That Could Be Used

In a real SOC investigation, analysts could use resources such as:

- VirusTotal
- AbuseIPDB
- WHOIS/RDAP
- URLScan
- DNS investigation tools
- Internal SIEM/EDR telemetry

## Lab Limitation

The indicators in this project are simulated and use reserved
documentation domains/IP addresses. Therefore, no claim of real-world
malicious reputation is made for these indicators.

The purpose of this section is to demonstrate the investigation
methodology and workflow used by a security analyst.
