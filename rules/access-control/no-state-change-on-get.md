---
$schema: https://straion.com/schemas/rule/v1.json
id: a8bb2460-6d44-426f-bdb2-39512cdd4aa6
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT perform state changes on GET requests.

## Examples

```python kind=violating
@app.get("/users/{uid}/delete")
def delete_user(uid: int): ...
```

```python kind=compliant
@app.delete("/users/{uid}")
def delete_user(uid: int, user: User = Depends(require_admin)): ...
```
