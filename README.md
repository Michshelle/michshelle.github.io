# michshelle.github.io

Static personal presentation site.

## Local update workflow

1. Edit files.
2. Commit and push:

```bash
git add .
git commit -m "Update site"
git push
```

GitHub Pages deploys automatically from `main`.

## GitHub Pages settings

For repository `Michshelle/michshelle.github.io`:

1. Go to `Settings -> Pages`.
2. Source: `Deploy from a branch`.
3. Branch: `main` and folder `/ (root)`.

## Custom domain: sync.michshell.net

This repository already includes [CNAME](CNAME) with:

```txt
sync.michshell.net
```

In your DNS provider for `michshell.net`, create:

- Type: `CNAME`
- Name/Host: `sync`
- Target/Value: `michshelle.github.io`
- TTL: default

After DNS propagates:

1. In `Settings -> Pages`, ensure Custom domain shows `sync.michshell.net`.
2. Enable `Enforce HTTPS`.

## Verify

```bash
curl -I https://michshelle.github.io/
curl -I https://sync.michshell.net/
```
