---
$schema: https://straion.com/schemas/rule/v1.json
id: 44abd114-9388-434e-96f0-6c225c128678
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST deny when an authorization, validation, signature or rate-limit check raises or returns an unexpected value.

## Examples

```python kind=violating
try:
    allowed = policy.check(user, action)
except PolicyError:
    allowed = True
```

```python kind=compliant
try:
    allowed = policy.check(user, action)
except PolicyError:
    logger.exception("policy check failed")
    allowed = False
if allowed is not True:
    raise PermissionDenied
```
