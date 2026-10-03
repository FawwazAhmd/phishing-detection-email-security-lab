# Phishing Email 01 — Incident Investigation Report

## 1. Incident Overview

**Incident Type:** Phishing / Credential Theft Attempt  
**Severity:** High  
**Status:** Confirmed Simulated Phishing  
**Environment:** Controlled Security Lab

### Summary

A simulated phishing email impersonating Microsoft 365 Security was
analysed after being identified as suspicious.

The message attempted to create urgency by claiming that the
recipient's Microsoft 365 account would be suspended unless identity
verification was completed.

Multiple indicators were identified, including a lookalike sender
domain, suspicious URL, social-engineering techniques and failed
email-authentication checks.

---

## 2. Indicators Identified

### Sender

`security@micr0soft-security.example`

The sender uses a lookalike representation of Microsoft by replacing
the letter `o` with the number `0`.

### Suspicious URL

`https://login-microsoft-security.example/verify`

The URL uses a domain that impersonates a Microsoft security service.

### Authentication

- SPF: FAIL
- DKIM: FAIL
- DMARC: FAIL

### Other Indicators

- Urgent account-suspension language
- Request for account verification
- Suspicious Reply-To address
- Brand impersonation

---

## 3. Investigation Process

The investigation followed these stages:

1. Reviewed the email sender and subject.
2. Analysed the message content for social-engineering indicators.
3. Extracted URLs, domains and email addresses.
4. Analysed simulated email headers.
5. Reviewed SPF, DKIM and DMARC results.
6. Documented identified indicators of compromise.
7. Developed phishing detection criteria.
8. Assessed appropriate mitigation measures.

---

## 4. Risk Assessment

The combination of multiple indicators significantly increases the
likelihood that the message represents a phishing attempt.

The most significant indicators were:

- Lookalike sender domain
- Suspicious verification URL
- Urgency and account-threat language
- Failed SPF, DKIM and DMARC authentication

---

## 5. Recommended Mitigation

For a real-world incident, recommended actions would include:

### Immediate Actions

- Quarantine the suspicious email.
- Prevent users from accessing confirmed malicious URLs.
- Search for the identified indicators across email and security logs.
- Determine whether any users interacted with the message.

### If Credentials Were Submitted

- Reset the affected user's credentials.
- Revoke active sessions where appropriate.
- Review authentication logs for suspicious activity.
- Investigate possible account compromise.

### Preventive Measures

- Strengthen email authentication controls.
- Implement phishing and impersonation detection.
- Educate users about suspicious links and urgency-based social
  engineering.
- Monitor for similar sender domains and URLs.

---

## 6. Final Assessment

The simulated email was classified as a phishing attempt based on
multiple independent indicators identified during the investigation.

The investigation demonstrates a structured SOC workflow covering
email analysis, header analysis, IOC extraction, threat intelligence,
detection criteria and incident response.
