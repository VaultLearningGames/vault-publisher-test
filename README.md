# vault-publisher-test

A stand-in for a Unity game repo, for testing [vault-publisher](https://github.com/VaultLearningGames/vault-publisher)
without a 45-minute Unity build. `simulate-build.mjs` writes Unity-style WebGL files in seconds (Brotli
WebAssembly, gzip JavaScript and data, a Unity 2019 `.unityweb` file).

It publishes to Vault's **staging** system (`VAULT_PUBLISHER_URL` = `https://portal.vaultlearninggames-staging.org`), so
tests never touch production. See vault-publisher's docs/setup.md.

- **Push any branch** → published to `https://builds.vaultlearninggames-staging.org/vault/publisher-test/<branch>/`,
  then the workflow checks the CDN's headers. Open the URL in a browser for in-page ✅/❌ checks.
- **Delete the branch** → its preview is removed.
