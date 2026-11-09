---
$schema: https://straion.com/schemas/rule/v1.json
id: 274409af-a6de-494c-a6e0-203904d6c454
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST handle cancellation in asyncio code.

## Examples

```python kind=compliant
try:
    await process(job)
except asyncio.CancelledError:
    await job.release()
    raise
```
