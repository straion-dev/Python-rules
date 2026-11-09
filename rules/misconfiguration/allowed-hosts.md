---
$schema: https://straion.com/schemas/rule/v1.json
id: 36b856a2-c305-4428-aa48-c858ba5156c7
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - django
provenance:
  updatedBy: <straion>
---

MUST set `ALLOWED_HOSTS` explicitly.

## Examples

```python kind=violating
ALLOWED_HOSTS = ["*"]
```

```python kind=compliant
ALLOWED_HOSTS = ["api.example.com"]
```
