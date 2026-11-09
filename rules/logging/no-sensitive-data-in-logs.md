---
$schema: https://straion.com/schemas/rule/v1.json
id: d72105d5-4553-49fe-a003-b2e879094b7a
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT log secrets or sensitive data (passwords, tokens, session IDs, `Authorization`/`Cookie` headers, API keys, full card numbers, health data, unnecessary PII).

## Examples

```python kind=violating
logger.info("login %s with password %s", username, password)
```

```python kind=violating
logger.debug("headers: %s", dict(request.headers))
```
