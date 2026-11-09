---
$schema: https://straion.com/schemas/rule/v1.json
id: cf4e1041-3e6f-4472-a3ee-72c779df948f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST put `--` before user-supplied positional arguments in commands to prevent option injection.

## Examples

```python kind=violating
subprocess.run(["git", "log", branch], check=True, timeout=30)
```

```python kind=compliant
subprocess.run(["git", "log", "--end-of-options", branch], check=True, timeout=30)
```

```python kind=compliant
subprocess.run(["tar", "-xf", "--", archive], check=True, timeout=60)
```
