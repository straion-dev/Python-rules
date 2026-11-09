---
$schema: https://straion.com/schemas/rule/v1.json
id: e7cb05c2-9a48-45a2-ba5c-f0345aaa8d38
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT store passwords in plaintext, encrypted, or with a fast hash (SHA-*, MD5).

## Examples

```python kind=violating
user.password = hashlib.sha256(password.encode()).hexdigest()
```
