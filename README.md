# caddy-builder

This repository builds custom Caddy binaries with:

- `github.com/mholt/caddy-l4`
- `github.com/caddy-dns/cloudflare`

The GitHub Actions workflow in `.github/workflows/build-caddy.yml` runs daily and can also be started manually. It checks the latest upstream Caddy release plus the latest releases or tags for both plugins. A new release is created only when that combined version set has not been published before.

Release notes are based on the upstream Caddy release notes, with an added component table showing the exact plugin versions used for the build.

The workflow uses the built-in `GITHUB_TOKEN` with `contents: write` permission to create releases and upload assets.
