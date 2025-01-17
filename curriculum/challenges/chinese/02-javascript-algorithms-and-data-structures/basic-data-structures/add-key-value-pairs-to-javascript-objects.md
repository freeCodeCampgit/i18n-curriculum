---
id: 587d7b7c367417b2b2512b18
title: 将键值对添加到对象中
challengeType: 1
forumTopicId: 301153
dashedName: add-key-value-pairs-to-javascript-objects
---

# --description--

At their most basic, objects are just collections of <dfn>key-value</dfn> pairs. In other words, they are pieces of data (<dfn>values</dfn>) mapped to unique identifiers called <dfn>properties</dfn> (<dfn>keys</dfn>). Take a look at an example:

```js
const tekkenCharacter = {
  player: 'Hwoarang',
  fightingStyle: 'Tae Kwon Doe',
  human: true
};
```

上面的代码定义了一个叫做 `tekkenCharacter` 的“铁拳”游戏人物对象。 它有三个属性，每个属性都对应一个特定的值。 如果我们想为它再添加一个叫做 `origin` 的属性，可以这样写：

```js
tekkenCharacter.origin = 'South Korea';
```

上面的代码中，我们使用了点号表示法。 如果我们现在输出 `tekkenCharacter` 对象，便可以看到它具有 `origin` 属性。 接下来，因为这个人物在游戏中有着与众不同的橘色头发， 我们可以通过方括号表示法来为它添加这个属性，像这样：

```js
tekkenCharacter['hair color'] = 'dyed orange';
```

如果要设置的属性中存在空格，或者要设置的属性是一个变量，那我们必须使用方括号表示法（bracket notation）来为对象添加属性。 在上面的代码中，我们把属性（hair color）放到引号里，以此来表示整个字符串都是需要设置的属性。 如果我们不加上引号，那么中括号里的内容会被当作一个变量来解析，这个变量对应的值就会作为要设置的属性， 请看这段代码：

```js
const eyes = 'eye color';

tekkenCharacter[eyes] = 'brown';
```

执行以上所有示例代码后，对象会变成这样：

```js
{
  player: 'Hwoarang',
  fightingStyle: 'Tae Kwon Doe',
  human: true,
  origin: 'South Korea',
  'hair color': 'dyed orange',
  'eye color': 'brown'
};
```

# --instructions--

我们已经为你创建了包含三个项目的 `foods` 对象。 请使用上述任意语法，来为 foods 对象添加如下三个键值对：`bananas` 属性，值为 `13`；`grapes` 属性，值为 `35`；`strawberries` 属性，值为 `27`。

# --hints--

`foods` 应为一个对象。

```js
assert(typeof foods === 'object');
```

`foods` 应有一个值为 `13` 的 `bananas` 属性。

```js
assert(foods.bananas === 13);
```

`foods` 应有一个值为 `35` 的 `grapes` 属性。

```js
assert(foods.grapes === 35);
```

`foods` 应有一个值为 `27` 的 `strawberries` 属性。

```js
assert(foods.strawberries === 27);
```

`foods` 对象的定义不应更改。

```js
assert(
  __helpers.removeJSComments(code).search(/let foods/) === -1 &&
  __helpers.removeJSComments(code).search(/const\s+foods\s*=\s*{\s*apples:\s*25,\s*oranges:\s*32,\s*plums:\s*28\s*};/
) !== -1
);
```

# --seed--

## --seed-contents--

```js
const foods = {
  apples: 25,
  oranges: 32,
  plums: 28
};

// Only change code below this line

// Only change code above this line

console.log(foods);
```

# --solutions--

```js
const foods = {
  apples: 25,
  oranges: 32,
  plums: 28
};

foods['bananas'] = 13;
foods['grapes']  = 35;
foods['strawberries'] = 27;
```
