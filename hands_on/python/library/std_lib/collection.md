# Collection

## DefaultDict

DefaultDict is subclass of dict.  
[defaultdict](https://docs.python.org/3/library/collections.html#collections.defaultdict)

an example of collections.defaultdict(dict)

```python
s = [('yellow', 1), ('blue', 2), ('yellow', 3), ('blue', 4), ('red', 1)]
d = defaultdict(list)
for k, v in s:
    d[k].append(v)

sorted(d.items())
[('blue', [2, 4]), ('red', [1]), ('yellow', [1, 3])]
```
