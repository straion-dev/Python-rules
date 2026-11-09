---
$schema: https://straion.com/schemas/rule/v1.json
id: b3f4b90a-e46a-4d82-b4bd-e371da9c7191
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use the framework's or a well-established identity solution (Django auth, an OIDC provider, `authlib`).

## Examples

```python kind=compliant
user = authenticate(request, username=username, password=password)
if user is not None:
    login(request, user)  # Django rotates the session key
```
