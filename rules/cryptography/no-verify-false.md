---
$schema: https://straion.com/schemas/rule/v1.json
id: 48903579-02a3-4fee-a40b-aa5063c69432
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT pass `verify=False` to HTTP clients.

## Examples

```python kind=violating
requests.get(url, verify=False, timeout=10)
```
