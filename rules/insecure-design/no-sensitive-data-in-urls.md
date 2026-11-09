---
$schema: https://straion.com/schemas/rule/v1.json
id: b2361a89-5e40-4796-879e-972a83b419c8
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT put sensitive data (tokens, passwords, PII) in URLs or query strings.

## Examples

```python kind=violating
requests.get(f"{API}/reports?api_key={key}", timeout=10)
```

```python kind=compliant
requests.get(f"{API}/reports", headers={"Authorization": f"Bearer {key}"}, timeout=10)
```
