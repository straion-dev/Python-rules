---
$schema: https://straion.com/schemas/rule/v1.json
id: 12eb793f-415a-4cc6-aa10-bd7da7139814
meta:
  tags:
    - security
  frameworks:
    - django
provenance:
  updatedBy: <straion>
---

SHOULD NOT use `.raw()`, `.extra()` or `RawSQL` with interpolated values.

## Examples

```python kind=violating
User.objects.raw(f"SELECT * FROM auth_user WHERE email = '{email}'")
```

```python kind=compliant
User.objects.raw("SELECT * FROM auth_user WHERE email = %s", [email])
```
