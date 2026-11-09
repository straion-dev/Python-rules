---
$schema: https://straion.com/schemas/rule/v1.json
id: 4c593acc-707e-4e6c-8dc4-9dc6a49f6f7a
meta:
  tags:
    - architecture
    - security
provenance:
  updatedBy: <straion>
---

MUST define one central error handler per app (Django middleware, Flask `errorhandler`, FastAPI `exception_handler`).

## Examples

```python kind=compliant
@app.exception_handler(Exception)
async def unhandled(request: Request, exc: Exception):
    cid = request.state.request_id
    logger.exception("unhandled error", extra={"request_id": cid})
    return JSONResponse({"error": "Internal error", "correlation_id": cid}, status_code=500)
```
