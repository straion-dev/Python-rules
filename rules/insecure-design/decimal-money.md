---
$schema: https://straion.com/schemas/rule/v1.json
id: f1130011-7d21-4b1a-8644-f4aae3ffbbb0
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST use `decimal.Decimal`, not `float`, for monetary amounts.

## Examples

```python kind=violating
price = 0.1 + 0.2
```

```python kind=compliant
price = Decimal("0.10") + Decimal("0.20")
```
