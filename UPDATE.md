# Maintenance Policy

This repository is the GitHub profile README for `binesheb`. It is documentation-only and has no runtime dependencies, application installer, or self-update mechanism.

## Manual updates

Update a local checkout from the repository source of truth:

```bash
git fetch --prune origin main
git pull --ff-only origin main
```

`--ff-only` prevents an update from silently creating a merge commit. If the checkout has local changes or has diverged, review and resolve them before updating.

## Automatic updates

Automatic runtime self-updates are intentionally not applicable. GitHub renders the README directly from the repository's `main` branch.

If a local mirror is maintained automatically, it must fetch **only `origin/main`**, never a feature branch, pull request ref, or arbitrary remote content. Validate the target revision before replacing any generated or deployed copy.

## Dependency policy

The profile currently has no package-managed dependencies. Future automation or tooling added to this repository must use supported, maintained dependencies and must not introduce packages that are marked deprecated or abandoned when a maintained alternative exists.

## Recovery

Use a known-good commit SHA to reproduce or restore the profile content. Keep GitHub `main` as the source of truth.
