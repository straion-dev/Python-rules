---
$schema: https://straion.com/schemas/rule/v1.json
id: 4e10db13-f6ff-40a4-9181-f90fc81bbed0
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST invoke unavoidable subprocesses as `subprocess.run([...], shell=False, check=True, timeout=...)` with an argument list.

## Examples

```python kind=violating
os.system(f"convert {name} out.png")
```

```python kind=compliant
subprocess.run(["convert", "--", name, "out.png"], shell=False, check=True, timeout=30)
```
