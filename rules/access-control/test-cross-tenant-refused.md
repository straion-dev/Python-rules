---
$schema: https://straion.com/schemas/rule/v1.json
id: ad5d261c-982a-49af-bcca-926142af348e
meta:
  tags:
    - security
    - testing
provenance:
  updatedBy: <straion>
---

MUST add a test for every protected endpoint proving a different user or tenant is refused.

## Examples

```python kind=compliant
def test_other_user_cannot_read_order(client, alice_order, bob_headers):
    resp = client.get(f"/orders/{alice_order.id}", headers=bob_headers)
    assert resp.status_code == 404
```
