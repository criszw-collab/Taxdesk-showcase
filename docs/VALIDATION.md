# Validation and scope

## Recorded development checks

The version 2.2 test run completed with 192 passing automated tests. Earlier milestones recorded 168 tests for the staff/practice layer and 186 after client-portal isolation checks were added. These are development test counts, not user counts, model accuracy percentages or tax-return validation results.

Backend checks covered account bootstrap, salted password hashing, MFA enrollment/replay behavior, login throttling, session expiry and revocation, role checks, origin/request tokens, record-type checks and client record ownership. Portal-specific checks denied access to other clients' files and reports, blocked staff APIs, fixed ownership from the session and excluded internal material from client report projections.

Tax and pipeline checks used selected supported inputs and controlled model/source fixtures. The individual wage example produced a supported bracket-based planning estimate; this is not a substitute for an IRS Tax Table calculation or a completed return.

Email checks used mocked Gmail delivery. Duplicate-send claims, recipient restrictions, caps and uncertain outcomes were exercised without sending real client messages in those tests. The account owner separately tested the app locally, but this repository does not claim a measured production success rate.

## Browser checks

Controlled browser sessions exercised client login, question submission, document upload/linking, follow-up questions, direct planning calculations, PDF downloads, staff account creation, staff access to linked records and visibility of a saved staff answer in the client portal. A mobile viewport was also inspected. Model responses and email sending were controlled in these browser runs.

The interface images in this showcase come from those development runs and contain fictional records only. They are not live client screenshots or evidence of real tax advice.

## What has not been established

- Accuracy across all U.S. individual and business tax scenarios.
- Reliability of unverified answers for complex or changing tax rules.
- Independent security/compliance certification or a penetration test.
- Load capacity, uptime, disaster recovery or multi-tenant production readiness.
- A deployed internet portal linked to a worker on a personal computer.
- Automatic document interpretation or OCR.

The application source and executable test suite remain private. This showcase describes the checks and their limits without distributing the implementation.
