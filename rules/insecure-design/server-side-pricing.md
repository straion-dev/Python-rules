---
$schema: https://straion.com/schemas/rule/v1.json
id: e3f421c9-c8c5-4f1b-a366-e184f551286f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST recompute prices, totals and discounts server-side instead of trusting client-supplied values.

## Examples

```python kind=violating
charge(user, request.json["total"])
```

```python kind=compliant
charge(user, pricing.total_for(cart, user))
```
