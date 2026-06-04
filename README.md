# caddy-builder

## Build contents

This repository builds Caddy 2 with the plugins listed in `caddy-build-plugins.json`.

Current plugins:

- `github.com/mholt/caddy-l4`
- `github.com/caddy-dns/cloudflare`

## Plugin purpose

- `github.com/mholt/caddy-l4`: adds layer 4 TCP/UDP proxy support to Caddy.
- `github.com/caddy-dns/cloudflare`: adds Cloudflare DNS support for ACME DNS-01 certificate challenges.

## Build command

```sh
xcaddy build \
  --with github.com/mholt/caddy-l4 \
  --with github.com/caddy-dns/cloudflare
```
