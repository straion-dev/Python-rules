---
$schema: https://straion.com/schemas/rule/v1.json
id: 81f56f1e-575f-43e8-af77-719c6e350094
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST keep framework CSRF protection enabled for cookie-authenticated, state-changing requests.

## Examples

```python kind=violating
@csrf_exempt
def update_profile(request): ...
```
