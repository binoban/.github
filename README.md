# binoban/.github

Organization-level GitHub configuration for **Binoban**.

This repository powers the public org profile and provides default community health files
inherited by every Binoban repository that does not define its own.

## Contents

| Path | Purpose |
|---|---|
| `profile/README.md` | The public **organization profile** page shown at github.com/binoban |
| `SECURITY.md` | Default security policy (report to security@binoban.io) |
| `CONTRIBUTING.md` | Default contribution guidance |
| `SUPPORT.md` | Where to get help |
| `CODE_OF_CONDUCT.md` | Community standards |
| `.github/PULL_REQUEST_TEMPLATE.md` | Default PR template |
| `.github/ISSUE_TEMPLATE/` | Default issue forms + contact links |

> Repository-specific files (e.g. a repo's own `README.md`, `SECURITY.md`, or
> `CONTRIBUTING.md`) always override these org defaults.

## Publishing this repo

The GitHub repository **must** be named `.github` (the local folder name does not matter).

```sh
# from this folder
git init -b main
git config user.name "Binoban Engineering"
git config user.email "engineering@binoban.io"
git add -A
git commit -m "Add organization profile and default community health files"

gh repo create binoban/.github --public --source=. --remote=origin --push \
  --description "Binoban organization profile and default community health files."
```

The org profile page updates automatically once `profile/README.md` is on the default
branch.

## Maintenance

- Keep `profile/README.md` aligned with approved positioning copy and Binoban naming
  standards (Advertiser Portal, Retail Media, Supply / SSP, Exchange).
- After publishing, pin the priority repos on the org page (e.g. the SDK example repos,
  docs, OpenAPI, event spec).
