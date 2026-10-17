# Changelog — `armature-grpc`

All notable changes to this crate will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this crate adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Earlier changes are recorded in the workspace [`CHANGELOG.md`](../CHANGELOG.md).

## [Unreleased]

## [0.3.0] - 2026-10-17

### Changed

- **Sibling requirements follow the security-hardening release train (breaking).**
  `armature-log` 0.2 → 0.3. Those releases change public APIs and secure-by-default behaviour
  (see each crate's CHANGELOG); this crate's minor moves with them so a
  downstream build can't mix it with the previous sibling releases. No code
  changes in this crate.

## [0.2.2] - 2026-09-15

### Security

- Require `rustls` 0.23.45 or later, which fixes RUSTSEC-2026-0285 (TLS 1.3 handshake messages accepted across encryption-level boundaries).

