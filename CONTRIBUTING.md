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

Use the Node version in `.node-version`:

```sh
npm ci --ignore-scripts
npm run check
```

The checks run locally without network access after dependencies are installed. They validate Markdown, local paths and anchors, navigation, publication text and paper checksums. They do not prove a technical claim or confirm an external website's contents.

For a paper change, update `papers/SHA256SUMS`, render and inspect the changed pages, and explain the publication revision in [Papers](docs/network/papers.md). Do not edit a binary merely to make its checksum pass.

## Review and publication

The team reviews changes before merging. This repository is the documentation source; it does not assert that a separate docs website is already deployed or automatically updated.

By contributing, you agree that your contribution is licensed under CC-BY-SA 4.0. The Komms name and logo remain excluded as set out in [NOTICE](NOTICE).
