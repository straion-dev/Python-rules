---
$schema: https://straion.com/schemas/rule/v1.json
id: 794ef236-f859-4e2e-b3ea-09b6f66b3578
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST verify webhook signatures with `hmac.compare_digest` before processing the payload.

## Examples

```python kind=compliant
expected = hmac.new(WEBHOOK_SECRET, request.body, hashlib.sha256).hexdigest()
if not hmac.compare_digest(expected, request.headers.get("X-Signature", "")):
    raise PermissionDenied
```
