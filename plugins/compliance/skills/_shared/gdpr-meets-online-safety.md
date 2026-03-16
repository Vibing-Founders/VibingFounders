# Where GDPR Meets Online Safety

> How GDPR data protection constraints interact with online safety processing obligations — specifically around age assurance data, moderation logs, and incident records. This intersection creates a tension that platforms must navigate carefully.

---

## The Core Tension

**Online safety law** (UK OSA, EU DSA) **requires** platforms to:
- Collect and retain data about users to assure their age
- Log safety-relevant events and moderation actions
- Retain records of incidents (especially those involving minors) for extended periods
- Report CSAM and other serious content to authorities

**GDPR** **requires** platforms to:
- Have a lawful basis for all processing
- Collect only minimum necessary data
- Retain data only as long as necessary
- Give data subjects rights including erasure

These can appear to conflict. The resolution is in the lawful bases available and the explicit exemptions.

---

## 1. Age Assurance Data

### What it is

Age assurance data includes:
- Date of birth (collected at signup)
- Verification outcomes (verified/unverified, age band, verification method, timestamp)
- Risk signals used to determine age band (device signals, behavioural signals — where stored)
- Verification documents (ID images, selfies) if collected for L3 verification

### GDPR analysis

**DOB (date of birth):**
- **Lawful basis**: Contract (necessary to deliver the age-gated service) and/or Legitimate Interests (necessary to comply with regulatory obligations to protect minors)
- **Retention**: Keep for the lifetime of the account + a short period after deletion (for legal defence if an incident is later investigated); delete with the account
- **Minimisation**: Store the full DOB (day/month/year) so age recalculates over time — don't store just an age band, as that becomes stale

**Verification outcome + timestamp:**
- **Lawful basis**: Contract + Legal Obligation (compliance with OSA/DSA age assurance duties)
- **Retention**: Store the outcome permanently (or for the account lifetime) — you may need to prove you performed verification if a regulator asks during an investigation; delete with the account or soon after
- **Minimisation**: Store outcome only (e.g. "L3 verified, 2024-01-15") — not the raw document

**Verification documents (ID, selfies for L3):**
- **Lawful basis**: Legitimate Interests (safety, protecting minors) or Legal Obligation (where mandated)
- **Special category**: Selfies used for facial recognition / biometric age estimation may be **biometric special category data** (GDPR Art. 9) — this requires an Article 9 condition in addition to Art. 6 basis. Options: explicit consent, substantial public interest in child protection (GDPR Art. 9(2)(g)), legal claims.
- **Retention**: Keep only as long as needed for verification; **delete immediately after outcome is recorded** (keep only the outcome). Never retain ID documents permanently.
- **Practical**: Most platforms outsource this to a third-party KYC/age-assurance provider (Onfido, Jumio, Yoti, Veriff) who holds the raw documents under their own data agreements. You receive only the outcome.

**Risk signals (device fingerprint, IP, behavioural signals):**
- **Lawful basis**: Legitimate Interests (fraud prevention, safeguarding)
- **Retention**: Retain as long as the account is active and for a reasonable period after; archive risk scores for significant events
- **Minimisation**: Don't log every click — log signals that actually inform the risk model
- **Transparency**: Disclose in your privacy notice that you use these signals for age assurance purposes

---

## 2. Moderation Logs

### What they are

Moderation logs include:
- Reports submitted by users (reporter ID, reported user ID, content, timestamp, reason)
- Moderation actions taken (action type, moderator ID, outcome, timestamp)
- Content reviewed (message text, call metadata, flagged content)
- Automated system flags (keyword matches, risk model triggers)

### GDPR analysis

**Lawful basis**: Legitimate Interests (safety, fraud prevention) + Legal Obligation (UK OSA requires moderation capability and record-keeping; DSA requires similar)

**Retention**: OSA and DSA don't specify exact retention periods, but platforms must be able to respond to regulatory enquiries. Practical approach:
- Standard moderation logs (no action taken, no harm found): **90 days** is common; 6–12 months defensible
- Moderation actions taken (warning, suspension, ban): retain for **duration of account + 2 years** for appeals/regulatory enquiries
- Logs relating to CSAM: retain **indefinitely** (legal obligation to preserve evidence; reporting obligation)
- Logs relating to grooming/serious harm investigations: retain **until investigation closed + 2 years**

**Special category data**: Reports may contain sensitive information (e.g. a report about sexual content involving a minor). Process under public interest / substantial public interest basis (Art. 9(2)(g) or (b)) or legal claims.

**Data subject rights**:
- **Erasure**: A user can request erasure. You can refuse to erase moderation logs where they are needed for: legal claims (defence against litigation), regulatory obligations (OSA/DSA require record-keeping), ongoing investigations, compliance with a legal obligation.
- **Access (SAR)**: A user can request their own data. You do not need to disclose information about who reported them (reporter identity can be withheld on public interest / third-party rights grounds) or details of ongoing investigations.

---

## 3. Incident Records (Serious Harm Cases)

### What they are

For serious incidents — CSAM, grooming, sextortion, self-harm triggers:
- Full call metadata (participants, timestamps, duration, IP, device)
- Any recordings or screenshots preserved as evidence
- Incident investigation records
- Communications with law enforcement / NCMEC / IWF
- Referral records

### GDPR analysis

**Lawful basis**: Legal Obligation (mandatory CSAM reporting; law enforcement cooperation required by OSA/DSA) + Legitimate Interests (child protection, legal defence)

**Retention**:
- **CSAM evidence**: Must be preserved for law enforcement. Do not delete CSAM content or evidence (you are legally required to report and preserve). Retain **indefinitely** pending law enforcement direction.
- **Other serious incidents**: Retain all records **for the duration of any investigation, plus a period for legal defence** — in practice, 5–7 years for serious incidents is defensible.
- **Law enforcement referral records**: Retain permanently (you need to be able to show you acted)

**Data subject rights (attacker / perpetrator)**:
- Right to erasure: Can be refused — processing is necessary for legal claims, compliance with legal obligations, and substantial public interest in child protection
- Right of access: Can be refused where disclosure would prejudice an investigation or compromise third-party rights
- Right to restriction: Can be refused on legal obligation grounds

**Data subject rights (victim — the minor)**:
- Handle with extra care and sensitivity
- Erasure: The victim/their parent may want records deleted. Tension: you need to retain for legal proceedings. Explain clearly what you retain and why. Where possible, accommodate deletion of non-essential data while retaining legally required evidence.
- Access: A victim or their parent may SARs for investigation details. Handle sensitively; consider redacting information about other parties.

---

## 4. DPIA Requirements at the Intersection

Where online safety processing and GDPR interact, a **Data Protection Impact Assessment (DPIA)** is almost certainly required. Under UK GDPR Art. 35, DPIAs are required where processing is:
- Systematic and extensive profiling with significant effects on individuals → **age assurance = yes**
- Large-scale processing of special category data → **biometric age assurance = yes**
- Systematic monitoring of publicly accessible areas → **content moderation = yes**

**What your DPIA should cover for safety processing:**
1. **Description**: What data is collected, for what safety purposes, by what means
2. **Necessity and proportionality**: Is each type of processing the minimum needed for the safety purpose?
3. **Risks**: Impact on users (especially children) — profiling risk, surveillance risk, risk of misuse of retained data
4. **Mitigation measures**:
   - Strict access controls on safety data
   - Encryption at rest and in transit
   - Audit logs for access to sensitive moderation data
   - Retention limits and automated deletion workflows
   - Anonymisation/pseudonymisation where possible
   - Separation of safety data from commercial data (no using safety logs for targeting)
5. **Residual risk and sign-off**: Document that the DPIA was conducted and any residual risks accepted at the appropriate level (senior leadership / DPO)

---

## 5. Practical Recommendations

### Keep safety data separate from commercial data

Safety logs, moderation records, and incident data should be:
- In a separate data store with restricted access (not accessible to the marketing/analytics team)
- Subject to their own retention policies (stricter, not looser)
- Not used for any commercial purpose (targeting, product analytics, profiling)

This separation:
- Makes your legitimate interests argument much stronger (safety purpose is clearly separate from commercial purpose)
- Reduces the risk that safety data gets included in a commercial data breach
- Makes it easier to demonstrate to regulators that safety data is not misused

### Document your lawful basis for each safety process

Create a processing activity register that includes:
- Age assurance: lawful basis, data retained, retention period
- Moderation logs: lawful basis, data retained, retention tiers
- Incident records: lawful basis, retention period, law enforcement obligations
- Third-party processors used (KYC providers, moderation tools): DPAs in place, their security posture

### Train moderators on data protection

Moderators handle personal data (reports, content, user information). They need:
- Awareness of what data they can and cannot access
- Understanding of confidentiality obligations (especially for sensitive reports)
- Knowledge of when and how to escalate data protection concerns (e.g. if a SAR relates to an ongoing investigation)
- Clear instructions on not sharing information from reports with third parties without approval

### Brief your legal team

Regulatory enquiries from Ofcom (OSA) and the ICO can overlap. Ensure your legal team knows:
- What data you retain, and for how long
- The lawful basis for safety processing
- How you've reconciled OSA retention requirements with GDPR deletion rights
- Your CSAM reporting procedures and evidence preservation policies
