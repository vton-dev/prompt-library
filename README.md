# prompt-library

`prompt-library` is a collection of organized, copy/paste-ready prompts for AI coding assistants.

The prompts are designed for practical software review work: architecture audits, backend and frontend checks, security reviews, data-flow analysis, deployment hardening, testing gaps, documentation accuracy, and operational readiness.

## What’s in this repo

The library is grouped by review area:

- [`architecture/`](architecture) - boundary, dependency-direction, and interface-contract audits.
- [`backend/`](backend) - correctness, error handling, and resource management audits.
- [`data/`](data) - persistence, import/export, data-flow, and cache correctness audits.
- [`deployment/`](deployment) - production hardening and CI/CD supply-chain audits.
- [`documentation/`](documentation) - documentation accuracy and decision-drift audits.
- [`frontend/`](frontend) - accessibility, design-system, and frontend correctness audits.
- [`hygiene/`](hygiene) - dead code, duplicate code, and placeholder/mock audits.
- [`legal/`](legal) - license compliance audits.
- [`operations/`](operations) - logging, monitoring, incident, and agent-readiness audits.
- [`performance/`](performance) - startup and runtime efficiency audits.
- [`security/`](security) - authentication, authorization, ABAC, input validation, secrets, file handling, and attack-surface audits.
- [`testing/`](testing) - coverage, contract testing, and authorization test-matrix audits.

## How to use

1. Pick the prompt file that matches the review you want to perform.
2. Copy the prompt into your coding assistant.
3. Run it against the repository you want audited.
4. Replace any generic placeholders with the real files, paths, or module names from your codebase.

These prompts work best when you give the assistant concrete source files, diffs, or repository context. They are written to encourage evidence-based review rather than speculative feedback.

## Adding prompts

When adding a new prompt, keep it:

- focused on one audit or task type
- specific about the evidence to gather
- explicit about the output format
- grounded in real repository behavior, not idealized architecture

Prefer short, reusable prompts that can be applied across repositories without heavy editing.

## License

This repository is licensed under the terms in [`LICENSE`](LICENSE).
