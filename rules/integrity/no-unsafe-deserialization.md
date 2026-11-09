---
$schema: https://straion.com/schemas/rule/v1.json
id: 461e2a95-942a-47bd-a6cd-47b64a2a68c8
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT deserialize untrusted data with `pickle`, `marshal`, `shelve`, `dill`, `cloudpickle`, `joblib.load`, `jsonpickle`, or `yaml.load`/`yaml.unsafe_load`.

## Examples

```python kind=violating
data = pickle.loads(request.body)
```

```python kind=violating
cfg = yaml.load(text)
```

```python kind=compliant
cfg = yaml.safe_load(text)
```
