# Phishing Email 01 — Header Analysis

## Email Authentication

### SPF
Result: FAIL

The simulated email failed SPF authentication for the sender domain.

### DKIM
Result: FAIL

The simulated email failed DKIM authentication.

### DMARC
Result: FAIL

The simulated email failed DMARC authentication.

## Received Headers

The email passed through multiple simulated mail servers before
reaching the recipient.

The earliest connection originated from:

198.51.100.23

The subsequent connection was:

192.0.2.45

These addresses are documentation/example IP addresses used for this
lab and are not real infrastructure.

## Reply-To

security-verification@micr0soft-security.example

The Reply-To address uses the same suspicious lookalike domain as the
sender.

## Findings

The simulated headers provide additional evidence that the email
should be treated as phishing:

- SPF authentication failed
- DKIM authentication failed
- DMARC authentication failed
- Sender uses a lookalike domain
- Reply-To uses the same suspicious domain
- Multiple mail-server hops are present

## Analyst Assessment

The header information strengthens the initial phishing assessment.
In a real SOC environment, these authentication failures would be
investigated alongside the sender domain, message content, URLs and
other indicators.
