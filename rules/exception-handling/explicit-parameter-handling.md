---
$schema: https://straion.com/schemas/rule/v1.json
id: c7c5e603-d7b5-42ac-8b76-4ce88a138a86
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST handle missing and extra parameters explicitly with schema validation using `extra="forbid"`.

## Examples

```python kind=violating
name = request.json["name"]  # KeyError -> 500
```

```python kind=compliant
payload = CreateItem.model_validate(request.json)  # extra="forbid"
```
