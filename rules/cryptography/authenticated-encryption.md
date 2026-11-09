---
$schema: https://straion.com/schemas/rule/v1.json
id: 1245c9d0-3116-473a-ba1d-036bfae33429
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use only authenticated encryption (`AESGCM` or `ChaCha20Poly1305`) for symmetric encryption.

## Examples

```python kind=compliant
key = AESGCM.generate_key(bit_length=256)
nonce = os.urandom(12)  # fresh per message
ciphertext = AESGCM(key).encrypt(nonce, plaintext, associated_data)
```
