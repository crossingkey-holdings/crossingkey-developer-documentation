# Verification Standard

CrossingKey distinguishes **attempted**, **completed**, **verified**, and **blocked**.

## Minimum evidence

Where applicable, verification should include:

- executable behavior tests;
- syntax or build validation;
- link/path validation;
- dependency or configuration checks;
- checksums or manifests for release artifacts;
- remote-state confirmation after publication or deployment.

## Claim discipline

A successful local test is evidence of local behavior, not proof of production behavior. A deployment command is not proof of a successful deployment. A push is not considered verified until the intended remote state is confirmed.

## Failure reporting

Verification failures should preserve the failing command, relevant status, and the smallest actionable next step without exposing secrets.
