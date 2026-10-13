# Validation record

## 2026-10-13 package adaptation

Framework snapshot: d77194a, already fetched before adaptation. No framework source was modified. Package id/root github, schema_version 1, system gh declaration and command paths were adapted from the earlier domain-github prototype.

Local --path installation succeeded with 22 plugins; single-package validate passed with expected warnings for framework dependencies outside scope. Full validation and runtime checks are recorded separately below after execution.

The eight focused prototype regressions cover Notes preservation, offline reads, expiry, immutable identity mismatch, wrong account/API failure preservation, account switching, path validation and sanitized errors. Actual run results are appended below.

The target repository was initialized and write access granted before PR preparation. Registry registration and remote installation are not yet tested. No release tag exists. No official registry listing is claimed. Per-page atomic replacement is not a multi-page transaction; connector-channel recording remains manual, and issue/PR/CI caching and concurrent writers are outside this version.

## Executed results

- Full kernel all: 22 plugins passed; repeat convergence unchanged.
- Eight regression groups passed after relocation.
- Installed helper resolved its own instance root correctly from another working directory.
- Real authenticated gh refresh of account plus the explicitly selected target repository succeeded.
- Derived pipeline verify passed; combined audit: zero errors, zero warnings (five informational notices for empty instance declarations and newly mapped pages).
- Personal observations remain outside package source, in a separate local sandbox.
