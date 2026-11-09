---
$schema: https://straion.com/schemas/rule/v1.json
id: 4f049137-8cd1-48b1-a341-a09eebe43d8d
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use user-controlled strings as `str.format` or `format_map` templates.

## Examples

```python kind=violating
message = request.form["template"].format(user=current_user)  # "{user.__init__.__globals__}" leaks secrets
```

```python kind=compliant
message = string.Template(request.form["template"]).safe_substitute(name=current_user.name)
```
