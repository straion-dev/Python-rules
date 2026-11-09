---
$schema: https://straion.com/schemas/rule/v1.json
id: f7e98d30-d065-4991-86d1-756202a86819
meta:
  tags:
    - security
    - tooling
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT suppress security lint findings without justification.

## Examples

```python kind=violating
subprocess.run(cmd, shell=True)  # noqa
```

```python kind=compliant
data = yaml.load(f, Loader=CSafeLoader)  # noqa: S506 -- CSafeLoader is the safe C loader
```
