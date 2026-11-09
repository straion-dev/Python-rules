---
$schema: https://straion.com/schemas/rule/v1.json
id: 7d5fde7c-6604-432e-808c-a264a804df5a
meta:
  tags:
    - dependencies
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST pin each private package to its own index.

## Examples

```toml kind=compliant
[[tool.uv.index]]
name = "internal"
url = "https://pypi.internal.example.com/simple"
explicit = true

[tool.uv.sources]
acme-auth = { index = "internal" }
```
