---
$schema: https://straion.com/schemas/rule/v1.json
id: dd8c76e9-02f3-4ac1-bb45-63ed23d45875
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST map user-supplied SQL identifiers (table, column, sort fields) through an allowlist.

## Examples

```python kind=violating
cur.execute(f"SELECT * FROM products ORDER BY {request.args['sort']}")
```

```python kind=compliant
SORT_FIELDS = {"name": "name", "created": "created_at"}
order_by = SORT_FIELDS.get(request.GET.get("sort"), "created_at")
products = Product.objects.order_by(order_by)
```
