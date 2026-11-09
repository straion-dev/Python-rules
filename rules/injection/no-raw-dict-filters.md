---
$schema: https://straion.com/schemas/rule/v1.json
id: 6abe683b-4c41-4c70-8d4d-accfdef176c1
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT pass a raw user dict as a NoSQL/ORM query or filter.

## Examples

```python kind=violating
User.objects.filter(**request.json)
```

```python kind=violating
db.users.find(request.json)
```
