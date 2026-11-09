---
$schema: https://straion.com/schemas/rule/v1.json
id: 6a0e96b1-4a7f-4615-88ac-1aa99879c230
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use RSA keys shorter than 2048 bits.

## Examples

```python kind=compliant
key = rsa.generate_private_key(public_exponent=65537, key_size=3072)
```
