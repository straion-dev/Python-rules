---
$schema: https://straion.com/schemas/rule/v1.json
id: 81e1da74-37fd-4595-b1b6-78f6f08b7ffc
meta:
  tags:
    - infrastructure
    - security
provenance:
  updatedBy: <straion>
---

MUST pin container base images by digest.

## Examples

```dockerfile kind=violating
FROM python:3.13-slim
```

```dockerfile kind=compliant
FROM python:3.13-slim@sha256:<digest>
```
