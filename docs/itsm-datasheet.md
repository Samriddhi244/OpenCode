# ITSM Product Datasheet

> **Assessment status:** Preliminary / access-limited
>
> **Source reviewed:** Anakage demonstration portal at `https://demo.anakage.com/`
>
> This datasheet records only capabilities that could be verified from the accessible product surface. Items requiring authenticated navigation are explicitly marked **Not verified** rather than inferred as available.

## 1. Product overview

| Field | Finding | Status |
|---|---|---|
| Product / portal | Anakage demonstration portal | Observed |
| Primary URL | `https://demo.anakage.com/` | Observed |
| Visible entry point | Sign-in page with username and password fields | Observed |
| Product positioning | ITSM/self-service demonstration environment | Partially observed |
| Deployment model | Hosted web application / demo tenant | Inferred |
| Public documentation | Not available from the login page | Not verified |

## 2. Executive summary

The accessible surface is a hosted login page for an Anakage demo environment. The page provides username/password authentication, a **Remember** option, and a password-reset flow based on an email address. No authenticated application modules, records, workflows, dashboards, or administrative functions were accessible for verification in this assessment.

Accordingly, this document is a discovery-ready datasheet rather than a complete feature certification. It should be updated after an authenticated walkthrough or product documentation review.

## 3. ITSM capability matrix

| Capability | What to verify | Status | Evidence / notes |
|---|---|---|---|
| Incident management | Logging, categorization, prioritization, assignment, escalation, resolution, closure | Not verified | Requires authenticated application access |
| Service request fulfillment | Request intake, approvals, fulfillment tasks, closure | Not verified | Requires authenticated application access |
| Self-service portal | Service catalog, knowledge search, request tracking, user profile | Not verified | Login page is accessible; portal contents were not |
| Major incident management | Major-incident declaration, communications, review process | Not verified | Requires authenticated application access |
| Problem management | Root-cause analysis, known errors, workarounds, problem-to-incident relationships | Not verified | Requires authenticated application access |
| Change management | Change types, risk/impact, approvals, implementation, backout, PIR | Not verified | Requires authenticated application access |
| Knowledge management | Authoring, review, publishing, search, feedback, expiry | Not verified | Requires authenticated application access |
| Service catalog | Business/technical services, request forms, entitlement, approvals | Not verified | Requires authenticated application access |
| SLA management | Service targets, calendars, pause rules, breach warnings, reporting | Not verified | Requires authenticated application access |
| CMDB / asset management | Configuration items, relationships, discovery, lifecycle, ownership | Not verified | Requires authenticated application access |
| Service desk operations | Queues, assignment groups, agent workspace, omnichannel intake | Not verified | Requires authenticated application access |
| Reporting and analytics | Operational dashboards, KPI reports, filters, exports, scheduling | Not verified | Requires authenticated application access |
| Automation and orchestration | Rules, approvals, notifications, task automation, integrations | Not verified | Requires authenticated application access |
| Surveys and feedback | CSAT, NPS, post-resolution surveys, trend analysis | Not verified | Requires authenticated application access |

## 4. Observed authentication and access features

The public login page exposes the following elements:

- Username input.
- Password input.
- Login action.
- Remember option.
- Forgot-password flow requiring an email address.
- Return/back action from the password-reset view.

**Security interpretation:** These are UI observations only. Authentication protocol, MFA, SSO, password policy, session timeout, account lockout, audit logging, and authorization controls were not verified.

## 5. Workflow and lifecycle assessment

No authenticated records or workflow states were available for inspection. The following should be captured during a product walkthrough:

1. Intake channels and record creation.
2. Categorization and priority calculation.
3. Assignment and reassignment rules.
4. Approval stages and delegated approvals.
5. SLA start, pause, resume, and breach behavior.
6. Work notes versus customer-visible updates.
7. Resolution validation and closure codes.
8. Reopen behavior and parent/child record relationships.
9. Audit history and activity timeline.

## 6. Roles and permissions to validate

| Persona | Items to validate | Status |
|---|---|---|
| Requester / employee | Create requests, view own records, approve or comment | Not verified |
| Service desk agent | Work queues, update records, communicate with requesters | Not verified |
| Resolver / fulfillment team | Execute assigned tasks and update work | Not verified |
| Approver / manager | Approve requests and changes, delegate approvals | Not verified |
| Problem or change manager | Govern problem/change lifecycles and reviews | Not verified |
| Knowledge manager | Author, review, publish, retire articles | Not verified |
| ITSM administrator | Configure forms, workflows, SLAs, roles, notifications | Not verified |
| Platform administrator | Manage integrations, tenants, security, and audit settings | Not verified |

## 7. Data objects and fields to validate

The following data model elements should be documented from the application forms and APIs:

- Incident: number, caller, service, category, priority, assignment group, assignee, SLA, description, work notes, resolution, closure code.
- Service request: catalog item, requester, requested-for user, quantity, approvals, fulfillment tasks, cost, status.
- Problem: symptoms, affected services, root cause, known error, workaround, related incidents, corrective actions.
- Change: type, risk, impact, implementation plan, test plan, backout plan, approvals, maintenance window, PIR.
- Knowledge article: title, article type, audience, owner, version, approval state, publication dates, feedback.
- Configuration item / asset: class, owner, location, lifecycle state, relationships, support group, warranty or contract.
- SLA target: service, priority, calendar, response target, resolution target, pause conditions, breach status.

**Status:** Not verified against the demo tenant.

## 8. Reporting and KPI checklist

Validate whether the product provides:

- Incident volume and aging.
- First-contact resolution.
- Mean time to acknowledge and resolve.
- SLA compliance and breach trends.
- Backlog by queue, service, category, and priority.
- Major incident timelines.
- Change success, failure, emergency-change, and rollback rates.
- Problem reduction and known-error aging.
- Knowledge usage and deflection.
- Request fulfillment time and approval aging.
- Customer satisfaction trends.
- CSV, spreadsheet, PDF, API, scheduled, or role-based exports.

No dashboards or reports were visible from the unauthenticated surface.

## 9. Integrations, notifications, and administration

The following areas remain to be validated:

- Email intake and outbound notifications.
- Microsoft Teams, Slack, or other collaboration integrations.
- Identity providers and SSO/SAML/OIDC.
- Monitoring, event, and alert integrations.
- Discovery, endpoint management, or asset data sources.
- REST APIs, webhooks, import/export tools, and integration middleware.
- Notification templates, event triggers, escalation rules, and recipient controls.
- Audit logs, data retention, encryption, tenant isolation, and administrator activity history.

## 10. Access limitations

- The web-accessible inspection reached the login page only.
- Authenticated application screens could not be inspected in this environment.
- No credentials, tokens, or secrets are included in this repository.
- No claims are made about features that were not directly observed.

## 11. Discovery questions

1. Which ITIL practices are available out of the box, and which require configuration?
2. Does the platform support separate incident, request, problem, change, and task records?
3. Can administrators design forms and workflows without custom code?
4. How are SLAs calculated across business calendars, time zones, pauses, and escalations?
5. Does the service catalog support conditional fields, approvals, entitlements, and fulfillment orchestration?
6. What CMDB classes and relationship types are supported?
7. Which authentication methods and identity providers are supported?
8. What APIs, webhooks, import tools, and prebuilt integrations are available?
9. How are audit logs, retention, backups, and tenant isolation handled?
10. Which reports and dashboards are included, and can customers create custom analytics?
11. What licensing, user, agent, asset, storage, and API limits apply?
12. What implementation, migration, training, and support services are available?

## 12. Comparison-ready summary

| Dimension | Current finding |
|---|---|
| Accessible product surface | Hosted login and password-reset experience |
| ITSM feature verification | Incomplete; authenticated access required |
| Security verification | Limited to visible login controls |
| Workflow verification | Not completed |
| Reporting verification | Not completed |
| Integration verification | Not completed |
| Recommended next step | Conduct a guided authenticated demo and capture evidence for each capability in the matrix |

## Source inventory

- `https://demo.anakage.com/` — redirected to the demo login page; reviewed for visible authentication and password-reset elements.
