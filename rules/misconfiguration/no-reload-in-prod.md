---
$schema: https://straion.com/schemas/rule/v1.json
id: cb8e4b2b-8223-40fc-8264-92bb5d6184f5
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT run the server with `--reload` in production.

## Examples

```bash kind=violating
uvicorn app.main:app --reload
```

```bash kind=compliant
uvicorn app.main:app --host 0.0.0.0 --port 8000 --workers 4
```
