---
$schema: https://straion.com/schemas/rule/v1.json
id: 27f33608-d6eb-417f-9045-08b457274b69
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use OAEP padding for RSA encryption.

## Examples

```python kind=violating
public_key.encrypt(data, padding.PKCS1v15())
```

```python kind=compliant
public_key.encrypt(data, padding.OAEP(mgf=padding.MGF1(hashes.SHA256()), algorithm=hashes.SHA256(), label=None))
```
