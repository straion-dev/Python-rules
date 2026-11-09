---
$schema: https://straion.com/schemas/rule/v1.json
id: 0ad9b769-6414-42e6-ace0-1d085b029fbb
meta:
  tags:
    - security
    - testing
provenance:
  updatedBy: <straion>
---

MUST add a test for every protected endpoint proving an unauthenticated user is refused.

## Examples

```python kind=compliant
def test_orders_require_auth(client):
    assert client.get("/orders/1").status_code == 401
```
