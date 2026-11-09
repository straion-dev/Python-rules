---
$schema: https://straion.com/schemas/rule/v1.json
id: c4ebe279-235a-4b9a-9d41-481f18235952
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT include stack traces, SQL, file paths or library versions in error responses to clients.

## Examples

```python kind=violating
return JSONResponse({"error": traceback.format_exc()}, status_code=500)
```

```python kind=compliant
return JSONResponse({"error": "Internal error", "correlation_id": cid}, status_code=500)
```
