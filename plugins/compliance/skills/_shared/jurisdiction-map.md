# Jurisdiction Map: Which Laws Apply Where

> Quick-reference guide for digital consumer platforms serving users in the UK, EU, and US. Covers data protection, online safety, children's privacy, and application security regulations.

---

## Quick Reference Table

| Jurisdiction | Data Protection | Online Safety / Content | Children's Privacy | Age Verification |
|---|---|---|---|---|
| **UK** | UK GDPR + DPA 2018 | Online Safety Act 2023 (Ofcom) | Children's Code (ICO) | OSA Part 5 |
| **EU (all MS)** | EU GDPR + ePrivacy | Digital Services Act (DSA) | GDPR Art. 8 (child consent) | DSA Art. 28 |
| **Germany** | EU GDPR + BDSG | DSA + NetzDG | Age of consent: 16 | JMStV |
| **France** | EU GDPR + loi Informatique et Libertés | DSA + ARCOM | Age of consent: 15 | ARCOM |
| **Ireland** | EU GDPR + Data Protection Act 2018 | DSA + Coimisiún na Meán | Age of consent: 16 | — |
| **Netherlands** | EU GDPR + UAVG | DSA | Age of consent: 16 | — |
| **Spain** | EU GDPR + LOPDGDD | DSA | Age of consent: 14 | — |
| **US (Federal)** | No comprehensive federal law | No federal OSA equivalent | COPPA (<13) | — |
| **US — California** | CCPA/CPRA | CA AB 2273 (AADC — blocked by courts, check status) | CPRA + AADC provisions | — |
| **US — Texas** | TDPSA | SCOPE Act (18+) | TDPSA provisions | HB 1709 |
| **US — Utah** | UCPA | Social Media Regulation Act | UCPA minor provisions | SB 152 |
| **US — Arkansas** | ADPPA proposals | Social Media Safety Act | — | AV law |
| **US — Florida** | — | HB 3 (under-14 social media ban) | — | — |

---

## UK — Detailed

### UK GDPR + Data Protection Act 2018

**Regulator**: Information Commissioner's Office (ICO)

**Applies to**: Any organisation established in the UK, or processing data of UK residents in connection with a UK establishment.

**Key provisions for platforms:**
- Lawful basis required for all processing (Art. 6)
- Children's consent for ISS: **13** is the threshold; under-13 requires parental authorisation (Art. 8)
- DPIA required for high-risk processing (Art. 35) — includes minors + comms
- Data subject rights: access, erasure, portability, objection (Arts. 15–22)
- Fines: up to **£17.5m or 4% of global annual turnover**

**Children specifically**: The ICO applies the Children's Code (Age Appropriate Design Code) to services "likely to be accessed by children" (under 18). Applies to all under-18s, not just under-13s.

---

### Online Safety Act 2023

**Regulator**: Ofcom

**Applies to**: User-to-user services and search services accessible to UK users.

**Key provisions:**
- Illegal content duties: must take steps to prevent, remove, and reduce priority illegal content
- Children's safety duties: risk assessment + proportionate safety measures for services likely to be accessed by children
- Age assurance duties: "highly effective" age assurance required to prevent under-18s accessing content that is legal for adults but harmful for children
- Transparency and accountability duties
- Fines: up to **£18m or 10% of global annual turnover** + potential criminal liability for senior managers

**Enforcement timeline**: Codes of practice taking effect in 2024–2025. Ofcom has already fined adult content sites.

---

## EU — Detailed

### EU GDPR (Regulation 2016/679)

**Regulator**: National Data Protection Authorities (DPAs) in each member state; coordinated via EDPB

**Applies to**: Organisations offering goods/services to EU residents, or monitoring behaviour of EU residents, regardless of where the organisation is based.

**Key differences from UK GDPR:**
- Child consent threshold for ISS: **16** (member states can lower to 13; varies)
- DPO mandatory in more circumstances
- Right to lodge complaints with DPA in member state of habitual residence
- Fines: up to **€20m or 4% of global annual turnover**

**Age-of-digital-consent by member state (verify — can change):**

| Country | Age of digital consent |
|---|---|
| Germany | 16 |
| France | 15 |
| Ireland | 16 |
| Netherlands | 16 |
| Belgium | 13 |
| Spain | 14 |
| Italy | 14 |
| Denmark | 13 |
| Sweden | 13 |
| Finland | 13 |
| Austria | 14 |
| Poland | 16 |
| Portugal | 13 |
| Czech Republic | 15 |
| Croatia | 16 |

---

### Digital Services Act (Regulation 2022/2065)

**Regulator**: National Digital Services Coordinators (DSCs) in each member state; European Commission for VLOPs/VLOSEs

**Applies to**: Online intermediary services with EU users. More obligations for larger platforms.

**Platform size tiers:**
- **All intermediary services**: basic liability and transparency obligations
- **Hosting services**: notice-and-action mechanisms
- **Online platforms** (including most consumer apps): complaint/redress mechanisms, trusted flaggers, counter-measures against misuse
- **Very Large Online Platforms (VLOPs)**: 45M+ active EU users — systemic risk assessments, audits, data sharing with regulators, researcher data access
- **Very Large Online Search Engines (VLOSEs)**: same as VLOPs for search

**Children provisions (Article 28):**
- No targeted advertising to minors
- No profiling of minors for advertising purposes
- High level of privacy, safety, and security by default for minors
- Prohibited: design features that create addictive behaviour or otherwise harm minors

**Fines**: Up to **6% of global annual turnover** for violations by VLOPs/VLOSEs; other providers up to national DSC-imposed penalties.

---

## US — Detailed

### COPPA (Children's Online Privacy Protection Act)

**Regulator**: Federal Trade Commission (FTC)

**Applies to**: Operators of websites and online services directed to children under 13, and operators of general services with actual knowledge they are collecting from under-13s.

**Key requirements:**
- Verifiable parental consent before collecting personal information from under-13s
- Right of parents to review and delete child's data
- Data minimisation and security for children's data
- Civil penalties: currently up to ~$51,744 per violation per day (updated by FTC periodically)

**2025 COPPA rule amendments** (verify current status): Expanded definition of personal information; strengthened parental consent requirements; new restrictions on targeted advertising to children.

**Practical approach for platforms excluding under-13s**: Must have genuine age-gating; cannot simply disclaim that the service is "for 13+". FTC holds platforms accountable for "actual knowledge" of underage users, which can arise from user-provided information (e.g. "I'm 12" in support).

---

### US State Laws — Overview

**No single federal teen privacy law** (as of early 2026). Patchwork of state laws:

**Comprehensive privacy laws with minor provisions** (opt-in for "sale"/"sharing" of minor data, stricter defaults):
- California (CCPA/CPRA), Colorado (CPA), Connecticut (CTDPA), Virginia (VCDPA), Texas (TDPSA), Montana (MCDPA), and many others

**Age-appropriate design / teen safety laws:**
- California AB 2273 (AADC) — blocked by federal courts for First Amendment reasons; monitor for updates
- Nebraska LB 1074 / Vermont H.89 — design code style laws with risk assessment + privacy-by-default requirements for minors
- Various others in 2024–2025 legislative cycles

**Social media restriction laws** (may restrict under-13/16 from joining without parental consent):
- Florida HB 3 (under-14 ban on social media accounts)
- Utah SB 152 (parental consent for minor social media accounts)
- Arkansas Social Media Safety Act (struck down; monitor)

**Age verification laws** (typically for adult content):
- Texas, Utah, Arkansas, Mississippi, Louisiana, Virginia, Montana, North Carolina — require age verification for pornographic/harmful-to-minors content

**Practical compliance posture for UK/EU-primary platforms:**
- Conservative baseline: treat all 13–17s as a protected group; no behavioural advertising to minors; high privacy defaults
- US-specific notices and rights (CCPA opt-out mechanism if selling/sharing data)
- Do not operate adult content accessible to US users without age verification that meets your most restrictive applicable state's requirements

---

## Applicability Matrix for Common Features

| Feature | UK Laws | EU Laws | US Laws |
|---|---|---|---|
| User registration (under 18) | UK GDPR Art. 8, Children's Code | EU GDPR Art. 8 (age varies by country) | COPPA if under 13 |
| Private or direct interactions (video, messaging, live sessions) | OSA (duty of care, risk assessment) | DSA (risk assessment, moderation) | State minor safety laws (CA, TX etc.) |
| Group chat with minors | OSA (mandatory moderation) | DSA Art. 28 | COPPA / state laws |
| Behavioural advertising | Children's Code (off by default) | DSA Art. 28 (banned for minors), GDPR consent | CCPA, TDPSA, state minor provisions |
| Age verification | OSA Part 5 | DSA Art. 28 | COPPA (effective blocking), state AV laws |
| Creator payouts | UK GDPR (financial data), AML | EU GDPR, AML Directives | BSA/AML (FinCEN), IRS |
| Selfies / recordings with minors | UK GDPR, Children's Code | EU GDPR (special category if biometric) | BIPA (Illinois), state biometric laws |
| Data export / erasure | UK GDPR Arts. 20, 17 | EU GDPR Arts. 20, 17 | CCPA/CPRA right to delete |
