# Emerging Technology Security Culture Portal

A readiness portal for aligning security culture with AI, IoT, cloud, edge, quantum, and zero-trust adoption.

This repository provides a production-minded PHP 8.x and MySQL 8.0 portal aligned with themes from Musaab Hasan's book, [Artificial Intelligence for Security Culture Transformation](https://www.amazon.com/Artificial-Intelligence-Security-Culture-Transformation/dp/3639876954). It translates the book's security culture transformation concepts into a working application foundation that can be extended for institutional, enterprise, and professional development contexts.

## Book Alignment

- Primary reference: **Chapter 16: Emerging Technologies and Their Impact on Security Culture**
- Transformation theme: Technology-adaptive security culture, secure innovation, anticipatory controls, and responsible adoption.
- Broader framing: moving from compliance-centered activity to measurable security culture, adaptive learning, and organizational resilience.

## Core Capabilities

- Role or unit assessment intake with CSRF protection and server-side validation.
- Weighted scoring model with maturity bands.
- MySQL schema for assessments, dimension scores, initiatives, evidence, and audit records.
- Dashboard view with maturity score, assessment volume, initiative tracking, and dimension cards.
- Roadmap view for implementation workflows and improvement planning.
- JSON summary endpoint for integration with reporting tools.
- Docker-based local development environment.
- Lint and self-test scripts for maintainability.

## Assessment Dimensions

- **AI Security Readiness**: Measures secure and responsible adoption of AI-enabled workflows.
- **IoT Awareness**: Tracks awareness of device, sensor, and operational technology risks.
- **Cloud and Edge Behavior**: Measures secure configuration, data handling, and shared responsibility.
- **Zero-Trust Mindset**: Assesses identity-first, least-privilege, and verification behaviors.
- **Quantum Preparedness**: Tracks early awareness of cryptographic transition needs.
- **Innovation Governance**: Measures whether new technology decisions include risk and ethics checks.

## Operating Workflow

- Assess readiness by emerging technology domain.
- Identify culture gaps that could lead to shadow technology or unsafe adoption.
- Create targeted interventions for teams adopting new platforms.
- Review readiness as part of innovation governance and architecture boards.

## Quick Start

```bash
cp .env.example .env
docker compose up --build
```

Then open:

- Application: `http://localhost:8080`
- Health endpoint: `http://localhost:8080/health`
- JSON summary: `http://localhost:8080/api/summary`

## Local Checks

```bash
php bin/lint.php
php bin/test.php
```

## Repository Structure

```text
public/              Web entry point and assets
src/                 PHP application services, repository, and support classes
config/              Portal configuration and scoring dimensions
database/            MySQL migration and seed data
docs/                Architecture, security, testing, and extension documentation
bin/                 Developer and release checks
```

## Production Notes

- Store database credentials and application secrets outside source control.
- Enforce HTTPS at the reverse proxy or load balancer.
- Use least-privilege database users.
- Route logs and audit records to approved monitoring systems.
- Review assessment data retention rules before collecting identifiable responses.

## License

MIT License. See [LICENSE](LICENSE).
