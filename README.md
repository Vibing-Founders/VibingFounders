# VibingFounders — Compliance Plugin Marketplace

A public Claude plugin marketplace hosting compliance-focused plugins for website, platform, and app builders.

## Install this marketplace

```
/plugin marketplace add VibingFounders
```

Once added, you can install any plugin from this marketplace:

```
/plugin add compliance@VibingFounders
```

---

## Available Plugins

| Plugin | Description | Skills |
|--------|-------------|--------|
| `compliance` | Online safety, GDPR, and application security compliance for platform builders | `online-safety`, `gdpr`, `application-security` |

---

## Plugin Details

### `compliance`

Covers the regulations that matter most to platform builders:

- **UK Online Safety Act 2023** — illegal content duties, children's safety, risk assessments
- **EU Digital Services Act 2022** — platform obligations, transparency, content moderation
- **UK GDPR & EU GDPR** — data protection, lawful basis, data subject rights
- **UK Children's Code** — age-appropriate design for services likely accessed by children
- **US COPPA** — children's online privacy protection for US-facing platforms
- **OWASP Top 10** — application security baseline

### Skills

**`/online-safety`** — Assess your platform against UK OSA and EU DSA obligations
```
/online-safety assess my video-sharing platform
/online-safety checklist for a forum with user-generated content
/online-safety strategy-check for a consumer app that might have teen users
```

**`/gdpr`** — GDPR compliance for UK and EU data processing
```
/gdpr assess my user data handling
/gdpr checklist for a SaaS product collecting EU user data
/gdpr lawful-basis for sending marketing emails
```

**`/application-security`** — OWASP-based security assessment and checklists
```
/application-security assess my API
/application-security checklist for a new feature handling payments
```

---

## Repository Structure

```
plugins/
  compliance/
    .claude-plugin/plugin.json
    skills/
      _shared/          # Legislation and cross-cutting knowledge
      online-safety/    # UK OSA, EU DSA skills
      gdpr/             # UK/EU GDPR skills
      application-security/  # OWASP skills
```

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) to add a new plugin to this marketplace.

To add or update legislation in the compliance plugin, see [LEGISLATION.md](./LEGISLATION.md).
