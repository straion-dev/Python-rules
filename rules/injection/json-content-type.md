---
$schema: https://straion.com/schemas/rule/v1.json
id: 7381572d-ab0b-4546-8451-519328829378
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST serve JSON API responses with `Content-Type: application/json`.

## Examples

```python kind=violating
return json.dumps(data)  # Flask sends text/html
```

```python kind=compliant
return jsonify(data)
```
