```
export const deepCopy = (object) => {
  if (object === null || typeof object !== 'object') {
    return object;
  }
  const copy = Array.isArray(object) ? [] : {};

  for (let key of Object.keys(object)) {
    copy[key] = deepCopy(object[key]);
  }

  return copy;
};
```

```
JSON.stringify(JSON.parse(object))
```
