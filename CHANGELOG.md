# Changelog — `toxi-auth`

Per-crate history extracted from the monolith changelog
([meshackbahati/toxi](https://github.com/meshackbahati/toxi/blob/main/CHANGELOG.md)),
which remains the full documentation hub.

## [3.2.0] - 2026-09-28

- **toxi-auth** (`3.2.0`): password hashes use a fresh random salt per
  password. The previous fixed salt made identical passwords hash
  identically. Stored hashes remain verifiable; new hashes differ.

## Unreleased

- **toxi-auth** (`3.2.0`): session stores hand out `Arc<Session>` instead
  of deep copies. `SessionStore::get`, `SessionManager::get`, and session
  middleware move to shared sessions.

## Unreleased

- **toxi-auth** (`3.1.1`): `JwtManager` derives encoding, decoding, and
  validation once at construction instead of per token; the auth
  middleware shares one manager and no longer clones claims into
  extensions.
