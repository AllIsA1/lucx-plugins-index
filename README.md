# lucx-plugins-index

The signed catalog of reviewed LucX-UI plugins. The panel reads `index.json` and `index.json.sig` from this repository
(`https://raw.githubusercontent.com/AllIsA1/lucx-plugins-index/main/`), checks the signature with the public keys built
into the panel and shows the plugins on its Plugins page. Installing from the catalog puts a plugin on exactly the commit
listed here.

- `index.json` — the list (schema, sequence, plugins).
- `index.json.sig` — ed25519 signature of `index.json`.

Never edit `index.json` by hand: the signature covers its exact bytes. Use the publisher tool from the panel repository
(`go run ./tools/plugincatalog`); see `docs/plugin-catalog.md` there for the commands and the format.

To get a plugin listed, read [CONTRIBUTING.md](CONTRIBUTING.md).
