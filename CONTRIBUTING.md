# Getting a plugin listed

A listing says "someone read this exact commit and it does what it says". It is not an endorsement of later commits:
every new version is reviewed again and listed at its own commit.

Open an issue with:

1. the repository link and the full commit SHA you want reviewed;
2. what the plugin does, and why each permission in its `lucx-plugin.json` is needed;
3. the licence (the repository must contain its text).

What the review looks at: the manifest and permissions (a permission the plugin does not need is a reason to decline),
network use, what it stores, how it behaves when the panel is unreachable, that prebuilt binaries match the source, and that
removing it leaves the panel as it was. Plugins that need `network` or any `:write` permission get a closer look.

Reviewers: `go run ./tools/plugincatalog add ...` then `sign` (see the panel repository, `docs/plugin-catalog.md`).
