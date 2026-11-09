---
$schema: https://straion.com/schemas/rule/v1.json
id: 2294dcad-3078-4a67-b379-868391d2486d
meta:
  tags:
    - security
    - testing
provenance:
  updatedBy: <straion>
---

MUST write misuse-case tests alongside use-case tests for every critical flow.

## Examples

```python kind=compliant
def test_coupon_cannot_be_applied_twice(client, cart, coupon):
    client.post(f"/carts/{cart.id}/coupons", json={"code": coupon.code})
    resp = client.post(f"/carts/{cart.id}/coupons", json={"code": coupon.code})
    assert resp.status_code == 409
```
