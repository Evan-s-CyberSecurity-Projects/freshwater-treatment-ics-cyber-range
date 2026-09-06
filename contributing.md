
---

# `CONTRIBUTING.md`

For this project, I would make contributing rules deliberately simple.

```markdown
# Contributing

Thank you for contributing to the Freshwater Treatment ICS Cyber Range.

This project is designed to be a reproducible educational ICS/OT
environment, so changes should prioritize reliability, clarity,
security, and repeatability.

---

## Development Principles

Contributions should follow these principles:

### Reproducibility

Changes should work consistently when the cyber range is rebuilt.

Avoid changes that depend on manual configuration unless the manual
step is explicitly documented.

### Safety

Changes must remain appropriate for an isolated educational
environment.

Do not introduce functionality that could unintentionally affect
production systems or external networks.

### Security

Do not commit:

- Passwords
- API tokens
- Personal access tokens
- SSH keys
- Jenkins credentials
- Docker registry credentials
- `.env` files containing secrets
- Production configuration

Use placeholders and environment variables instead.

### Documentation

Changes that affect deployment, networking, SCADA behavior, PLCs,
sensors, or security testing should include corresponding
documentation updates.

---

## Repository Structure

Major project components are organized as follows:

```text
architecture/     System and network architecture
deployment/       GNS3 and CI/CD automation
scada/            SCADA configuration and visualization
plc/              PLC documentation and process definitions
sensors/          Sensor definitions and simulation behavior
labs/             Training exercises
security/         Security research and testing
documentation/    Technical documentation
screenshots/      Project visuals
.github/          Repository automation and templates
