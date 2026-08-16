# openOODA registry (static files)

This is the file-backed vendor published over HTTPS.

**Origin:** https://registry.openooda.org  
**Repo:** https://github.com/openOODA/registry

It is a static tree (`index`, `index.sig`, package dirs). It is not a write API, not crates.io, and not a live `ooda add --registry` client yet. The product CLI still requires `--vendor` on disk.

`index.sig` is the existing local HMAC catalog signature (`ooda-local-pm`). That is not a public trust root. Do not treat a GET of this host as “verified from the internet” until minisign (or better) replaces HMAC.

```
./bin/ooda add hello --vendor ../registry
```

Packages here include proof fixtures (`evilcap`, `tooyank`). They are not recommended apps.
