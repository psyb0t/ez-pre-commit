# Changelog

All notable changes per release. Versions follow [semver](https://semver.org).

## v0.1.0 — 2026-08-01

First tagged release. This marks the existing contents of the repository as a
released state; it does not add new work.

The repository contains a single bash script that manages a git pre-commit hook:
it installs a hook (backing up any existing one) that runs a `pre-commit.sh`
script from the repository root, drops in a skeleton for that script, and can
uninstall the hook and restore the backup.

The repository is mirrored to Codeberg and GitLab, and archived to the Wayback
Machine, Software Heritage, and archive.org. The mirrors are force-pushed from
GitHub, so pull requests are disabled on them; issues and forking stay enabled,
and issues opened on either mirror are copied back into GitHub.
