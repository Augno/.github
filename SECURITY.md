# Security Policy

This applies to every OpenMRP repository that does not carry its own `SECURITY.md`.

## Reporting a vulnerability

Email **[security@openmrp.ai](mailto:security@openmrp.ai)**, or use GitHub's private vulnerability
reporting on the affected repository (**Security → Report a vulnerability**). Please do not open a
public issue, and please give us a chance to ship a fix before disclosing publicly.

Include whatever you have: the affected component, steps to reproduce, what an attacker gains, and
any proof of concept. A working reproduction gets a fix out considerably faster than a description.

We aim to acknowledge within 3 business days and to give you an assessment and a rough timeline
within 10. We will keep you updated as the fix progresses and will credit you when it ships, unless
you would rather stay anonymous.

## Where to report

Several OpenMRP repositories are generated from `open-mrp/api` on every release — the SDKs
(`typescript-sdk`, `python-sdk`, `openmrp-go`) and `openapi-spec`. Report against whichever
repository you found it in; we will route it to wherever the fix has to land.

## Please don't

- Run automated scanners against production infrastructure
- Access, modify, or exfiltrate data belonging to other OpenMRP accounts
- Perform denial-of-service testing

## A note on test credentials

OpenMRP repositories contain fabricated sample keys and fixtures — `sk_test_`, `mrp_sk_test_`,
`whsec_`, sample JWTs, and local database passwords such as `root:Testing123!@localhost`. These are
not real. If you believe you have found a **real** credential, report it privately using the process
above rather than opening an issue.
