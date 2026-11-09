---
$schema: https://straion.com/schemas/rule/v1.json
id: 78d8a403-28df-48f3-842b-eb5c6b057808
meta:
  tags:
    - architecture
    - security
provenance:
  updatedBy: <straion>
---

MUST enforce business limits (quantities, amounts, per-user caps, workflow state transitions) server-side in the domain/service layer.

## Examples

```python kind=compliant
TRANSITIONS = {"draft": {"submitted"}, "submitted": {"approved", "rejected"}}

def transition(order, new_status):
    if new_status not in TRANSITIONS.get(order.status, set()):
        raise InvalidTransition(order.status, new_status)
    order.status = new_status
```
