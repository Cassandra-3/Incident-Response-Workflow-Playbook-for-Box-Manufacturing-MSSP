# Incident Response Case Study: Box Manufacturing

## Project profile

- **Project type:** Individual academic cybersecurity project
- **Program:** Lighthouse Labs
- **Completed:** 2024
- **Environment:** Fictional manufacturing organization and managed security service provider (MSSP) scenario
- **Focus:** Incident-response process design, escalation, stakeholder coordination, and communication
- **Operational status:** Design exercise; not deployed or tested in a production environment

## 1. Context

Box Manufacturing is a fictional manufacturer that relies on business laptops, networked systems, production technology, and Internet of Things (IoT) devices. The scenario assumes that the organization works with an MSSP for cybersecurity support but needs a clear internal workflow for identifying, escalating, containing, and learning from security incidents.

The project addressed a practical governance problem: technical responders, business leaders, and third parties need a shared process before an incident occurs. Without defined triggers, responsibilities, evidence-handling expectations, and communication paths, an organization can lose time during a high-impact event.

## 2. Project objective

The objective was to design a usable incident-response workflow and playbook that would:

1. guide staff through a consistent response process;
2. define when an issue should be escalated to management or the MSSP;
3. assign responsibilities to technical and business stakeholders;
4. provide separate communication formats for technical responders and executives;
5. account for endpoint, network, operational, and IoT-related risk; and
6. capture lessons learned for process improvement.

## 3. Framework basis

The original 2024 work was informed by:

- [NIST SP 800-61 Rev. 2 — Computer Security Incident Handling Guide](https://csrc.nist.gov/pubs/sp/800/61/r2/final)
- [NIST IR 8228 — Considerations for Managing Internet of Things Cybersecurity and Privacy Risks](https://csrc.nist.gov/pubs/ir/8228/final)
- [CISA Federal Government Cybersecurity Incident and Vulnerability Response Playbooks](https://www.cisa.gov/sites/default/files/2024-08/Federal_Government_Cybersecurity_Incident_and_Vulnerability_Response_Playbooks_508C.pdf)

The five-stage workflow is an academic adaptation of incident-handling concepts. It is not a claim of formal compliance or certification.

> **Standards maintenance note:** NIST withdrew SP 800-61 Rev. 2 and superseded it with [SP 800-61 Rev. 3](https://csrc.nist.gov/pubs/sp/800/61/r3/final) in April 2025. This case study preserves the framework used when the project was completed and identifies the newer publication for current readers.

## 4. Scenario used to exercise the playbook

A Windows 11 business laptop is reported lost. Monitoring information suggests that the device may be communicating without authorization. The event creates several possible risks:

- exposure of organizational or personal information;
- unauthorized access using cached credentials or active sessions;
- further access to internal systems;
- operational disruption;
- regulatory, contractual, or notification obligations; and
- reputational impact.

The scenario is fictional. Asset identifiers, names, contact details, and message templates in this public version have been generalized.

## 5. Designed incident-response workflow

![Five-stage incident-response workflow](../IR%20workflow.png)

### Stage 1 — Detection and identification

**Purpose:** determine whether an observable event is a security incident and establish an initial scope.

Key activities:

- record the time, source, and nature of the alert or report;
- identify the affected asset, user, system, location, and business owner;
- collect available logs, screenshots, alerts, and user observations;
- preserve evidence and document who collected it;
- check for related indicators on other systems;
- assess confidentiality, integrity, availability, safety, and operational impact;
- assign a preliminary severity and open an incident record; and
- notify the appropriate internal lead.

**Decision point:** If malicious activity cannot be ruled out, the device is missing, sensitive data may be exposed, or operations may be affected, proceed to containment and escalate according to the criteria below.

### Stage 2 — Containment

**Purpose:** limit harm while preserving information needed for investigation.

Potential actions, subject to approval and technical capability:

- isolate the affected endpoint from the network;
- disable or restrict relevant sessions, tokens, or credentials;
- block confirmed malicious indicators;
- preserve volatile and non-volatile evidence;
- identify other potentially affected assets;
- apply temporary network segmentation or access restrictions; and
- communicate business workarounds to affected teams.

Containment decisions should balance security, safety, evidence preservation, and continuity of operations.

### Stage 3 — Eradication

**Purpose:** remove the cause and persistence mechanisms after the scope is understood.

Potential actions:

- remove malicious files, software, accounts, scheduled tasks, or persistence;
- remediate exploited vulnerabilities or configuration weaknesses;
- reset or rotate affected credentials and secrets;
- validate that unauthorized access paths have been closed;
- rebuild or reimage systems when integrity cannot be established; and
- document all changes and retained evidence.

### Stage 4 — Recovery

**Purpose:** return systems to service in a controlled manner.

Key activities:

- restore from known-good sources where appropriate;
- validate security controls and required business functions;
- reconnect systems in stages;
- increase monitoring for recurrence;
- obtain technical and business-owner approval;
- record the recovery time, residual risk, and outstanding actions; and
- communicate service restoration to stakeholders.

### Stage 5 — Lessons learned

**Purpose:** improve controls, documentation, and readiness.

The review should capture:

- what happened and how it was detected;
- the timeline of decisions and response actions;
- root cause and contributing factors;
- business, technical, privacy, and operational impact;
- what worked and what caused delay;
- control, policy, training, or architecture improvements;
- owners and due dates for corrective actions; and
- measurable updates to the playbook.

## 6. Escalation model

The project defined escalation triggers so that responders would not rely only on personal judgment during a stressful event.

| Trigger | Example | Escalation |
|---|---|---|
| High or critical severity | Sensitive information, privileged access, multiple systems, safety concern | Notify incident lead and senior management immediately; engage MSSP |
| Critical system affected | Production, identity, core network, or business-critical service | Engage system owner and MSSP; assess continuity plan |
| Third party involved | Supplier, cloud provider, or service provider may be affected | Notify contract/vendor owner and coordinate evidence exchange |
| Containment unsuccessful | Malicious activity continues or scope expands | Escalate technical response and management oversight |
| Significant operational or financial impact | Production outage, service interruption, or material revenue risk | Notify business leadership and continuity stakeholders |
| Legal, privacy, or contractual concern | Possible reportable breach or contractual notification | Engage authorized legal/privacy decision-makers |
| Unresolved after 48 hours | Root cause, scope, or containment remains uncertain | Formal management review and additional specialist support |

The 48-hour condition is an internal scenario trigger, not a universal legal deadline.

## 7. Roles and responsibilities

| Role | Designed responsibilities |
|---|---|
| Incident lead / MSSP consultant | Coordinate the response, maintain the incident record, support analysis, and communicate status |
| Executive leadership | Set business priorities, approve high-impact decisions, and accept residual risk |
| Production managers | Explain operational impact, coordinate safe workarounds, and support recovery validation |
| Database specialist | Assess database exposure, preserve relevant evidence, and support restoration |
| IT support | Triage reports, identify assets and users, implement authorized endpoint actions, and document changes |
| Network administrator | Review network activity, apply authorized isolation or blocking, and preserve network evidence |
| Security operations | Monitor alerts, correlate indicators, support investigation, and watch for recurrence |
| Legal/privacy or designated management contact | Determine notification and regulatory obligations when required |

These roles describe the proposed operating model for the scenario; they do not claim that the author performed each production role.

## 8. Communication design

The playbook separates technical and executive communication because each audience needs different information.

### Technical escalation template

**Subject:** Security incident escalation — [incident ID / affected asset]

- Detection time:
- Reporting source:
- Affected asset(s) and user(s):
- Observed indicators:
- Initial severity and rationale:
- Actions already completed:
- Evidence preserved:
- Current containment status:
- Known or suspected business impact:
- Assistance or decision required:
- Next planned update:

### Executive status template

**Subject:** Executive update — [incident ID / business service]

- What happened:
- What is currently affected:
- Business and customer impact:
- What the response team has done:
- Current risk:
- Decisions or resources required:
- Expected next milestone:
- Time of next update:

Communications should use approved channels, protect sensitive investigation details, and avoid unsupported conclusions.

## 9. Response checklist for the lost-laptop scenario

- [ ] Confirm the report and asset ownership.
- [ ] Record the last known location and time of authorized use.
- [ ] Determine whether the device is managed, encrypted, and remotely controllable.
- [ ] Preserve relevant identity, endpoint, network, email, and cloud logs.
- [ ] Review recent sessions and suspicious communications.
- [ ] Revoke or restrict exposed sessions and credentials as authorized.
- [ ] Isolate, lock, or wipe the device only through approved procedures.
- [ ] Identify data that may have been stored or accessible.
- [ ] Assess related systems and accounts for unauthorized activity.
- [ ] Notify business, privacy, legal, insurance, law-enforcement, or third-party contacts when authorized decision-makers determine it is required.
- [ ] Validate containment and increase monitoring.
- [ ] Document recovery, closure approval, lessons learned, and corrective actions.

## 10. Skills demonstrated

This project provides evidence of:

- incident-response workflow and playbook design;
- incident triage and severity reasoning;
- escalation criteria and decision-point development;
- role and responsibility definition;
- technical and executive communication;
- evidence-preservation and documentation awareness;
- endpoint and IoT risk consideration;
- stakeholder coordination planning; and
- framework-informed cybersecurity documentation.

## 11. Limitations

This was an individual academic design project. It did not include:

- response to a live security incident;
- deployment in a production SOC or MSSP;
- legal advice or a determination of regulatory notification duties;
- technical validation against a live Box Manufacturing environment;
- formal certification against NIST, CISA, ISO, or another standard; or
- evidence that every referenced product or control was implemented.

The public case study intentionally removes fictional contact data and unsupported references from the original classroom report.
