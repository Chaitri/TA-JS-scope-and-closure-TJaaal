1. Implement `forEach` array method using Array.reduce

- `forEach` accepts two parameter array and callback
- It does not return anything
- It should work exactly like array `forEach` method

```js
function forEach(arr, cb) {
  arr.reduce((acc, elm, i, arr) => {
    cb(elm, i, arr);
  }, arr[0]);
}

forEach(['Sam', 'Jon', 'Arya'], (name, i, arr) =>
  console.log(name + name, i, arr)
);
```

2. Implement `map` array method using Array.reduce

- `map` accepts two parameter array and callback
- It returns same size of array
- It should work exactly like array `map` method

```js

function map(arr, cb) {
  let mappedArr = arr.reduce(function (acc, elm) {
    let newStr = cb(elm);
    acc.push(newStr);
    return acc;
  }, []);
  return mappedArr;
}

map(['Sam', 'Jon', 'Arya'], (name) => name + name); // ['SamSam', 'JonJon', 'AryaArya']
```

3. Implement `filter` array method using Array.reduce

- `filter` accepts two parameter array and callback
- It returns same size or smaller array
- It should work exactly like array `filter` method

```js
function filter(arr, cb) {
  let filteredArr = arr.reduce((acc, elm) => {
    if(cb(elm)) {
      acc.push(elm);
    }
    return acc;
  }, []);
  return filteredArr;
}

filter(['Sam', 'Jon', 'Arya'], (name) =>
  name.startsWith('S')
); // ['Sam']
```
