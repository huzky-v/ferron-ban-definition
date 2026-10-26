# Ferron ban definitions

Data-only definitions for [ferron-mod](https://github.com/huzky-v/ferron-mod): the canonical SQLite snapshot source, honeypot response templates, and executable snapshot test cases. Runtime Rust code and schema migrations remain in ferron-mod.

Clone ferron-mod with its submodule to get a compatible definition revision:

```sh
git clone --recurse-submodules https://github.com/huzky-v/ferron-mod.git
cd ferron-mod
cargo test --workspace
```

To test edits in this repository locally, check it out at `ferron-mod/definitions` and run the same test command in ferron-mod. The definition publishing workflow builds the snapshot and packages the templates without running tests; the rolling release title is the UTC publication date (`YYYY-MM-DD`). See [database updates](docs/database/README.md) for deployment details. Publish this repository before publishing a ferron-mod commit that points its submodule here.
