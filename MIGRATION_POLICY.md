# Migration Policy

General Sports Desk starts from a clean public history. Material from retired or private projects is not automatically eligible for import.

## Allowed

- new code and documentation authored directly for this repository;
- clean-room implementations of provider-neutral interfaces and schemas;
- synthetic fixtures with no real users, private leagues, wagers, or provider-derived records;
- third-party dependencies whose licenses are reviewed and recorded in this repository.

## Not allowed

- private Git history, credentials, environment files, infrastructure details, databases, logs, backups, or caches;
- real user, account, league, wager, or other personal data;
- archived API responses or derived datasets without explicit redistribution rights;
- proprietary model weights, scoring, calibration, selection, grading, or evaluation logic;
- legacy branding, portraits, textures, logos, screenshots, or other assets without documented provenance and compatible rights.

## Provider integrations

Each provider integration must document:

- the official API and data terms;
- permitted use, storage, retention, redistribution, and commercial use;
- attribution requirements;
- rate limits and required client identification;
- privacy treatment for user or league identifiers;
- a removal path if access or terms change.

Provider-specific behavior belongs behind a small adapter. Tests should use synthetic payloads unless the fixture's redistribution license is documented.

## Import checklist

Before merging material influenced by a private or retired project:

1. identify its source, author/owner, and license;
2. prefer a clean-room rewrite over copying;
3. remove branding, identifiers, private logic, and provider data;
4. run tests, dependency/license review, and secret scanning on the tree and history;
5. add `THIRD_PARTY_NOTICES.md` when third-party code, data, or assets are included;
6. obtain explicit maintainer approval for the scoped import.

When rights are unclear, do not import the material.
