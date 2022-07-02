# `for...of` iterations - [@abozhilov](https://twitter.com/abozhilov)

## Iterating over an `Array`

```js
const arr = ['A', 'B', 'C', 'D', 'E', 'F'];

for (const i of arr) {
    console.log(i); // 'A', 'B', ..., 'F'
}

for (const entry of arr.entries()) {
    console.log(entry); // [0, 'A'], [1, 'B'], ..., [5, 'F']
}

for (const key of arr.keys()) {
    console.log(key); // 0, 1, ..., 5
}
```

## Iterating over a `String`

```js
const str = 'ABCDEF';

for (const i of str) {
    console.log(i); // 'A', 'B', ..., 'F'
}
```

## Iterating over a `Map`

```js
const map = new Map([
    [1, 'A'],
    [2, 'B'],
    [3, 'C'],
    [4, 'D'],
    [5, 'E'],
    [6, 'F']
]);

for (const i of map) {
    console.log(i); // [1, 'A'], [2, 'B'], ..., [6, 'F']
}

for (const entry of map.entries()) {
    console.log(entry); // [1, 'A'], [2, 'B'], ..., [6, 'F']
}

for (const key of map.keys()) {
    console.log(key); // 1, 2, ..., 6
}

for (const value of map.values()) {
    console.log(value); // 'A', 'B', ..., 'F'
}
```


## Iterating over a `Set`

```js
const set = new Set(['A', 'B', 'C', 'D', 'E', 'F']);

for (const i of set) {
    console.log(i); // 'A', 'B', ..., 'F'
}

for (const entry of set.entries()) {
    console.log(entry); // ['A', 'A'], ['B', 'B'], ..., ['F', 'F']
}

for (const key of set.keys()) {
    console.log(key); // 'A', 'B', ..., 'F'
}
```