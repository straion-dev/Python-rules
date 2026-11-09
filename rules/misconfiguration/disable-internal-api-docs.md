---
$schema: https://straion.com/schemas/rule/v1.json
id: a7547036-d609-436d-8638-11ce28ff7ff6
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - fastapi
provenance:
  updatedBy: <straion>
---

SHOULD disable `/docs` and `/openapi.json` in production for internal APIs.

## Examples

```python kind=compliant
app = FastAPI(docs_url=None, redoc_url=None, openapi_url=None)
```
