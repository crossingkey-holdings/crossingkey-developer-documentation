# CrossingKey Developer Documentation

**Public engineering guidance for integrating, reviewing, and operating CrossingKey systems.**

This repository documents the engineering standards behind CrossingKey implementations: explicit interfaces, bounded authority, recoverable execution, environment-managed secrets, meaningful verification, and documentation that separates claims from evidence.

## Engineering focus

- API and webhook integration
- workflow and automation architecture
- agent/tool orchestration
- commerce and payment integrations
- failure handling, retry, and idempotency
- local and cloud-oriented deployment patterns
- verification, release discipline, and handoff documentation

## Operating principles

1. **Capability does not imply authority.**
2. Inputs, permissions, side effects, and ownership boundaries must be explicit.
3. Retriable operations should be idempotent where practical.
4. Failures should preserve evidence and recovery paths.
5. Secrets belong in environment-managed storage, never source control.
6. Production claims require production evidence.
7. Documentation should make systems easier to inspect, operate, and transfer.

## Start here

- [`docs/ENGINEERING_STANDARD.md`](docs/ENGINEERING_STANDARD.md)
- [`docs/VERIFICATION_STANDARD.md`](docs/VERIFICATION_STANDARD.md)
- [`docs/REPOSITORY_SCOPE.md`](docs/REPOSITORY_SCOPE.md)
- [`SECURITY.md`](SECURITY.md)

## Evidence and related surfaces

- Professional review and project evidence: https://github.com/crossingkey-holdings/experience
- Open specifications: https://github.com/crossingkey-holdings/crossingkey-open-specifications
- Web experience: https://github.com/crossingkey-holdings/crossingkey-web-experience
- Company: https://crossingkeyintelligence.com

## Contact

Implementation, integration, white-label, or technical-diligence inquiries: **founder@crossingkeyintelligence.com**
