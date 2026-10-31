# Contributing

Corrections to facts, unclear wording, accessibility and broken links are welcome.

## Suggest a change

For a small correction, open a pull request. For a change to scope, policy or architecture, open an issue first. Do not include private correspondence, credentials, customer data or internal operational records.

Pages are plain Markdown, one guide per subject. From the repository root, a guide link looks like `[Plans and pricing](docs/getting-started/plans-and-pricing.md)`. Inside `docs/`, use a path relative to the page being edited.

## House style

- Use British English and plain, direct language.
- Never use an em dash. Rewrite with a comma, colon or full stop.
- Keep one canonical location for each policy or status fact; link to it elsewhere.
- Distinguish specified, implemented, tested, deployed and independently qualified. See [Evidence and claim boundaries](docs/network/evidence.md).
- Label planned features and prices. A design, merged change or test count does not establish operating readiness.
- Preserve the scope of security claims. State relevant metadata, availability and recovery limits.
- Source commercial claims from the owner-approved [website](https://komms-landing-landing-page.up.railway.app/) and technical claims from verified specifications and evidence. Resolve contradictions before publication.
- Do not add authorship credits or tool attribution to repository text, commits or pull requests.

## Run the checks

Use the Node version in `.node-version` and the dependency versions in `package-lock.json`. When Markdownlint is already installed under `node_modules`, run it through its Node API with `.markdownlint.json`.

This snapshot does not contain a publication checker or tool test suite. Review local paths and anchors, navigation, publication text and paper checksums separately. Markdown lint does not prove a technical claim or confirm an external website's contents.

For a paper change, include a `papers/SHA256SUMS` manifest, render and inspect the changed pages, and explain the publication revision in [Papers](docs/network/papers.md). A checksum identifies bytes; it does not validate the paper's claims.

## Review and publication

The team reviews changes before merging. This repository is the documentation source; it does not assert that a separate docs website is already deployed or automatically updated.

By contributing, you agree that your contribution is licensed under CC-BY-SA 4.0. The Komms name and logo remain excluded as set out in [NOTICE](NOTICE).
