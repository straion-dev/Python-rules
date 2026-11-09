---
$schema: https://straion.com/schemas/rule/v1.json
id: b7ecaedf-8d81-45bf-b28a-2a7b08fbc3b1
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST configure CORS with an explicit origin allowlist only.

## Examples

```python kind=compliant
app.add_middleware(
    CORSMiddleware,
    allow_origins=["https://app.example.com"],
    allow_credentials=True,
)
```
