---
$schema: https://straion.com/schemas/rule/v1.json
id: 0a09f9cd-322d-41b7-88e4-0f5442d48ad4
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST build HTML with templates instead of concatenating user input into HTML strings in Python code.

## Examples

```python kind=violating
return f"<h1>Hello {request.args['name']}</h1>"
```

```python kind=compliant
return render_template("hello.html", name=request.args["name"])
```
