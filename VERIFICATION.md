# The Abundance Declaration — Verification Guide

**Author:** Prometheus
**Publication Date:** [December 31, 2025]
**PGP Key Fingerprint:** [F66452213D36CB92B88BF9BB8656F983AF71BDA1]

---

## Files Included

- THE_ABUNDANCE_DECLARATION.pdf — The Declaration
- THE_ABUNDANCE_DECLARATION.pdf.asc — PGP Signature
- THE_ABUNDANCE_DECLARATION.pdf.sha256 — SHA-256 Hash
- THE_ABUNDANCE_DECLARATION.pdf.ots — Blockchain Timestamp Proof
- prometheus-public-key.asc — Prometheus Public Key
- VERIFICATION.md — This file

---

## Quick Verification (No Tools Needed)

**SHA-256 Hash:** [85500f219d0a8557aa7b94347e7aaf8f2aa217dde887464b1551b7568e7a8f04]

Compare this hash with the output of running the hash command on your downloaded PDF.

---

## Full Verification Steps

### 1. Verify PGP Signature

Install GPG:
- Mac: brew install gnupg
- Windows: https://www.gpg4win.org/
- Linux: sudo apt install gnupg

Import Prometheus public key:

    gpg --import prometheus-public-key.asc

Verify signature:

    gpg --verify THE_ABUNDANCE_DECLARATION.pdf.asc THE_ABUNDANCE_DECLARATION.pdf

Expected output: "Good signature from Prometheus"

### 2. Verify SHA-256 Hash

Mac/Linux:

    shasum -a 256 THE_ABUNDANCE_DECLARATION.pdf

Windows:

    certutil -hashfile THE_ABUNDANCE_DECLARATION.pdf SHA256

Compare output to hash above.

### 3. Verify Blockchain Timestamp

Install OpenTimestamps:

    pip install opentimestamps-client

Verify:

    ots verify THE_ABUNDANCE_DECLARATION.pdf.ots

This confirms the document existed at the timestamp date on the Bitcoin blockchain.

---

## Security Notice

The Abundance Declaration is intended to be built upon by citizens who take up the mantle of Prometheus.

All future communications from Prometheus will be signed with this PGP key.

Unsigned communications are reflective of the Prometheus community, not the original author.

---

## Key Distribution

Public key available at:
- Keyserver: keyserver.ubuntu.com
- Search for: [F66452213D36CB92B88BF9BB8656F983AF71BDA1]
