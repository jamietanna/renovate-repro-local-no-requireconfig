# Renovate repro for `local` platform cannot override `requireConfig`

As part of https://github.com/renovatebot/renovate/discussions/25202.

When running:

```sh
env LOG_LEVEL=debug RENOVATE_REQUIRE_CONFIG=ignored npx renovate@37 --platform=local
```

You can see that no package files are detected, as the `renovate.json` gets used regardless.
