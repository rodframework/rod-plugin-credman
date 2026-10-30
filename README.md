# rod-plugin-credman

credman -- Windows credential manager: survey the calling logon session's store and read its entries in place -- the inventory enumerated through the credential API (the system performs its own decryption), the generic entries' material returned as the credential rows the credentials board parses, nothing landing on disk -- collect.credman's exec...

A Rod capability module (entry kind: plugin) in the
[Rod](https://github.com/rodframework/Rod) ecosystem. The manifest
(`rod-module.toml`) is the contract; the package installs from the
[rod-registry](https://github.com/rodframework/rod-registry) index:

    rod mod install credman

## Building the artifact

The execution half compiles from the Rust module crates in the Rod
platform tree; `build.sh` drops it at the path the manifest's
`[[plugin.artifacts]]` row names, then `rod mod publish` packs it.
Point `ROD_RUST_TREE` at a Rod checkout's `src/implant/rust` (or an
unpacked `rod-src.tar.gz`):

    ROD_RUST_TREE=/path/to/src/implant/rust ./build.sh

## License

Apache-2.0, as declared in the manifest.
