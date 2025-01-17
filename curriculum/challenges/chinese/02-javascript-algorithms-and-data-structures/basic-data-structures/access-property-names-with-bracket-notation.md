---
id: 587d7b7c367417b2b2512b1a
title: 使用方括号访问属性名称
challengeType: 1
forumTopicId: 301150
dashedName: access-property-names-with-bracket-notation
---

# --description--

In the first object challenge we mentioned the use of bracket notation as a way to access property values using the evaluation of a variable. For instance, imagine that our `foods` object is being used in a program for a supermarket cash register. We have some function that sets the `selectedFood` and we want to check our `foods` object for the presence of that food. This might look like:

```js
let selectedFood = getCurrentFood(scannedItem);
let inventory = foods[selectedFood];
```

上述代码会先读取 `selectedFood` 变量的值，并返回 `foods` 对象中以该值命名的属性所对应的属性值。 若没有以该值命名的属性，则会返回 `undefined`。 有时候对象的属性名在运行之前是不确定的，或者我们需要动态地访问对象的属性值。在这些场景下，方括号表示法就变得十分有用。

# --instructions--

我们已经定义了 `checkInventory` 函数，它接受一个被扫描到的商品名作为输入参数。 请让这个函数返回 `foods` 对象中，以 `scannedItem` 的值所命名的属性对应的属性值。 在本挑战中，只有合理有效的属性名会作为参数传入 `checkInventory`，因此你不需要处理参数无效的情况。

# --hints--

`checkInventory` 应是一个函数。

```js
assert.strictEqual(typeof checkInventory, 'function');
```

`foods` 对象应只包含以下键值对：`apples: 25`、`oranges: 32`、`plums: 28`、`bananas: 13`、`grapes: 35`、`strawberries: 27`。

```js
assert.deepEqual(foods, {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
});
```

`checkInventory("apples")` 应返回 `25`。

```js
assert.strictEqual(checkInventory('apples'), 25);
```

`checkInventory("bananas")` 应返回 `13`。

```js
assert.strictEqual(checkInventory('bananas'), 13);
```

`checkInventory("strawberries")` 应返回 `27`。

```js
assert.strictEqual(checkInventory('strawberries'), 27);
```

# --seed--

## --seed-contents--

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  // Only change code below this line

  // Only change code above this line
}

console.log(checkInventory("apples"));
```

# --solutions--

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  return foods[scannedItem];
}
```
