---
$schema: https://straion.com/schemas/rule/v1.json
id: 6ecc3ec6-0fd2-4352-a727-dea1cbb9e552
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST catch the most specific exception at the point where you can actually handle it.

## Examples

```python kind=violating
try:
    cfg = load(path)
except Exception:
    cfg = {}
```

```python kind=compliant
try:
    cfg = load(path)
except FileNotFoundError:
    cfg = DEFAULT_CONFIG
```
