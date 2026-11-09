---
$schema: https://straion.com/schemas/rule/v1.json
id: 0257f30d-c511-4a6e-a836-854f97236de0
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

SHOULD NOT apply `|safe`, `Markup()` or `mark_safe()` to anything user-influenced.

## Examples

```python kind=violating
mark_safe(f"<b>{comment.author}</b>")
```

```python kind=compliant
format_html("<b>{}</b>", comment.author)
```
