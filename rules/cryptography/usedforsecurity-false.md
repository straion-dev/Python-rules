---
$schema: https://straion.com/schemas/rule/v1.json
id: 6125bdfe-6572-4da6-9ce1-7edee59d7a3a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST pass `usedforsecurity=False` when using MD5 or SHA-1 for non-security checksums.

## Examples

```python kind=compliant
hashlib.md5(data, usedforsecurity=False).hexdigest()
```
