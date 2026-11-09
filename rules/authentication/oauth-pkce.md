---
$schema: https://straion.com/schemas/rule/v1.json
id: 293003d0-2975-472f-9d5c-402dc4e2ed27
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use PKCE in OAuth authorization-code flows.

## Examples

```python kind=compliant
oauth.register("provider", ..., client_kwargs={"code_challenge_method": "S256"})
```
