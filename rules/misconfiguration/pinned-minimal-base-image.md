---
$schema: https://straion.com/schemas/rule/v1.json
id: e78a1ac8-bb60-4741-bf74-1da355063584
meta:
  tags:
    - infrastructure
    - security
provenance:
  updatedBy: <straion>
---

MUST build containers on a minimal, pinned base image.

## Examples

```dockerfile kind=violating
FROM python:latest
```

```dockerfile kind=compliant
FROM python:3.13-slim@sha256:<digest>
```
