# PRD Safety Guide

This guide defines the minimum safety requirements for product requirement documents (PRDs) that introduce AI behaviors, automations, or model-assisted decisions.

## Scope

Use this guide for all PRDs in:

- `tasks/**-prd-*.md`
- `docs/prd/**/*.md`
- `prd/**/*.md`

## Required PRD Section

Each PRD must include the exact heading:

```markdown
## AI Ethics & Risk
```

At minimum, this section must document:

- AI involvement (yes or no)
- Risk assessment
- Mitigation strategies
- Human oversight requirements

## Risk Assessment Baseline

Document risks in each category below:

- Accuracy and truthfulness risk (incorrect outputs, hallucinations, stale data)
- Bias and fairness risk (unequal outcomes across users or cohorts)
- Privacy and data handling risk (sensitive data exposure, retention scope)
- Security and abuse risk (prompt injection, misuse paths, privilege escalation)
- Reliability and operations risk (failure modes, degraded services, rollback)

For each risk, include severity, impact, and detection method.

## Mitigation Requirements

For every identified risk, define:

- Preventive controls (input validation, policy checks, authorization gates)
- Detective controls (logging, alerts, anomaly thresholds)
- Corrective controls (fallback behavior, rollback plan, incident response path)
- Owner and due date for unresolved controls

## Human Oversight Requirements

Specify where a human must review or approve:

- High-impact outputs (legal, financial, medical, or safety-impacting)
- Release approvals for AI-feature changes
- Exception handling when confidence thresholds are not met

Also define escalation routes and accountable owners.

## Ethics Checklist for AI Features

If a pull request uses the `ai-feature` label, repository checks require an `ethics-checklist.yml` file at repository root. Use `docs/prd/ethics-checklist-template.yml` as the starting point.

Do not set `release_approved: true` until all required review and control fields are complete.

## Definition of Ready for Merge

A PRD is ready when:

- The `## AI Ethics & Risk` section is present and complete
- Risks and mitigations are concrete and testable
- Human oversight points are explicit and assigned
- The ethics checklist is present and consistent with the PRD

Document last updated on 2026-03-01. Verified against project logs, deliverables tracking, and communication archives.
