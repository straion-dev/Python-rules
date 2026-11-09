---
$schema: https://straion.com/schemas/rule/v1.json
id: a1faf272-4e7a-4b22-8221-fe00b343bf0f
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

MUST set `DEBUG = False` in production.

## Examples

```python kind=violating
DEBUG = True
```

```python kind=compliant
DEBUG = os.environ.get("DJANGO_DEBUG") == "1"  # only set in the dev profile
```
