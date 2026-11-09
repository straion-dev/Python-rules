---
$schema: https://straion.com/schemas/rule/v1.json
id: 125be7f8-bb99-44b0-8dfe-ab47516a0d74
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST generate security-relevant randomness (tokens, IDs, nonces, reset codes, salts) with `secrets` or `os.urandom`.

## Examples

```python kind=violating
token = str(random.random())
```

```python kind=compliant
token = secrets.token_urlsafe(32)
```
