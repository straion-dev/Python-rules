---
$schema: https://straion.com/schemas/rule/v1.json
id: e5a62251-bc5c-45ed-b2c9-e69f37746de9
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST keep template autoescaping on (Jinja2 `autoescape=select_autoescape()` or framework defaults).

## Examples

```python kind=violating
env = Environment(loader=FileSystemLoader("templates"))  # autoescape is off by default
```

```python kind=compliant
env = Environment(loader=FileSystemLoader("templates"), autoescape=select_autoescape())
```
