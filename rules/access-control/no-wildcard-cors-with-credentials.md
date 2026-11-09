---
$schema: https://straion.com/schemas/rule/v1.json
id: 0f5905e5-6898-4105-877e-353d72212a0c
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT combine `allow_origins=["*"]` with `allow_credentials=True`.

## Examples

```python kind=violating
app.add_middleware(CORSMiddleware, allow_origins=["*"], allow_credentials=True)
```
