---
$schema: https://straion.com/schemas/rule/v1.json
id: be65426d-2bdc-4d83-86e2-13980aab518a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST treat LLM output as untrusted input to any interpreter (SQL, shell, HTML, tools).

## Examples

```python kind=violating
cur.execute(llm_response.text)
```

```python kind=violating
subprocess.run(llm_response.text, shell=True)
```
