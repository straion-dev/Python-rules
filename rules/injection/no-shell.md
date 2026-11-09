---
$schema: https://straion.com/schemas/rule/v1.json
id: 14c8d5ba-dd9c-4c56-9f96-cac1dd7940b8
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `shell=True`, `os.system` or `os.popen`.

## Examples

```python kind=violating
subprocess.run(f"ping -c 1 {host}", shell=True)
```

```python kind=violating
os.popen("ls " + directory)
```
