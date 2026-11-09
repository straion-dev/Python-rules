---
$schema: https://straion.com/schemas/rule/v1.json
id: 8a1c4b0a-83f3-4c8d-9640-a0fe040761f2
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST log security events with timestamp, user/account ID, source IP, request/correlation ID, action and outcome.

## Examples

```python kind=compliant
logger.warning("access denied", extra={
    "event": "authz.denied", "user_id": user.id, "source_ip": ip,
    "request_id": request_id, "action": "order.delete", "outcome": "deny",
})
```
