# Contributing to OpenMRP

Thanks for your interest in OpenMRP. This applies to every OpenMRP repository that does not carry
its own `CONTRIBUTING.md`.

## Before you start

**Security issues do not belong in the issue tracker.** Email
[security@augno.com](mailto:security@augno.com) and give us a chance to ship a fix first.

**Some repositories are generated.** The SDKs (`typescript-sdk`, `python-sdk`, `openmrp-go`) and
`openapi-spec` are produced from the API on every release, so a direct edit is overwritten by the
next sync. Report the problem on the generated repository, but expect the fix to land in
`open-mrp/api`.

**For anything large, open an issue first.** A bug fix or a typo needs no preamble. A new
endpoint, a schema change, or a refactor spanning several packages is worth agreeing on before you
write it — we would rather discuss a design than decline a finished branch.

## Making a change

1. Fork, then branch from `main`.
2. Follow the repository's `README.md` for setup and match the surrounding code. Each repository
   documents its own toolchain.
3. Add tests. A bug fix should come with a test that fails without it.
4. Run that repository's test, lint, and format commands before pushing. CI runs them anyway, and
   running them locally is faster than waiting.

## Commits and pull requests

We use [Conventional Commits](https://www.conventionalcommits.org/), and releases are automated
from them by [release-please](https://github.com/googleapis/release-please). The prefix decides the
version bump, so it is worth getting right:

```
fix: reject an expired token on the refresh path     → patch
feat: add ship-by dates to the sales order list      → minor
feat!: rename the account_id query parameter         → major (breaking)
```

Pull request titles follow the same convention — most repositories squash-merge, so the PR title
becomes the commit message and the changelog entry.

In the description, say what changed and **why**. The diff already shows what; the reasoning is the
part a reviewer cannot reconstruct. Link the issue it closes, and call out anything you were unsure
about — a flagged judgment call is easier to review than a buried one.

## Licensing

Contributions are licensed under the terms of the repository you are contributing to; see its
`LICENSE` file. Most OpenMRP repositories are
[Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0). By contributing, you agree your
contribution is licensed under those terms.

The license covers the code, not the OpenMRP name or logo. Trademark terms are in `TRADEMARKS.md`
in `open-mrp/api`.

## Questions

Open an issue on the relevant repository, or email
[support@augno.com](mailto:support@augno.com).
