# Incident Response Workflow and Playbook for Box Manufacturing

An individual academic cybersecurity project that translates incident-response guidance into a practical workflow for a fictional manufacturing organization working with an MSSP.

**Completed:** 2024  
**Program:** Lighthouse Labs  
**Project type:** Individual academic project  
**Scope:** Process and documentation design; not a production deployment

## Project summary

The project defines how a manufacturing organization could identify, escalate, contain, eradicate, recover from, and learn from a cybersecurity incident. It combines a visual workflow with escalation triggers, stakeholder responsibilities, evidence-handling expectations, and audience-specific communication templates.

The scenario used to exercise the design involves a missing Windows 11 business laptop with suspected unauthorized communications. All organizations, incidents, asset details, and contact information are fictional or generalized.

## Deliverables

- Five-stage incident-response workflow
- Escalation criteria for severity, business impact, third parties, critical systems, legal/privacy concerns, failed containment, and unresolved incidents
- Roles for executive, production, IT, network, database, security-operations, and MSSP stakeholders
- Technical escalation and executive status-update templates
- Lost-endpoint response checklist
- Post-incident review and corrective-action requirements
- Sanitized public case study with scope and limitations

## Framework basis

The original 2024 project was informed by:

- [NIST SP 800-61 Rev. 2](https://csrc.nist.gov/pubs/sp/800/61/r2/final) for incident-handling concepts
- [NIST IR 8228](https://csrc.nist.gov/pubs/ir/8228/final) for IoT cybersecurity and privacy-risk considerations
- [CISA incident and vulnerability response playbooks](https://www.cisa.gov/sites/default/files/2024-08/Federal_Government_Cybersecurity_Incident_and_Vulnerability_Response_Playbooks_508C.pdf) as supporting guidance

This repository does **not** claim implementation of MITRE ATT&CK, ISO/IEC 27001, or ITIL. Those frameworks were removed from the earlier README because they were not materially applied in the final project artifact.

> **Current-standard note:** NIST withdrew SP 800-61 Rev. 2 and superseded it with [SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final) in April 2025. The documentation preserves the 2024 project basis and points current readers to the newer publication.

## Workflow

![Incident Response Workflow](IR%20workflow.png)

| Stage | Intended outcome |
|---|---|
| Detection and identification | Validate the event, establish initial scope, preserve evidence, and assign severity |
| Containment | Limit damage while balancing evidence, safety, and operational continuity |
| Eradication | Remove the cause, persistence, and affected access paths |
| Recovery | Restore services in stages, validate controls, and monitor for recurrence |
| Lessons learned | Document root cause, impact, improvements, owners, and deadlines |

## Skills demonstrated

- Incident-response and playbook design
- Security-incident triage and escalation logic
- Technical and executive communication
- Stakeholder and responsibility mapping
- Evidence-preservation awareness
- Endpoint and IoT risk considerations
- Post-incident review and corrective-action planning
- Cybersecurity documentation grounded in authoritative guidance

## Repository contents

- [Detailed case study](docs/incident-response-case-study.md)
- [Workflow diagram](IR%20workflow.png)

## Scope and limitations

This was a design exercise, not a live incident response or production implementation. The workflow was not deployed in a SOC, MSSP, or client environment, and the project does not make claims of formal framework compliance, legal sufficiency, or control effectiveness. Public documentation has been sanitized to remove fictional contact details, duplicated content, and unsupported references from the original classroom report.
