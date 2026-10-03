# Phishing Email 01 — Investigation

## 1. Email Analysis

The email claims to originate from Microsoft 365 Security and warns
that the recipient's account will be suspended within 24 hours.

### Sender Analysis

Sender:
security@micr0soft-security.example

The sender uses a lookalike spelling of Microsoft by replacing the
letter "o" with the number "0". The sender domain is also not an
official Microsoft domain.

### Subject Analysis

Subject:
Urgent: Your Microsoft 365 account will be suspended

The subject creates urgency by suggesting that the user's account
will be suspended.

## 2. URL Analysis

URL:
https://login-microsoft-security.example/verify

The URL uses a domain designed to resemble a Microsoft security
service but does not belong to Microsoft's legitimate domain space.

The use of a separate domain combined with Microsoft branding is a
strong phishing indicator.

## 3. Social Engineering Indicators

The message contains several social engineering techniques:

- Brand impersonation
- Urgency
- Threat of account suspension
- Request for identity verification
- Lookalike sender/domain

## 4. Initial Verdict

Based on the sender, subject, URL and social engineering indicators,
the message should be treated as a simulated phishing email.

Further investigation would normally include email-header analysis,
URL reputation checks and domain intelligence.
