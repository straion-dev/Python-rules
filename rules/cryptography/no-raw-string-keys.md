---
$schema: https://straion.com/schemas/rule/v1.json
id: b61145f5-b085-4cb8-9322-98d5e374bc0b
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use a password or string directly as a cryptographic key.

## Examples

```python kind=violating
AESGCM(password.encode().ljust(32, b"0"))
```
