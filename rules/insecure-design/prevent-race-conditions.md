---
$schema: https://straion.com/schemas/rule/v1.json
id: ae714a65-3cc0-444f-a88a-7940132fed59
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST prevent race conditions on critical state with DB constraints, transactions with row locks (`select_for_update` / `with_for_update`) or atomic updates.

## Examples

```python kind=compliant
with transaction.atomic():
    account = Account.objects.select_for_update().get(id=aid, owner=user)
    if account.balance < amount:
        raise InsufficientFunds
    account.balance -= amount
    account.save(update_fields=["balance"])
```

```python kind=compliant
updated = Account.objects.filter(id=aid, owner=user, balance__gte=amount).update(balance=F("balance") - amount)
if updated != 1:
    raise InsufficientFunds
```
