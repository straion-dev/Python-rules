---
$schema: https://straion.com/schemas/rule/v1.json
id: fa226dbe-0879-4421-a748-040482e45382
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST disable automatic redirects or re-validate each redirect hop for outbound requests to user-influenced URLs.

## Examples

```python kind=violating
requests.get(user_url, timeout=5)
```

```python kind=compliant
requests.get(user_url, allow_redirects=False, timeout=5)
```
