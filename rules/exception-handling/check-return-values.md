---
$schema: https://straion.com/schemas/rule/v1.json
id: 28792e94-9567-4595-b6ae-eb9454c68d3f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST check return values and status codes (`response.raise_for_status()`, `check=True` for subprocess).

## Examples

```python kind=violating
data = requests.get(url, timeout=10).json()
```

```python kind=compliant
resp = requests.get(url, timeout=10)
resp.raise_for_status()
data = resp.json()
```
