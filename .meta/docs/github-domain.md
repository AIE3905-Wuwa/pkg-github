# GitHub domain: design and package placement

GitHub remains the source of truth for repository, issue and PR state. The initial implementation caches only relatively stable account, organization, repository and gh runtime metadata. Fast-changing issue/PR/CI facts remain live queries.

The package id and its single family root are both `github`: the current kernel requires the package root to appear in its member roster. The former development name `domain-github` is superseded, not an additional dependency. Package source has PKG.yaml at repository root, matching existing package repos and the installer contract; installation lands it at `.meta/plugins/domains/github/`. No framework kernel changes are needed.

The system connector is declared as name gh, system true, expect >= 2.0. It ships no executable, performs no login and does not own credentials. Python 3.9+ is required by the helper. The current kernel exposes the connector as system in its package inventory; declaration alone does not enforce the binary version.

Host, observing principal, numeric identity and observation channel identify snapshots. GitHub connector access and gh access are independent. Local Markdown holds allowlisted snapshots and preserved human Notes, with exact UTC expiry (24h by default). Failed collection preserves earlier files; missing data is unknown. Cached permission never authorizes a remote write. Tokens, auth files, cookies and repository content are excluded.

Uninstall retains wiki/github and system gh credentials; no other plugin depends on this package. The package can be installed into an isolated framework instance via --path. Package registration follows review and first landing in pkg-github, via the independent registry repository.
