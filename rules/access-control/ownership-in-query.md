---
$schema: https://straion.com/schemas/rule/v1.json
id: df1ee8e3-a4f5-4673-94a4-b5aa87982d83
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST enforce record ownership in the query itself on every read, update and delete instead of fetching by ID and checking afterwards.

## Examples

```python kind=violating
order = Order.objects.get(id=oid)
```

```python kind=compliant
order = Order.objects.get(id=oid, owner=request.user)
```

```python kind=compliant
select(Order).where(Order.id == oid, Order.owner_id == user.id)
```
