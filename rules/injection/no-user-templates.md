---
$schema: https://straion.com/schemas/rule/v1.json
id: b4dfcd00-9e2b-4ba1-a39c-1d5a41dd5650
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT render user input as a template (`Template(user_input)`, `render_template_string(user_input)`).

## Examples

```python kind=violating
return render_template_string(request.args["msg"])
```

```python kind=compliant
return render_template_string("<p>{{ msg }}</p>", msg=request.args["msg"])
```
