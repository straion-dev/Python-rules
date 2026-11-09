---
$schema: https://straion.com/schemas/rule/v1.json
id: 8a9b9d68-bd40-46b8-9582-52617ad946d0
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST deserialize untrusted data as JSON or with `yaml.safe_load` into validated schemas.

## Examples

```python kind=compliant
payload = OrderIn.model_validate_json(request.body)
```
