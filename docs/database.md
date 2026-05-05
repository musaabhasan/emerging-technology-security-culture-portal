# Database Schema

The portal uses MySQL 8.0 with `utf8mb4` collation.

## Tables

- `dimensions`: scoring dimensions and weights.
- `assessments`: assessment subject, weighted score, maturity band, and notes.
- `assessment_scores`: per-dimension scoring evidence.
- `initiatives`: improvement initiatives linked to impact areas.
- `evidence_items`: examples and supporting evidence records.
- `audit_events`: system activity trail.

## Portal Dimensions

- `ai_readiness`: AI Security Readiness - Measures secure and responsible adoption of AI-enabled workflows.
- `iot_awareness`: IoT Awareness - Tracks awareness of device, sensor, and operational technology risks.
- `cloud_edge_behavior`: Cloud and Edge Behavior - Measures secure configuration, data handling, and shared responsibility.
- `zero_trust_mindset`: Zero-Trust Mindset - Assesses identity-first, least-privilege, and verification behaviors.
- `quantum_preparedness`: Quantum Preparedness - Tracks early awareness of cryptographic transition needs.
- `innovation_governance`: Innovation Governance - Measures whether new technology decisions include risk and ethics checks.

## Seeded Initiatives

- Responsible AI adoption checklist (Digital Transformation, high)
- Cloud shared responsibility campaign (Cloud Platform, medium)
- Quantum transition awareness brief (Architecture, low)
