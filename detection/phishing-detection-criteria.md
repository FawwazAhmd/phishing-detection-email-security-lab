# Phishing Detection Criteria

## Objective

Develop detection criteria that can be used by a security analyst to
identify emails with characteristics commonly associated with phishing.

## Detection Indicators

### 1. Suspicious Sender Domain

Flag messages when:

- The sender domain does not match the organisation being impersonated.
- The domain contains deliberate spelling variations.
- Numbers or additional words are inserted into a legitimate brand name.
- The sender uses an unfamiliar or newly observed domain.

Example:

`micr0soft-security.example`

The use of `0` instead of `o` is a lookalike-domain indicator.

---

### 2. Suspicious URLs

Flag URLs when:

- The destination domain does not belong to the claimed organisation.
- The URL contains brand names combined with unrelated domains.
- The URL uses suspicious or misleading subdomains.
- The link requests account verification or credential submission.

Example:

`https://login-microsoft-security.example/verify`

---

### 3. Urgency and Threat Language

Increase the risk score when an email:

- Creates an urgent deadline.
- Threatens account suspension.
- Threatens loss of access.
- Requests immediate action.
- Uses fear or pressure to influence the recipient.

---

### 4. Email Authentication Failures

Increase the risk score when:

- SPF fails.
- DKIM fails.
- DMARC fails.

Authentication failures should be investigated together with other
indicators rather than treated as the only evidence of phishing.

---

### 5. Brand Impersonation

Flag emails that:

- Claim to originate from a well-known organisation.
- Use branding or terminology associated with that organisation.
- Use a sender domain that does not belong to the organisation.

---

## Example Detection Logic

A message should receive a higher phishing risk score when multiple
indicators are present.

Example:

IF

- sender domain is suspicious
AND
- URL domain does not match the claimed organisation
AND
- message contains urgency or account-threat language

THEN

- classify as HIGH-RISK
- send for analyst investigation

Additional authentication failures such as SPF, DKIM or DMARC failures
can increase the confidence of the assessment.

---

## Analyst Response

When a message is classified as high-risk:

1. Preserve the original email and headers.
2. Extract relevant IOCs.
3. Investigate domains, URLs and IP addresses.
4. Search internal security logs for related activity.
5. Determine whether the recipient interacted with the message.
6. Block confirmed malicious indicators where appropriate.
7. Remove similar messages from other mailboxes if necessary.
8. Document the incident and recommended remediation.

## Expected Outcome

The detection criteria provide a repeatable process for identifying
potential phishing emails and prioritising suspicious messages for
further investigation.
