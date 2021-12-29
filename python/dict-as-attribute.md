# Dict key as atrribute

Access dictionary as an attribute using dot notation with a help of SimpleNamespace that creates an empty class from which you can add or create attributes.

```python
from types import SimpleNamespace  

d = {
  "x": 100,
  "y": 200
}
ns = SimpleNamespace(**d)

print(ns.x) // 100
print(ns.y) // 200
```
