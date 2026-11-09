---
$schema: https://straion.com/schemas/rule/v1.json
id: f7e9cab0-0d8f-42eb-ab54-9fa1b3a4b96a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use unauthenticated CBC mode.

## Examples

```python kind=violating
Cipher(algorithms.AES(key), modes.CBC(iv)).encryptor()
```
