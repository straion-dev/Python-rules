---
$schema: https://straion.com/schemas/rule/v1.json
id: 0053f1e3-3cb0-4514-b69f-56c85d0ee291
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST mark deliberately public endpoints explicitly (e.g. a `@public` decorator or allowlist) so the default is closed.

## Examples

```python kind=compliant
@router.get("/health")
@public  # explicit opt-out; every other route requires auth by default
def health(): ...
```
