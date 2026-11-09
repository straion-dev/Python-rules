---
$schema: https://straion.com/schemas/rule/v1.json
id: b994e312-69d2-44f9-8072-655cbad28b50
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST set the `Secure` attribute on cookies.

## Examples

```python kind=violating
response.set_cookie("sid", sid)
```

```python kind=compliant
response.set_cookie("sid", sid, secure=True, httponly=True, samesite="Lax")
```
