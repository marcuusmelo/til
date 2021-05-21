# Application Layer Encryption
## Application Layer vs Infrastructure Layer Encryption
Both application layer encryption and infrastructure layer encryption are part of the overall security of your system.

You can think about driving security, both the security related to the car (application layer) and de security related to the road (infrastructure layer) will impact the driving security.


### Examples of Infrastructure Layer Encryption
- HTTPS/TLS
- VPNs, IPSEC
- Service Mesh
- Full Disk Encryption
- DB Encrypt


### When you need more application layer encryption?
When you need security travelling with data. Application layer encryption increases privacy.


### Encryption terminology:
- Encrypt: make something secret using a key
- Decrypt: Make something readable using a key
- Sign: Prove integrity using a key
- Verify: Check integrity using a key


## Symmetric Encryption vs. Asymmetric Encryption
### Symmetric Encryption
- Uses the same key for encrypt, decrypt, sign and verify
- Fast and efficient
- Challenge on how to share data

### Asymmetric Encryption (PKI)
- The key has 2 parts: public and private
- Used when you need to do key exchange

## What to do with the keys?
### Symmetric keys
- Encrypt and exchange using asymmetric keys

### Asymmetric public keys
- Share freely
- Certificate Authority, CSR, proves that you hold the private key

### Asymmetric private keys
- Store it in a file encrypted with password
- Secrets manager: 1Password, Vault, etc
