---
$schema: https://straion.com/schemas/rule/v1.json
id: 30b5ef3a-cadf-4199-a557-8dcb73f2410b
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST use idempotency keys for retried operations such as payments and orders.

## Examples

```python kind=compliant
key = request.headers["Idempotency-Key"]  # unique constraint on Payment.idempotency_key
payment, created = Payment.objects.get_or_create(
    idempotency_key=key, user=user, defaults={"amount": amount}
)
```
