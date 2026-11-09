---
$schema: https://straion.com/schemas/rule/v1.json
id: 683b33e8-4078-4209-90fe-9d954545773a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT select modules, classes or attributes by user string (`importlib.import_module`, `getattr`) without an allowlist.

## Examples

```python kind=violating
getattr(exporters, fmt)(report)
```

```python kind=compliant
EXPORTERS = {"csv": export_csv, "json": export_json}
exporter = EXPORTERS.get(fmt)
if exporter is None:
    raise ValidationError("unsupported format")
exporter(report)
```
