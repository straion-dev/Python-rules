---
$schema: https://straion.com/schemas/rule/v1.json
id: 1bbdace6-f6f9-43c0-b337-1ea291d6794d
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `print` for operational events.

## Examples

```python kind=violating
print("user logged in", user.id)
```

```python kind=compliant
logger.info("user logged in", extra={"user_id": user.id})
```
