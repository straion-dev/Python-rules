---
$schema: https://straion.com/schemas/rule/v1.json
id: b65c664a-ce07-4a86-a68c-9a845f381bbd
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST send a `Content-Security-Policy` header.

## Examples

```python kind=compliant
@app.middleware("http")
async def security_headers(request, call_next):
    response = await call_next(request)
    response.headers["Strict-Transport-Security"] = "max-age=31536000; includeSubDomains"
    response.headers["Content-Security-Policy"] = "default-src 'self'; frame-ancestors 'none'"
    response.headers["X-Content-Type-Options"] = "nosniff"
    response.headers["Referrer-Policy"] = "strict-origin-when-cross-origin"
    return response
```
