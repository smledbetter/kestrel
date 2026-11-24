# kestrel

A Tinfoil Containers config for a private demo app. It runs one container in a secure enclave.

- The app image is private and pinned by its SHA-256 digest.
- The enclave makes two attested keys at boot, `app-signer` (Ed25519) and `app-channel` (P-256), and grants them to the app. Both public keys appear in the attestation.
- The app reaches one outside host, `inference.tinfoil.sh`.
- The app's API key is a Tinfoil secret. It is not in this repo.

This repo holds only this README, `tinfoil-config.yml`, and Tinfoil's release workflows, unchanged from [tinfoil-containers-template](https://github.com/tinfoilsh/tinfoil-containers-template). It is temporary.
