---
$schema: https://straion.com/schemas/rule/v1.json
id: 2efbec29-3054-4f9b-a2af-d921a97f420a
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - django
    - flask
provenance:
  updatedBy: <straion>
---

MUST load the framework `SECRET_KEY` from the environment or a secret manager.

## Examples

```python kind=violating
SECRET_KEY = "django-insecure-3k@x..."
```

```python kind=compliant
SECRET_KEY = os.environ["DJANGO_SECRET_KEY"]
```
