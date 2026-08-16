# openOODA registry (static files)

This is the file-backed vendor published over HTTPS.

**Origin:** https://registry.openooda.org  
**Repo:** https://github.com/openOODA/registry

It is a static tree (`index`, `index.minisig`, `registry.pub`, package dirs). It is not a write API and not crates.io.

`index.minisig` is minisign of `index` with `registry.pub`. `ooda add --registry` verifies that signature with the pubkey shipped in the CLI. `index.sig` is leftover HMAC for local `--vendor` only.

```
./bin/ooda add hello --vendor ../registry
```

Packages here include proof fixtures (`evilcap`, `tooyank`). They are not recommended apps.
