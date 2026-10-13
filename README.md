# GitHub state package

Cache selected GitHub account, organization, repository and gh environment facts for agents. Read cached context offline; refresh explicitly when current state is needed.

Package: github 0.1. Framework: >= 0.3. Python: >= 3.9. System connector: official gh >= 2.0, authenticated by the human. No connector executable or credentials are shipped.

## Local development installation

From a separate framework instance:

```text
python .meta/scripts/wiki_plugin_kernel.py install github --path /path/to/pkg-github
python .meta/scripts/wiki_plugin_kernel.py validate --scope github
python .meta/scripts/wiki_plugin_kernel.py all
python .meta/plugins/domains/github/github/scripts/state.py show --account LOGIN
python .meta/plugins/domains/github/github/scripts/state.py refresh --account LOGIN --repo OWNER/REPO
```

Source layout: `PKG.yaml`, `github/` (domain manifest and scripts), `command/github-state/` (skill), `.meta/docs/` (review documentation). Installation lands the package at `.meta/plugins/domains/github/`; do not wrap this repository inside another domains/github directory.

See [.meta/docs/github-domain.md](.meta/docs/github-domain.md) for design and [.meta/docs/github-validation.md](.meta/docs/github-validation.md) for evidence and limitations. The complete domain contract lives in [github/PLUGIN.md](github/PLUGIN.md).

This package does not change GitHub resources, make login permanent or use cached permissions as authorization. Snapshots stay in the user's instance. No September kernel-reliability changes are included.
