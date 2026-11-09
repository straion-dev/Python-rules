---
$schema: https://straion.com/schemas/rule/v1.json
id: 7d63091d-2f31-4e59-afb9-c6761095626b
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST set a timeout on every network call.

## Examples

```python kind=violating
requests.get(url)
```

```python kind=compliant
requests.get(url, timeout=10)
```
