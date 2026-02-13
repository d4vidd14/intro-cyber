# Cryptography, TLS & PKI (Fundamentals)

## Kerckhoffs's principle
A cryptosystem should remain secure even if everything about the system is public, except the **key**.
Security must rely on strong algorithms and secret keys, not on “hidden” methods.

## Symmetric vs Asymmetric cryptography
### Symmetric (same key)
- Same key used to encrypt/decrypt.
- Fast, used for bulk data encryption.
- Examples: AES.

### Asymmetric (key pair)
- Public key encrypts / verifies, private key decrypts / signs.
- Slower, used for key exchange, signatures, identity.
- Examples: RSA, ECC (elliptic curve).

## Related concepts
- **Obfuscation (Ofuscar)**: hide/transform code or data to make analysis harder (not true encryption).
- **Hash**: one-way function used for integrity/verification (e.g., SHA-256). Not reversible.
- **Rainbow tables**: precomputed tables to crack weak hashes (especially unsalted).
- **Salt**: random value added before hashing to defeat rainbow tables and make hashes unique.
- **Nonce**: “number used once” to prevent replay and add freshness in protocols.
- **Entropy**: measure of randomness/unpredictability (good keys need high entropy).

## Secure protocols
- **SSL/TLS**: protocol family that provides encryption + integrity + authentication for communications.
  - SSL is legacy; modern systems use TLS.
- **TLS handshake**: negotiation phase where client and server agree on parameters and establish keys.
  - Typically involves authentication (certificates) and key exchange.

### Common terms in TLS
- **Algorithms / ciphers**: encryption and hashing functions used within TLS.
- **SNI (Server Name Indication)**: extension that tells the server which hostname the client wants during handshake (needed for multiple domains on one IP).
- **OCSP**: online certificate status protocol (checks if a certificate is revoked).
- **X.509**: standard format for public key certificates.

## PKI (Public Key Infrastructure)
PKI is the ecosystem that manages digital certificates and trust:
- **CA (Certificate Authority)**: entity that issues certificates.
- **Certificate (X.509)**: binds a public key to an identity (domain/org) via CA signature.
- Chain of trust: client trusts a root CA → validates intermediate CA → validates server certificate.

## Practical takeaways
- Use **TLS** for confidentiality/integrity on the network.
- Prefer salted hashes for password storage (and strong password hashing algorithms).
- Always validate certificates (avoid MITM risks).
