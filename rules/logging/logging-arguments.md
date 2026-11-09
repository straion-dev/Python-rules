---
$schema: https://straion.com/schemas/rule/v1.json
id: 390b4fe4-f10c-499a-8c16-96d86cf6d233
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST pass untrusted values as logging arguments instead of pre-formatted f-strings.

## Examples

```python kind=violating
logger.info(f"login failed for {user}")
```

```python kind=compliant
logger.info("login failed for %s", user)
```
