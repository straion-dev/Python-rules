---
$schema: https://straion.com/schemas/rule/v1.json
id: faf38d4b-9b78-4359-935a-e51b5092cd27
meta:
  tags:
    - infrastructure
    - security
provenance:
  updatedBy: <straion>
---

MUST run containers as a non-root user.

## Examples

```dockerfile kind=compliant
RUN useradd --system --uid 10001 app
USER app
```
