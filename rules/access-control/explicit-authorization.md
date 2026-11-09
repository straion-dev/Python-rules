---
$schema: https://straion.com/schemas/rule/v1.json
id: aa6b7d3e-3e21-47ad-bb5a-1415dd25c463
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST perform an explicit authorization check on every endpoint or view unless it is deliberately public.

## Examples

```python kind=compliant
@router.delete("/projects/{pid}")
def delete_project(pid: int, user: User = Depends(require_permission("project:delete"))): ...
```
