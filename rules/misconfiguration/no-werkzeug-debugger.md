---
$schema: https://straion.com/schemas/rule/v1.json
id: a2f1fe0d-63a0-499d-948d-c52192b56c86
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - flask
provenance:
  updatedBy: <straion>
---

MUST NOT use `app.run(debug=True)` or the Werkzeug debugger in production.

## Examples

```python kind=violating
app.run(debug=True)
```
