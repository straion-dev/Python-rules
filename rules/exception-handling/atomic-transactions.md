---
$schema: https://straion.com/schemas/rule/v1.json
id: 0f1ec068-e72f-4449-8779-c4405f5a549f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST run multi-step state changes inside one transaction (`transaction.atomic()`, `with session.begin():`).

## Examples

```python kind=compliant
with session.begin():
    session.add(order)
    inventory.reserve(session, order.items)
```
