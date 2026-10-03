# CrossingKey Developer Documentation

**Public engineering guidance for integrating, reviewing, and operating CrossingKey systems.**

This repository documents the engineering standards behind CrossingKey implementations: explicit interfaces, bounded authority, recoverable execution, environment-managed secrets, meaningful verification, and documentation that separates claims from evidence.

## Engineering focus

- MCP, API, and webhook integration
- workflow and agent/tool orchestration
- machine-commerce and payment integrations
- persistent state, idempotency, replay protection, and reconciliation
- failure handling, bounded retry, and recovery
- local and cloud-oriented deployment patterns
- verification, release discipline, and handoff documentation

## Governed execution loop

For consequential systems, CrossingKey engineering separates intent, authority, execution, and proof:

`Authorize → Inspect → Plan → Execute → Verify → Record or Escalate`

A successful tool response is not automatically proof of the intended outcome. Verification should inspect the state that matters to the operator, and ambiguous external outcomes should be reconciled before a side effect is repeated.

This engineering pattern aligns with the public [HAAR research architecture](https://github.com/crossingkey-holdings/crossingkey-public-research/blob/main/research/HAAR.md) while remaining implementation-agnostic.

## Operating principles

1. **Capability does not imply authority.**
2. Inputs, permissions, side effects, and ownership boundaries must be explicit.
3. Retriable operations should be idempotent where practical.
4. Ambiguous outcomes should trigger reconciliation, not blind repetition.
5. Failures should preserve evidence and recovery paths.
6. Secrets belong in environment-managed storage, never source control.
7. Production claims require production evidence.
8. Documentation should make systems easier to inspect, operate, and transfer.

## Live implementation reference

CrossingKey MCP is the primary public implementation reference for governed machine commerce:

- Source: https://github.com/crossingkey-holdings/crossingkey-mcp
- Endpoint: https://mcp.crossingkeyintelligence.com/mcp
- Canonical identity: `com.crossingkeyintelligence/crossingkey-mcp`

## Start here

- [docs/ENGINEERING_STANDARD.md](docs/ENGINEERING_STANDARD.md)
- [docs/VERIFICATION_STANDARD.md](docs/VERIFICATION_STANDARD.md)
- [docs/REPOSITORY_SCOPE.md](docs/REPOSITORY_SCOPE.md)
- [SECURITY.md](SECURITY.md)

## Evidence and related surfaces

- Professional review: https://github.com/crossingkey-holdings/experience
- Public research: https://github.com/crossingkey-holdings/crossingkey-public-research
- Open specifications: https://github.com/crossingkey-holdings/crossingkey-open-specifications
- Web experience: https://github.com/crossingkey-holdings/crossingkey-web-experience
- Company: https://crossingkeyintelligence.com

## Contact

Implementation, integration, white-label, or technical-diligence inquiries: **founder@crossingkeyintelligence.com**
