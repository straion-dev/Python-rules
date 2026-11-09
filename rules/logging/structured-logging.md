---
$schema: https://straion.com/schemas/rule/v1.json
id: a7d1a39c-de4c-41df-9057-aaa9cb19180d
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST use the `logging` module or `structlog` with structured, machine-parseable output.

## Examples

```python kind=compliant
logger = structlog.get_logger()
logger.info("order.created", order_id=order.id, user_id=user.id)
```
