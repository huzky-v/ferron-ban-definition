# Ferron ban definitions

- This repository owns the canonical snapshot (`docs/database/attack-definitions-snapshot-v1.sql`), matching honeypot templates (`honeypot-responses/`), and behavioral cases (`tests/cases/`).
- The implementation, schema migration code, and test runner live in `huzky-v/ferron-mod`. In a local checkout, run `cargo test --workspace` from `../ferron-mod` after initializing its `definitions` submodule.
- Update snapshot SQL, response YAML, and snapshot cases together. Do not add version-specific cases to `ferron-mod/crates/abuse-core/tests/integration.rs`.
- `.github/workflows/definitions.yml` builds and publishes `attack-def.zip` without running definition tests or Rust validation. The ZIP has `definitions.sqlite` and `honeypot-responses/` at its root; the rolling release title is the UTC publication date (`YYYY-MM-DD`). Run definition tests locally with ferron-mod.
