---
$schema: https://straion.com/schemas/rule/v1.json
id: d9ba6f9a-ca3f-4984-81a6-e828d80b3e02
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

SHOULD prefer a library over a subprocess for OS operations.

## Examples

```python kind=violating
subprocess.run(["rm", "-rf", "--", path], check=True, timeout=30)
```

```python kind=compliant
shutil.rmtree(path)
```
