# Engineering Standard

## Interfaces

Public or internal interfaces should document inputs, outputs, side effects, authorization requirements, failure modes, and version expectations.

## Secrets

Credentials and signing material must not be hard-coded. Use environment variables, platform secret stores, or equivalent managed mechanisms. Example values must be clearly non-production.

## Network operations

External calls should use bounded timeouts. Retriable mutations should use idempotency controls where the upstream service supports them. Retry logic must not silently duplicate irreversible actions.

## State and ownership

When an operation acts on user-, customer-, case-, account-, or tenant-scoped data, the implementation should verify the caller is authorized for that scope.

## Recovery

A useful failure result identifies what completed, what did not, what evidence exists, and what the safe next attempt should do.

## Handoff

A deliverable is not complete merely because it runs on the original developer's machine. Operational assumptions, configuration, verification steps, and known boundaries should be documented.
