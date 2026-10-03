# Phishing Detection & Email Security Lab

A hands-on cybersecurity lab focused on investigating simulated
phishing emails using email analysis, header analysis, IOC extraction,
threat intelligence and phishing detection techniques.

## Objective

The objective of this project is to simulate a SOC-style phishing
investigation and develop a structured workflow for identifying,
analysing and responding to suspicious emails.

## Investigation Workflow

Suspicious Email
       ↓
Email Content Analysis
       ↓
Header Analysis
       ↓
IOC Extraction
       ↓
Threat Intelligence
       ↓
Detection Criteria
       ↓
Risk Assessment
       ↓
Incident Response
       ↓
Mitigation


## Skills Demonstrated

- Phishing email analysis
- Email header analysis
- IOC identification and extraction
- Threat intelligence investigation
- Social-engineering analysis
- SPF, DKIM and DMARC analysis
- URL and domain investigation
- Detection criteria development
- Incident response documentation
- Security reporting

## Tools & Technologies

- Email header analysis
- Threat intelligence resources
- IOC analysis
- DNS/domain investigation concepts
- SPF
- DKIM
- DMARC
- GitHub

## Investigation

### 1. Email Analysis

The simulated email impersonates Microsoft 365 Security and attempts to create urgency by threatening account suspension.

Key indicators identified:

- Lookalike sender domain
- Suspicious verification URL
- Brand impersonation
- Urgency and account-threat language
- Request for identity verification

### 2. Header Analysis

The simulated email headers were analysed to identify:

- Sender information
- Received headers
- Reply-To address
- SPF results
- DKIM results
- DMARC results

The simulated authentication results were:

| Authentication | Result |
|----------------|--------|
| SPF            | FAIL   |
| DKIM           | FAIL   |
| DMARC          | FAIL   |

### 3. IOC Extraction

The investigation identified several indicators:

- Suspicious sender addresses
- Lookalike domains
- Suspicious URL
- Simulated IP addresses
- Email authentication failures

All indicators are documented in the `iocs/` directory.

### 4. Threat Intelligence Workflow

A structured workflow was developed for investigating:

- Email addresses
- Domains
- URLs
- IP addresses

Potential intelligence sources include reputation services, domain/DNS information and internal security telemetry.

The indicators used in this project are simulated and use reserved documentation domains/IP addresses.

### 5. Detection Criteria

Detection criteria were developed around:

- Suspicious sender domains
- Lookalike domains
- Suspicious URLs
- Urgency and threat language
- Brand impersonation
- SPF/DKIM/DMARC failures

Multiple indicators should be considered together when determining phishing risk.

### 6. Incident Response

The investigation follows a structured response process:

1. Preserve the original email and headers.
2. Extract relevant IOCs.
3. Investigate domains, URLs and IP addresses.
4. Search internal security logs for related activity.
5. Determine whether the recipient interacted with the message.
6. Block confirmed malicious indicators where appropriate.
7. Remove similar messages if necessary.
8. Document findings and remediation.

## Repository Structure

phishing-detection-email-security-lab/
│
├── analysis/
│   ├── phishing-email-01-analysis.md
│   ├── phishing-email-01-header-analysis.md
│   └── threat-intelligence-workflow.md
│
├── detection/
│   └── phishing-detection-criteria.md
│
├── iocs/
│   └── phishing-email-01-iocs.md
│
├── reports/
│   └── phishing-email-01-incident-report.md
│
├── samples/
│   ├── phishing-email-01.txt
│   └── phishing-email-01-headers.txt
│
└── screenshots/

## Key Takeaways

This project demonstrates a structured approach to phishing investigation, from initial email analysis through IOC extraction, technical header analysis, detection criteria and incident response.

> **Note:** All email addresses, domains, URLs and IP addresses in this project are simulated for educational purposes. No real phishing infrastructure or malicious services were used.
