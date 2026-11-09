---
$schema: https://straion.com/schemas/rule/v1.json
id: a7255bce-55a7-400b-8f08-8f23e86ba2f4
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use `TaskGroup` to manage asyncio tasks.

## Examples

```python kind=compliant
async with asyncio.TaskGroup() as tg:
    tg.create_task(fetch_profile(uid))
    tg.create_task(fetch_orders(uid))
```
