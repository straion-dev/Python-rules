---
$schema: https://straion.com/schemas/rule/v1.json
id: a0262628-861d-4c62-94c1-9b0dd0bba2c4
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST set limits on request body size, upload size, page size, JSON depth, decompressed archive size, loop iterations and queue length.

## Examples

```python kind=compliant
limit = min(max(int(request.GET.get("limit", 20)), 1), 100)
items = Item.objects.filter(owner=request.user)[:limit]
```
