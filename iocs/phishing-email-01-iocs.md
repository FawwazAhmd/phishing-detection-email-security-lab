# Phishing Email 01 — Indicators of Compromise

## Email Indicators

| Type | Indicator | Description |
|---|---|---|
| Email Address | security@micr0soft-security.example | Suspicious sender using Microsoft impersonation |
| Email Address | security-verification@micr0soft-security.example | Suspicious Reply-To address |

## Domain Indicators

| Type | Indicator | Description |
|---|---|---|
| Domain | micr0soft-security.example | Lookalike domain impersonating Microsoft |
| Domain | login-microsoft-security.example | Suspicious verification domain |

## URL Indicators

| Type | Indicator | Description |
|---|---|---|
| URL | https://login-microsoft-security.example/verify | Simulated phishing URL |

## IP Indicators

| Type | Indicator | Description |
|---|---|---|
| IP Address | 198.51.100.23 | Simulated originating IP |
| IP Address | 192.0.2.45 | Simulated mail-server IP |

> Note: The IP addresses above belong to documentation/example ranges
> and are used only for this simulated lab.

## Authentication Indicators

- SPF: FAIL
- DKIM: FAIL
- DMARC: FAIL

## Social Engineering Indicators

- Microsoft brand impersonation
- Lookalike domain
- Urgency
- Threat of account suspension
- Request for account verification
- Suspicious verification URL

## IOC Summary

The investigation identified multiple indicators associated with the
simulated phishing attempt, including suspicious sender addresses,
lookalike domains, a phishing URL, simulated IP addresses and failed
email authentication checks.
