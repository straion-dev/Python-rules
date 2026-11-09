---
$schema: https://straion.com/schemas/rule/v1.json
id: b87e9ac6-932c-46b3-9fd0-a531329f334c
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST verify the OAuth/OIDC `state` parameter on callbacks.

## Examples

```python kind=compliant
token = await oauth.provider.authorize_access_token(request)  # Authlib validates state
```
