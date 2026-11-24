# kestrel

A platform test for Tinfoil Containers. It runs a small probe in a secure enclave and checks three things:

1. The container deploys from this config and answers `GET /ping`.
2. `GET /attest?nonce=<64 hex>` returns a fresh attestation for the caller's nonce.
3. `GET /sign?nonce=<64 hex>` signs the nonce with an attested Ed25519 key that the attestation names.

The probe image is private. This repo holds only the config and Tinfoil's release workflows, unchanged from [tinfoil-containers-template](https://github.com/tinfoilsh/tinfoil-containers-template). The image is pinned by its SHA-256 digest.

This repo is temporary.
