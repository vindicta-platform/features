<!--
SYNC IMPACT REPORT
Version change: Initial → 1.0.0
Modified principles: Initial initialization from template.
Added sections: Core Principles, Administrative Oversight & Tooling Stack, Lifecycle & Workflow Gates, Governance.
Removed sections: N/A
Templates requiring updates:
- .specify/templates/plan-template.md: ✅ Updated (verified consistency)
- .specify/templates/spec-template.md: ✅ Updated (verified consistency)
- .specify/templates/tasks-template.md: ✅ Updated (verified consistency)
Follow-up TODOs: None.
-->

# Vindicta Platform - Features Constitution

## Core Principles

### I. Spec-Driven Methodology (BDD-First Mandate)
No code without a Spec. All development MUST follow the BDD → TDD → Implementation flow. Behavioral expectations MUST be defined and confirmed failing FIRST. Integration/unit tests satisfy the behavior; implementation satisfies the tests.

### II. Automated Quality Gates
Fast, predictable tests. Features must include Playwright tests for visual/structural changes and Python unit tests where backend validation is required. 60-second limit for full unit suite; <1s per individual test.

### III. Evidence-Led Stability & Blameless Retrospectives
Working models must not leave the repo in a broken state. Tests must prove feature validity. All failures are system failures to be documented and learned from.

### IV. Tooling Adherence & Environment
Strictly Windows (PowerShell/Batch). Use project-defined CLI tools (specify, just). Mandatory use of `uv` for dependency management.

### V. WIP Features & Blocked Test Tagging
Standardized use of `@wip` tags for features blocked by CLI/API structural gaps. These features must remain black-box oriented until the gap is closed.

## Administrative Oversight & Tooling Stack
Repository managed under the `vindicta-platform` organization. Tech stack includes HTML/JS/CSS for portals and Python for backend logic. `uv` is the mandatory package manager for Python environments.

## Lifecycle & Workflow Gates
Development follows the Speckit multi-agent workflow: Specify -> Plan -> Tasks -> Implement. Each phase requires artifact generation and verification. Gate completion is mandatory for phase transitions.

## Governance
Constitution supersedes all other practices. Amendments require documentation, approval, and a migration plan. All Pull Requests and reviews must verify compliance with these principles.

**Version**: 1.0.0 | **Ratified**: 2026-03-01 | **Last Amended**: 2026-03-01
